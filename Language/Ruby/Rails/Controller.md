# Rails Controller

* Aggregate controller
* Composite controller

---

* [How DHH Organizes His Rails Controllers](http://jeromedalbert.com/how-dhh-organizes-his-rails-controllers/)
* [Examining The Internals Of The Rails Request/Response Cycle](http://www.rubypigeon.com/posts/examining-internals-of-rails-request-response-cycle/)
* [How to Reduce Controller Bloat with Interactors in Ruby](https://semaphoreci.com/community/tutorials/how-to-reduce-controller-bloat-with-interactors-in-ruby)
* [Better Rails Performance with JSON Patch](https://formapi.io/blog/posts/json-patch-with-rails-5-and-react/)

## Jim Werich

```ruby
def create
  CreateRunner.new(self).run(params[:employee],
    success: ->(employee) {
      flash[:notice] = msg
      redirect_to employee_path(employee)
    },
    failure: ->(employee) {
      @employee = employee
      render :new
    }
  )
end
```

## Routes

```ruby
resources :sessions, only: [:create, :show]

resources :users do
  post :activate, on: :collection
  resources :followers
end
```

## Serializers

```ruby
has_many :followers, serializer: Api::V1::UserSerializer
```

## Strong Parameters

[protected_attributes](https://github.com/rails/protected_attributes) is a gem for Mass Assignment which is being replaced by Strong Parameters. No longer supported in Rails 5.



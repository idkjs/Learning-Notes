# API Authentication

## UUID

* [shortid](https://github.com/dylang/shortid)
* [Hashids](http://hashids.org/)
* [Do you really need a UUID/GUID?](https://rclayton.silvrback.com/do-you-really-need-a-uuid-guid)

## JWT

* Expire token
* Refresh token if user still using app

> What's also interesting with JWT is that basically this is what Rails already does with encrypted/signed cookie based sessions, it just doesn't use JSON. But essentially it's an identical mechanism. There isn't really much value at all in using JWT over just using sessions with a Rails based API outside of the fact that JWT is a standard (though I think that's a pretty good benefit.) I might be interesting to implement JWT as an option for handling Rails sessions with support for both cookies and Authorization headers built in.

### Storage

**LocalStorage**

* Same domain access
* No CSRF
* Vulnerable to XSS attack
* Use CSP to execute script from a CDN only, thus prevent script on same origin from executing
* leaking token through XSS will have full control

**Cookies**

* Vulnerable to CSRF attack
* Secure, HttpOnly
* More secured with CORS with domain origin

```js
{
  "iss": "https://example.com",
  "exp": 1200392345,
  "sub": "m@example.com",
  "csrf": "sHjjdqDs13"
}
```
# Webpack

* [An Easy to Understand Webpack 4+ Configuration File with Comments](https://medium.com/@timurcatakli/an-easy-to-understand-webpack-4-configuration-file-with-comments-6213882e9edf)
* [Use lodash-es for tree shaking](https://www.npmjs.com/package/lodash-es)
* [Smaller Lodash bundles with Webpack and Babel](https://nolanlawson.com/2018/03/20/smaller-lodash-bundles-with-webpack-and-babel/)
* [**Webpack Academy Free Videos**](https://webpack.academy/courses/enrolled/104961)
* [Webpack v2 Quick Start](http://bendyworks.com/blog/webpack-v2-quick-start)
* [From zero to webpack, one error at the time](http://www.jumoel.com/2017/zero-to-webpack.html)
* [Webpack 2 Loader Variations](http://andrewhfarmer.com/webpack-2-loader-variations/)
* [Getting Started with webpack 2](https://blog.madewithenvy.com/getting-started-with-webpack-2-ed2b86c68783)
* [Migrating to Webpack 2](https://javascriptplayground.com/blog/2016/10/moving-to-webpack-2/)
* [How I cut my Webpack bundle size in half](http://jmduke.com/posts/how-i-cut-my-webpack-bundle-size-in-half/)
* [Deploying ES2015+ Code in Production Today](https://philipwalton.com/articles/deploying-es2015-code-in-production-today/)
* [Setting up Webpack, Babel and React from scratch, revisited](https://stanko.github.io/webpack-babel-react-revisited/)
* [Jarvis - A very intelligent browser based Webpack dashboard](https://github.com/zouhir/jarvis)
* [webpack-dashboard by FormidableLabs](https://github.com/FormidableLabs/webpack-dashboard)
* [Webpack Monitor](http://webpackmonitor.com/)
* [Keep webpack Fast: A Field Guide for Better Build Performance](https://slack.engineering/keep-webpack-fast-a-field-guide-for-better-build-performance-f56a5995e8f1)

```
▶ yarn global add webpack-bundle-size-analyzer
▶ yarn global add source-map-explorer

▶ ./node_modules/.bin/webpack --json | webpack-bundle-size-analyzer
▶ source-map-explorer bundle.min.js bundle.min.js.map
```

```js
module: {
  rules: [
    {
      test: /\.css$/,
      use: [
        'style-loader',
        'css-loader'
      ]
    }
  ]
}

// Production
module: {
  rules: [
    {
      test: /\.css$/,
      use: ExtractTextPlugin.extract({
        fallback: 'style-loader',
        use: 'css-loader'
      })
    }
  ]
}
```

```js
// Shim jQuery
resolve: {
  alias: {
    jquery: 'jquery/src/jquery'
  }
},

plugins: [
  new webpack.ProvidePlugin({
    $: 'jquery',
    jQuery: 'jquery'
  })
]
```

## Raw Webpack

Without using CRA, just playing around.

```
▶ npm init -y
▶ npm i -D babel-loader @babel/core @babel/preset-env webpack webpack-dev-server
▶ npm i -D eslint eslint-loader babel-eslint
▶ npm i -D file-loader url-loader
▶ npm i -D css-loader style-loader
▶ npm i -D webpack-manifest-plugin terser-webpack-plugin mini-css-extract-plugin optimize-css-assets-webpack-plugin case-sensitive-paths-webpack-plugin
▶ 
```

## Polyfill

* [What is a polyfill](https://blog.kentcdodds.com/what-is-a-polyfill-acab87e8481e)
* In CRA 2.0, support for IE9-11 is opt-in with react-app-polyfill

## Browserlist

* [Use `default`](https://twitter.com/jamiebuilds/status/1022568918949408768)

## Sourcemap

Don't use sourcemap in production!

* [Yet another explanation on sourcemap](https://medium.com/@trungutt/yet-another-explanation-on-sourcemap-669797e418ce)

## Webpack 4 (and Babel 7)

* [Create React App 2.0: Babel 7, Sass, and More](https://reactjs.org/blog/2018/10/01/create-react-app-v2.html)
* [The minimal Node.js with Babel Setup](https://www.robinwieruch.de/minimal-node-js-babel-setup/)
* [Working with Babel 7 and Webpack](https://www.thebasement.be/working-with-babel-7-and-webpack/)
* [How to set up React, webpack 4, and Babel 7 (2018)](https://www.valentinog.com/blog/react-webpack-babel/)
* [Webpack 4 + Babel 7](https://medium.com/oredi/webpack-with-babel-7-b61f7caa9565)
* [webpack 4: Changes Part 1 (week 24–25)](https://medium.com/webpack/webpack-4-changes-part-1-week-24-25-fd4d77674e55)
* [A tale of Webpack 4 and how to finally configure it in the right way](https://hackernoon.com/a-tale-of-webpack-4-and-how-to-finally-configure-it-in-the-right-way-4e94c8e7e5c1)
* Split chunking vs common chunking
* [mini-css-extract-plugin](https://github.com/webpack-contrib/mini-css-extract-plugin) - Support dynamic CSS import
* [Simple example](https://hackernoon.com/how-to-build-a-react-project-from-scratch-using-webpack-4-and-babel-56d4a26afd32)

## Starter Kits

* [Next.js, Razzle, CRA. Why you should use them for a next project](https://hackernoon.com/next-js-razzle-cra-why-you-should-use-them-for-a-next-project-a78d320de97f)
* [Universal React+GraphQL starter kit CLI](https://github.com/reactql/cli)
* [Outline - a very good project to study on](https://www.getoutline.com/)

## create-react-app

* [CRA v2](https://github.com/facebook/create-react-app/issues/5103)
* [Porting enterprise React app to create-react-app](https://medium.com/@KarandikarMihir/porting-enterprise-react-app-to-create-react-app-bfb565a25460)
* [Tweaking Configuration For React Scripts In Create React App](https://medium.com/@shubheksha/tweaking-configuration-for-react-scripts-in-create-react-app-d91e9d03a42f)
* [Configure create-react-app without ejecting](https://medium.com/@kitze/configure-create-react-app-without-ejecting-d8450e96196a)
* [RFC - babel-macros](https://github.com/facebookincubator/create-react-app/issues/2730)
* [Deploy a React App to S3 and CloudFront with AWS Mobile Hub](https://aws.amazon.com/blogs/mobile/deploy-a-react-app-to-s3-and-cloudfront-with-aws-mobile-hub/)
* [Add ESLint & Prettier to VS Code for a Create React App](https://www.youtube.com/watch?v=bfyI9yl3qfE)
* [Upgrading a create-react-app project to a SSR + code splitting setup](https://medium.com/bucharestjs/upgrading-a-create-react-app-project-to-a-ssr-code-splitting-setup-9da57df2040a)

---

What we want from CRA:

* Support for CSS Module
* Code splitting with react-loadable
* Storybook support

```
▶ yarn add husky lint-staged prettier
▶ yarn add flow-bin
▶ yarn add enzyme react-test-renderer
▶ yarn add react-styleguidist
▶ yarn add source-map-explorer

▶ yarn flow init
```

### Ejecting/Forking

* [Configure create-react-app without ejecting ⏏](https://medium.com/@kitze/configure-create-react-app-without-ejecting-d8450e96196a)
* [custom-react-scripts](https://github.com/kitze/custom-react-scripts)
* [Maintaining a fork of create-react-app as an alternative to ejecting](https://medium.com/@denis.zhbankov/maintaining-a-fork-of-create-react-app-as-an-alternative-to-ejecting-c555e8eb2b63)

## Tree Shaking

* Relies on ES6 module definition

```js
const shake = () => console.log('Shake')
const bake = () => console.log('Bake')
export { shake, bake }

// Shake it with
import { bake } from './shake'
bake()
```

## NamedModulesPlugin

* [name-all-modules-plugin](https://github.com/timse/name-all-modules-plugin)

Webpack, by default, assigns modules integer ids based on order. So when modules are changed, all ids could change, invalidating the cache. To use names instead of ids, we can use NamedModulesPlugin.

However, it will make the file sizes larger as well as expose internal file paths of modules to outside world.

Use Webpack NamedModulesPlugin to use deterministic module names instead of non-deterministic integer ids.

## Production

`webpack -p` is equivalent to:

```
webpack --optimize-minimize --define process.env.NODE_ENV="production"
```

Make sure you don't use it twice at the CLI and at the webpack.config.js file. Remove `-p` or you will have double minification which will result in bad bugs.

## Long-term Caching: Chunkhash

Note that Hash is for "entire" build and chunkhash is for individual file.

* [Predictable long term caching with Webpack - May 2017](https://medium.com/webpack/predictable-long-term-caching-with-webpack-d3eee1d3fa31)
* [Caching assets long term with Webpack - Sep 2016](https://medium.com/connect-the-dots/caching-assets-long-term-with-webpack-5ad24a4c39bd#.427deo91l)

Long-term bundle caching is achieved with content-based hashing policy: `[chunkhash]`.

You should not use `[chunkhash]` or `[hash]` for development as this will cause memory leak, because the dev server does not know when to clean up the old files.

## Hot Reload

* [Hot reload all the things!](https://hackernoon.com/hot-reload-all-the-things-ec0fed8ab0#.dok0iuu17)

## CRA

* [v1.0.0 release](https://github.com/facebookincubator/create-react-app/releases/tag/v1.0.0)
* [README](https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md)

## Performance

> Avoid PROD tasks in DEV, offload loaders to thread-loader, move rarely changed code to DllPlugin?

https://twitter.com/addyosmani/status/1148479395692048384

* [Tinder PWA case study](https://medium.com/@addyosmani/a-tinder-progressive-web-app-performance-case-study-78919d98ece0)

## Loaders

* svgr-loader


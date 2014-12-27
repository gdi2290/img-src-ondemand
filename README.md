# img-src-ondemand

Angular module that delays image loading to when it is about to appear on the screen

## Usage

### Include module

```js
angular.module('your-module', ['img-src-ondemand']);
```

### Use it

```html
<img src-ondemand="/abc.png" alt="plain text">
<img src-ondemand="{{myImage.url}}" alt="interpolation">

<ul>
  <li ng-repeat="image in images">
    <img src-ondemand="{{image.url}}" alt="within ng-repeat">
  </li>
<ul>
```

**or**

```html
<ul>
  <li ng-repeat="image in images">
    <img src-var-ondemand="image.url" alt="with a variable">
  </li>
</ul>
```

#### Listeners

> Even though angular mutates the attribute value when `image.url` changes,
the `src` attribute on the image will not change. This module was purely written
for loading images ondemand.

#### Angular 1.3+

*The followings are legit when using AngularJS 1.3+*

```html
<img src-ondemand="{{::image.url}}" alt="interpolate once">
<img src-var-ondemand="::image.url" alt="bind once">
```

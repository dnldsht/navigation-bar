<p align="center"><br><img src="https://user-images.githubusercontent.com/236501/85893648-1c92e880-b7a8-11ea-926d-95355b8175c7.png" width="128" height="128" /></p>
<h3 align="center">Navigation Bar</h3>
<p align="center"><strong><code>@donald_sh/capacitor-navigation-bar</code></strong></p>
<p align="center">
  Capacitor plugin for Navigation Bar manipulation.
</p>

<p align="center">
  <img src="https://img.shields.io/maintenance/yes/2024?style=flat-square" />
  <a href="https://github.com/hugotomazi/navigation-bar/actions?query=workflow%3A%22CI%22"><img src="https://img.shields.io/github/workflow/status/hugotomazi/navigation-bar/CI/master?style=flat-square" /></a>
  <a href="https://www.npmjs.com/package/@donald_sh/capacitor-navigation-bar"><img src="https://img.shields.io/npm/l/@donald_sh/capacitor-navigation-bar?style=flat-square" /></a>
<br>
  <a href="https://www.npmjs.com/package/@donald_sh/capacitor-navigation-bar"><img src="https://img.shields.io/npm/dw/@donald_sh/capacitor-navigation-bar?style=flat-square" /></a>
  <a href="https://www.npmjs.com/package/@donald_sh/capacitor-navigation-bar"><img src="https://img.shields.io/npm/v/@donald_sh/capacitor-navigation-bar?style=flat-square" /></a>
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
<a href="#contributors-"><img src="https://img.shields.io/badge/all%20contributors-5-orange?style=flat-square" /></a>
<!-- ALL-CONTRIBUTORS-BADGE:END -->
<br/>
<a href="https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=F9VPVZKHK4SZW">
  <img src="https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif" alt="Donate with PayPal button">
</a>
</p>
<br/>
<p align="center">
  <img height="450" src="https://github.com/hugotomazi/navigation-bar/blob/master/demoProject/src/assets/example.gif?raw=true">
</p>

## Maintainers

| Maintainer  | GitHub                                      | Social                                                          |
| ----------- | ------------------------------------------- | --------------------------------------------------------------- |
| Hugo Tomazi | [hugotomazi](https://github.com/hugotomazi) | [@donald_sh](https://br.linkedin.com/in/hugo-tomazi-299034101) |


## Install

```bash
npm install git+https://github.com/donald_sh/navigation-bar.git
npx cap sync
```

## Configuration

No configuration required for this plugin.

## API

<docgen-index>

* [`show()`](#show)
* [`hide()`](#hide)
* [`setColor(...)`](#setcolor)
* [`setTransparency(...)`](#settransparency)
* [`getColor()`](#getcolor)
* [`addListener(NavigationBarPluginEvents.SHOW, ...)`](#addlistenernavigationbarplugineventsshow)
* [`addListener(NavigationBarPluginEvents.HIDE, ...)`](#addlistenernavigationbarplugineventshide)
* [`addListener(NavigationBarPluginEvents.COLOR_CHANGE, ...)`](#addlistenernavigationbarplugineventscolor_change)
* [Interfaces](#interfaces)
* [Enums](#enums)

</docgen-index>

<docgen-api>
<!--Update the source file JSDoc comments and rerun docgen to update the docs below-->

### show()

```typescript
show() => Promise<void>
```

Display the navigation bar.

--------------------


### hide()

```typescript
hide() => Promise<void>
```

Hide the navigation bar.

--------------------


### setColor(...)

```typescript
setColor(options: ColorParameters) => Promise<void>
```

Change the color of the navigation bar.
*Support alpha hexadecimal numbers.

| Param         | Type                                                        |
| ------------- | ----------------------------------------------------------- |
| **`options`** | <code><a href="#colorparameters">ColorParameters</a></code> |

--------------------


### setTransparency(...)

```typescript
setTransparency(options: { isTransparent: boolean; }) => Promise<void>
```

Set the Transparency

| Param         | Type                                     |
| ------------- | ---------------------------------------- |
| **`options`** | <code>{ isTransparent: boolean; }</code> |

--------------------


### getColor()

```typescript
getColor() => Promise<{ color: string; }>
```

Gets the current color of the navigation bar in Hexadecimal.

**Returns:** <code>Promise&lt;{ color: string; }&gt;</code>

--------------------


### addListener(NavigationBarPluginEvents.SHOW, ...)

```typescript
addListener(event: NavigationBarPluginEvents.SHOW, listenerFunc: () => void) => Promise<PluginListenerHandle>
```

Event fired after navigation bar is displayed

| Param              | Type                                                                                 | Description |
| ------------------ | ------------------------------------------------------------------------------------ | ----------- |
| **`event`**        | <code><a href="#navigationbarpluginevents">NavigationBarPluginEvents.SHOW</a></code> | The event   |
| **`listenerFunc`** | <code>() =&gt; void</code>                                                           | Callback    |

**Returns:** <code>Promise&lt;<a href="#pluginlistenerhandle">PluginListenerHandle</a>&gt;</code>

--------------------


### addListener(NavigationBarPluginEvents.HIDE, ...)

```typescript
addListener(event: NavigationBarPluginEvents.HIDE, listenerFunc: () => void) => Promise<PluginListenerHandle>
```

Event fired after navigation bar is hidden

| Param              | Type                                                                                 | Description |
| ------------------ | ------------------------------------------------------------------------------------ | ----------- |
| **`event`**        | <code><a href="#navigationbarpluginevents">NavigationBarPluginEvents.HIDE</a></code> | The event   |
| **`listenerFunc`** | <code>() =&gt; void</code>                                                           | Callback    |

**Returns:** <code>Promise&lt;<a href="#pluginlistenerhandle">PluginListenerHandle</a>&gt;</code>

--------------------


### addListener(NavigationBarPluginEvents.COLOR_CHANGE, ...)

```typescript
addListener(event: NavigationBarPluginEvents.COLOR_CHANGE, listenerFunc: (returnObject: { color: string; }) => void) => Promise<PluginListenerHandle>
```

Event fired after navigation bar color is changed

| Param              | Type                                                                                         | Description |
| ------------------ | -------------------------------------------------------------------------------------------- | ----------- |
| **`event`**        | <code><a href="#navigationbarpluginevents">NavigationBarPluginEvents.COLOR_CHANGE</a></code> | The event   |
| **`listenerFunc`** | <code>(returnObject: { color: string; }) =&gt; void</code>                                   | Callback    |

**Returns:** <code>Promise&lt;<a href="#pluginlistenerhandle">PluginListenerHandle</a>&gt;</code>

--------------------


### Interfaces


#### ColorParameters

| Prop              | Type                 | Description                                                               |
| ----------------- | -------------------- | ------------------------------------------------------------------------- |
| **`color`**       | <code>string</code>  | Sets the new color of the navigation bar.                                 |
| **`darkButtons`** | <code>boolean</code> | Sets whether the default navigation bar buttons should be black or white. |


#### PluginListenerHandle

| Prop         | Type                                      |
| ------------ | ----------------------------------------- |
| **`remove`** | <code>() =&gt; Promise&lt;void&gt;</code> |


### Enums


#### NavigationBarPluginEvents

| Members            | Value                        | Description                                  |
| ------------------ | ---------------------------- | -------------------------------------------- |
| **`SHOW`**         | <code>'onShow'</code>        | Called after the navigation bar is displayed |
| **`HIDE`**         | <code>'onHide'</code>        | Called after navigation bar is hidden        |
| **`COLOR_CHANGE`** | <code>'onColorChange'</code> | Called after navigation bar color is changed |

</docgen-api>

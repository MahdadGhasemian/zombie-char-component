# Vue Zombie Character Component

![image](https://user-images.githubusercontent.com/1289797/38184554-1654a98c-367b-11e8-8620-655d88916c90.png)

A Vue component for [CryptoZombies.io](https://cryptoZombies.io).

You can generate a preview of the zombie in the browser.
Refer to [lesson 6](https://cryptoZombies.io/course) for more detailed information on how it can work in conjunction with a solidity dApp.

## Vue2 or Vue3

- Please for VUE2 checkout [zombie-char-component-vue2 package](https://www.npmjs.com/package/zombie-char-component-vue2)
- Please for VUE3 checkout [zombie-char-component package](https://www.npmjs.com/package/zombie-char-component)

## Installation

### npm

```bash
npm i zombie-char-component --save
```

### Usage

main.js

```javascript
//...
import ZombieChar from "zombie-char-component";
Vue.component("zombie-char", ZombieChar);
//...
```

Or in component

```html
<template>
  <div>
    <zombie-char></zombie-char>
  </div>
</template>

<script>
  import ZombieChar from "zombie-char-component";
  export default {
    data() {
      return {
        date: "",
      };
    },
    components: {
      zombieChar: ZombieChar,
    },
  };
</script>
```

### Description

## Props

| Name               | Type             | Default | Description                                            |
| ------------------ | ---------------- | ------- | ------------------------------------------------------ |
| isZombieLoaded     | Boolean          | false   |                                                        |
| optionalDna        | String           |         |                                                        |
| zombieName         | String           |         | generate a dna from name, if the optionalDna not exist |
| skinColorChoice    | [Number, String] | 1       | skin color 1 - 100 \*                                  |
| eyeColorChoice     | [Number, String] | 1       | eye color 1 - 100 \*                                   |
| clothesColorChoice | [Number, String] | 1       | clothes color 1 - 100 \*                               |
| headChoice         | [Number, String] | 1       | head 1 - 7 \*                                          |
| eyeChoice          | [Number, String] | 1       | eye 1 - 11 \*                                          |
| shirtChoice        | [Number, String] | 1       | shirt 1 - 6 \*                                         |
| autoGenerate       | Boolean          | false   |                                                        |
| catMode            | Boolean          | false   |                                                        |

\* if the autoGenerate equal to false

# optionalDna

012345678901<br />
aabbccddeeff<br />

- aa = head
- bb = eye
- cc = shirt
- dd = skinColor
- ee = eyeColor
- ff = clothesColor

### Examples

# Example1

```html
<template>
  <div>
    <zombie-char :isZombieLoaded="false" />
  </div>
</template>
```

![Example1](https://user-images.githubusercontent.com/48379992/136317466-0c743a60-f090-4504-b479-069b0a2a2941.png)

# Example2

```html
<template>
  <div>
    <zombie-char
      :isZombieLoaded="true"
      zombieName="Zombie1"
      :autoGenerate="false"
      :eyeChoice="5"
      :clothesColorChoice="50"
    />
  </div>
</template>
```

![Example2](https://user-images.githubusercontent.com/48379992/136316964-f0b77640-ee86-4527-af43-3c3ab1df3997.png)

# Example3

```html
<template>
  <div>
    <zombie-char
      :isZombieLoaded="true"
      optionalDna="020603010101"
      :autoGenerate="true"
    />
  </div>
</template>
```

![Example3](https://user-images.githubusercontent.com/48379992/136317256-ceacfd95-2dce-425e-a4b2-4726993d3d12.png)

# Example4

```html
<template>
  <div>
    <zombie-char
      :isZombieLoaded="true"
      optionalDna="020603010101"
      :autoGenerate="true"
      :catMode="true"
    />
  </div>
</template>
```

![Example4](https://user-images.githubusercontent.com/48379992/136317323-d2420122-2455-49a9-a6ef-fe3d38aacfae.png)

### Change log

## 1.0.6 (2021-10-25)

- added vue2 repo

## 1.0.5 (2021-10-07)

- fixed readme

## 1.0.4 (2021-10-07)

- fixed some bugs and added examples

<br />
<br />
<br />
<hr />

![footer](https://user-images.githubusercontent.com/48379992/136317416-fac417d0-ea87-433f-a9cf-f62b92c65c2a.png)

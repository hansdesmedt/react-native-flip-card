react-native-flip-card
===

> The card component which have motion of flip for React Native(iOS/Android)

[![NPM](https://nodei.co/npm/react-native-flip-card.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/react-native-flip-card/)

[![npm](https://img.shields.io/npm/v/react-native-flip-card.svg)]()[![npm](https://img.shields.io/npm/l/react-native-flip-card.svg)]()

[![js-standard-style](https://cdn.rawgit.com/feross/standard/master/badge.svg)](https://github.com/feross/standard) [![forthebadge](http://forthebadge.com/images/badges/uses-js.svg)](http://forthebadge.com)

Demo
---
![](./doc/ver3_android_demo.gif)


Installation
==

in Cli
---
```
npm i react-native-flip-card
```

in JavaScirpt
---
```
import FlipCard from 'react-native-flip-card'
```


Usage
===

Simple
---
```
<FlipCard>
  {/* Face Side */}
  <View style={styles.face}>
    <Text>The Face</Text>
  </View>
  {/* Back Side */}
  <View style={styles.back}>
    <Text>The Back</Text>
  </View>
</FlipCard>
```

Customized
---
```
<FlipCard 
  style={styles.card}
  friction={6}
  flipHorizontal={true}
  flipVertical={false}
  flip={false}
  clickable={true}
  onFlipped={(isFlipped)=>{console.log('isFlipped', isFlipped)}}
>
  {/* Face Side */}
  <View style={styles.face}>
    <Text>The Face</Text>
  </View>
  {/* Back Side */}
  <View style={styles.back}>
    <Text>The Back</Text>
  </View>
</FlipCard>
```

Props
===

flip(bool) `Default: false`
---
If you change default display side, you can set `true` to this param. If you change side, you can pass `bool` variable dynamically.

clicakble(bool) `Default: true`
---
If you want to disable click a card, you can set `false` to this param.

friction(number) `Default: 6`
---
The friction of card animation

flipHorizontal(bool) `Default: false`
---
If you set true, a card flip to horizontal.

![](./doc/ver2_horizontal.gif)


flipVertical(bool) `Default: true`
---
If you set false, a card not flip to vertical. If you set true both `flipHorizontal` and `flipVertical` , a card flip to diagonal.
![](./doc/ver2_vertical.gif)
![](./doc/ver2_diagonal.gif)


onFlipped(function) `(is_flipped) => {}`
---
When a card finish a flip animation, call `onFlipped` function with param.

alignHeight(boolean) `Default:false`
---
If you pass `true` to `alignHeight` param, the card keep height of bigger side.

alignWidth(boolean) `Default:false`
---
If you pass `true` to `alignWidth` param, the card keep width of bigger side.



Credits
===
Inspired by [react-flipcard](https://github.com/mzabriskie/react-flipcard)


License
===
MIT


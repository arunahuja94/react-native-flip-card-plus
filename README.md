react-native-flip-card
===

> The card component which has a motion of flip for React Native(Android) with gestures


Demo
---


Installation
==

in Cli
---
```
npm i react-native-flip-card-plus
```


Usage
===

Simple
---
```
import FlipCard from 'react-native-flip-card'

<FlipCard
        style={styles.card}
        flipHorizontal={false}
        flipVertical
        friction={10}
        perspective={2000}
        pressable={true}
        longPressable={true}
		    onPressed={() => alert('Pressed')}
        onLongPressed={() => alert('Long Pressed')}
        flip={this.state.flip}
        
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

pressable(bool) `Default: true`
---
If you want to disable click a card, you can set `false` to this param.

friction(number) `Default: 6`
---
The friction of card animation

perspective(number) `Default: 0`
---
The amount of perspective applied to the flip transformation

flipHorizontal(bool) `Default: false`
---
If you set true, a card flip to horizontal.



flipVertical(bool) `Default: true`
---
If you set false, a card not flip to vertical. If you set true both `flipHorizontal` and `flipVertical` , a card flip to diagonal.


onFlipStart(function) `(isFlipStart) => {}`
---
When a card starts a flip animation, call `onFlipEnd` function with param.

onFlipEnd(function) `(isFlipEnd) => {}`
---
When a card finishes a flip animation, call `onFlipEnd` function with param.

alignHeight(boolean) `Default:false`
---
If you pass `true` to `alignHeight` param, the card keep height of bigger side.

alignWidth(boolean) `Default:false`
---
If you pass `true` to `alignWidth` param, the card keep width of bigger side.

useNativeDriver(boolean) `Default:false`
---
If you pass `true` to `useNativeDriver` param, the card animation will utilize the native driver.

Credits
===
Inspired by [react-flipcard](https://github.com/mzabriskie/react-flipcard)


License
===
MIT


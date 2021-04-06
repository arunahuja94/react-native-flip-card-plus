#react-native-flip-card-plus

> The card component which has a motion of flip for React Native(Android) with gestures


## Installation

`npm i react-native-flip-card-plus`

# License
This is an updated version by [arunahuja94](https://github.com/arunahuja94). <br/>
Original author [moschan](https://github.com/moschan/react-native-flip-card),

## Usage

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

## Props


| Props              | Type       | Default                   | Description  |
| -------------------|:----------:| ------------------------- | ------------ |
| flip               | bool       | false                     | If you change default display side, you can set `true` to this param. If you change side, you can pass `bool` variable dynamically |
| pressable          | bool       | true                      | If you want to disable click a card, you can set `false` to this param. |
| friction           | Number     | 6                         | The friction of card animation |
| perspective        | Number     | 0                         | The amount of perspective applied to the flip transformation |
| flipHorizontal     | bool       | false                     | If you set true, a card flip to horizontal. |
| flipVertical       | bool       | true                      | If you set false, a card not flip to vertical. |
| alignHeight        | bool       | false                     | If you pass `true` to `alignHeight` param, the card keep height of bigger side. |
| alignWidth         | bool       | false                     | If you pass `true` to `alignWidth` param, the card keep width of bigger side. |
| useNativeDriver    | bool       | false                     | If you pass `true` to `useNativeDriver` param, the card animation will utilize the native driver. |
| onFlipStart        | function   | `(isFlipStart) => {}`     | When a card starts a flip animation, call `onFlipEnd` function with param. |
| onFlipEnd          | function   | `(isFlipEnd) => {}`       | When a card finishes a flip animation, call `onFlipEnd` function with param. |

 

## Credits

Inspired by [react-flipcard](https://github.com/mzabriskie/react-flipcard)



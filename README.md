# react-native-flip-card-plus

> The card component which has a motion of flip for React Native(Android/ios) with gestures


## Installation

`npm i react-native-flip-card-plus`

# License
This is an updated version by [arunahuja94](https://github.com/arunahuja94). <br/>
Original author [moschan](https://github.com/moschan/react-native-flip-card),

## Usage

```
"use strict";
import React, { Component } from "react";

import { View, TouchableOpacity, Text, StyleSheet } from "react-native";

import FlipCard from "react-native-flip-card-plus";
const BASE_SIZE = { width: 200, height: 200 };
export default class App extends Component {
  constructor(props) {
    super(props);
    this.state = {
      flip: false,
    };
  }
  render() {
    return (
      <View style={styles.container}>
        <View style={{ ...BASE_SIZE }}>
          <FlipCard
            style={styles.card}
            flipHorizontal={false}
            flipVertical
            friction={10}
            perspective={2000}
            pressable={true}
            pressableCustomFunc={true}
            onPressed={() => alert("Pressed")}
            longPressable={true}
            onLongPressed={() => alert("Long Pressed")}
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
        </View>

        <View>
          <TouchableOpacity
            style={styles.button}
            onPress={() => {
              this.setState({ flip: !this.state.flip });
            }}
          >
            <Text style={styles.buttonText}>Flip</Text>
          </TouchableOpacity>
        </View>
      </View>
    );
  }
}
const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: "center",
    alignItems: "center",
    backgroundColor: "#F5FCFF",
  },
  card: {
    ...BASE_SIZE,
    justifyContent: "center",
    alignItems: "center",
  },
  face: {
    flex: 1,
    backgroundColor: "red",
    justifyContent: "center",
    alignItems: "center",
    ...BASE_SIZE,
  },
  back: {
    flex: 1,
    backgroundColor: "#f1c40f",
    justifyContent: "center",
    alignItems: "center",
    ...BASE_SIZE,
  },
  button: {
    width: 100,
    height: 30,
    marginTop: 30,
    paddingTop: 6,
    paddingBottom: 6,
    borderRadius: 3,
    borderWidth: 1,
    backgroundColor: "#007AFF",
    borderColor: "transparent",
  },
  buttonText: {
    color: "#fff",
    textAlign: "center",
  },
});

```

## Props


| Props              | Type       | Default                   | Description  |
| -------------------|:----------:| ------------------------- | ------------ |
| flip               | bool       | false                     | If you change default display side, you can set `true` to this param. If you change side, you can pass `bool` variable dynamically |
| pressable          | bool       | true                      | If you want to disable card press, you can set `false` to this param. |
| swipeable          | bool       | true                      | If you want to disable gesture , you can set `false` to this param. |
| pressableCustomFunc | bool      | true                      | If you want to flip card on press, you can set `false` to this param. |
| longPressable      | bool       | true                      | If you want to disable long press a card, you can set `false` to this param. |
| friction           | Number     | 6                         | The friction of card animation |
| perspective        | Number     | 0                         | The amount of perspective applied to the flip transformation |
| flipHorizontal     | bool       | false                     | If you set true, a card flip to horizontal. |
| flipVertical       | bool       | true                      | If you set false, a card not flip to vertical. If you set true both flipHorizontal and flipVertical , a card flip to diagonal. |
| alignHeight        | bool       | false                     | If you pass `true` to `alignHeight` param, the card keep height of bigger side. |
| alignWidth         | bool       | false                     | If you pass `true` to `alignWidth` param, the card keep width of bigger side. |
| useNativeDriver    | bool       | false                     | If you pass `true` to `useNativeDriver` param, the card animation will utilize the native driver. |
| onFlipStart        | function   | `(isFlipStart) => {}`     | When a card starts a flip animation, call `onFlipEnd` function with param. |
| onFlipEnd          | function   | `(isFlipEnd) => {}`       | When a card finishes a flip animation, call `onFlipEnd` function with param. |
| onPressed          | function   | `{}`       | When `pressableCustomFunc` is true, you can add custom callback function for when the card is pressed. |
| onLongPressed      | function   | `{}`       | you can add custom callback function for when the card is long pressed. |

 

## Credits

Inspired by [react-flipcard](https://github.com/mzabriskie/react-flipcard)



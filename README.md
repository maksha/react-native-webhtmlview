# **react-native-webhtmlview**

A wrapper around React native WebView which renders HTML content with auto height.

## **Installation**

  `npm i react-native-webhtmlview --save`

## **Sample Usage**

```javascript
import React, { Component } from 'react'
import { View } from 'react-native'
import WebHtmlView from 'react-native-webhtmlview'

class Example extends Component {
  constructor(props) {
    super(props)
    this.state = {
      htmlContent: '<h1>Hello World</h1><p>HTML Content</p>'
    }
  }

  render() {
    return (
      <View style={{flex: 1, padding: 10}}>
        <WebHtmlView
          source={{html: this.state.htmlContent}}
          innerCSS="body { font-size: 93%; font-family: serif; text-align: justify }"
        />
      </View>
    )
  }
}

```

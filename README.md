# **react-native-webhtmlview**

A wrapper around React Native WebView which renders static HTML content in a WebView with auto height enabled and the ability to add CSS.

## **Installation**

Inside your React Native project, run the following command:

  `npm install react-native-webhtmlview --save`

## **Props**

- **`source.html`**: Inject the static html with a custom JavaScript and loads it in the WebView
- **`autoHeight`** (default: `true`): Adjust the height of the webview and turns off scrolling.
- **`innerCSS`**: The CSS style to apply to the html content.

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

module.exports = Example
```

# **react-native-webhtmlview**

A wrapper around React Native WebView which renders static HTML content in a WebView with auto height enabled and the ability to add CSS.

## **Installation**

Inside your React Native project, run the following command:

  `npm install react-native-webhtmlview --save`

## **Props**

- **`source.html`**: Inject the static html with a custom JavaScript and loads it in the WebView
- **`autoHeight`**: Adjust the height of the webview and turns off scrolling.
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

## **License**

```
MIT License

Copyright (c) 2016-2020 Muhammad Baja Aksha

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

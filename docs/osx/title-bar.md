# TitleBar

### Properties

Property            | Type         | Description
:------------------ | :-----------:| :----------
controls            | bool         | Sets the visibility of the controls of the title bar.
isFullscreen        | bool         | Sets the title bar state to fullscreen.
onCloseClick        | function     | Callback function of the close button.
onMaximizeClick     | function     | Callback function of the maximize button
onMinimizeClick     | function     | Callback function of the minimize button
onResizeClick       | function     | Callback function of the resize button
title               | string       | Sets the title of the title bar.

### Examples

```jsx
import React, { Component } from 'react';
import { View, TitleBar } from 'react-desktop/osx';

export default class extends Component {
  constructor() {
    super();
    this.state = { isFullscreen: false };
  }

  render() {
    return (
      <TitleBar
        title="untitled text 5"
        controls
        isFullscreen={this.state.isFullscreen}
        onCloseClick={() => console.log('Close window')}
        onMinimizeClick={() => console.log('Minimize window')}
        onMaximizeClick={() => console.log('Mazimize window')}
        onResizeClick={() => this.setState({ isFullscreen: !this.state.isFullscreen })}
      />
    );
  }
}
```

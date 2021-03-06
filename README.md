<h1 align="center">
    👟 React Scroll-To
</h1>

[![CircleCI](https://circleci.com/gh/ganderzz/react-scroll-to/tree/master.svg?style=svg)](https://circleci.com/gh/ganderzz/react-scroll-to/tree/master)
[![Coverage Status](https://coveralls.io/repos/github/ganderzz/react-scroll-to/badge.svg?branch=feature%2Fcreate-circi-artifact)](https://coveralls.io/github/ganderzz/react-scroll-to?branch=feature%2Fcreate-circi-artifact)
[![All Contributors](https://img.shields.io/badge/all_contributors-3-orange.svg?style=flat-square)](#contributors)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com) 


A React component that makes scrolling easy.

React Scroll-To provides a Higher Order Component, and Render Props implementation.

### Install

**npm:** `npm install react-scroll-to --save`

**yarn:** `yarn add react-scroll-to`


### API

**Render Props:**

```jsx
// Scroll to position (0, 500) in the browser window
import React, { Component } from "react";
import { ScrollTo } from "react-scroll-to";

export default class MyComponent extends Component {
    render() {
        return (
            <ScrollTo>
                {
                    (scroll) => (
                        <a onClick={() => scroll(0, 500)}>
                            Scroll to Bottom
                        </a>
                    )
                }
            </ScrollTo>
        );
    }
}
```

```jsx
// Scroll to position (0, 500) within a provided container
import React, { Component } from "react";
import { ScrollTo, ScrollArea } from "react-scroll-to";

export default class MyComponent extends Component {
    render() {
        return (
            <ScrollTo>
                {
                  (scroll) => (
                      <ScrollArea style={{ height: 1000 }}>
                        <button onClick={() => scroll(0, 500)}>
                          Scroll within this container
                        </button>
                      </ScrollArea>
                  )
                }
            </ScrollTo>
        );
    }
}
```

**Higher Order Component:**

```jsx
// Scroll to position (0, 500) within the browser window
import React from "react";
import { ScrollToHOC } from "react-scroll-to";

export default ScrollToHOC(function(props) {
    return (
        <a onClick={() => props.scroll(0, 500)}>
            Scroll to Bottom
        </a>
    );
})
```

```jsx
// Scroll to position (0, 500) within a provided container
import React from "react";
import { ScrollToHOC, ScrollArea } from "react-scroll-to";

export default ScrollToHOC(function(props) {
    return (
        <ScrollArea style={{ height: 1000 }}>
            <a onClick={() => props.scroll(0, 500)}>
                Scroll to Bottom
            </a>
        </ScrollArea>
    );
})
```

### Example
Check out this [example on CodeSandbox](https://codesandbox.io/s/yqlj0yjr41).

## Contributors

Thanks goes to these wonderful people ([emoji key](https://github.com/kentcdodds/all-contributors#emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
| [<img src="https://avatars3.githubusercontent.com/u/5566054?v=4" width="100px;"/><br /><sub><b>Dylan Paulus</b></sub>](http://www.dylanpaulus.com)<br />[💻](https://github.com/ganderzz/react-scroll-to/commits?author=ganderzz "Code") [📖](https://github.com/ganderzz/react-scroll-to/commits?author=ganderzz "Documentation") | [<img src="https://avatars1.githubusercontent.com/u/14035529?v=4" width="100px;"/><br /><sub><b>Anthony Ng</b></sub>](http://anthonyng.me)<br />[💻](https://github.com/ganderzz/react-scroll-to/commits?author=newyork-anthonyng "Code") [📖](https://github.com/ganderzz/react-scroll-to/commits?author=newyork-anthonyng "Documentation") | [<img src="https://avatars1.githubusercontent.com/u/17663679?v=4" width="100px;"/><br /><sub><b>UmenR</b></sub>](https://github.com/UmenR)<br />[💻](https://github.com/ganderzz/react-scroll-to/commits?author=UmenR "Code") |
| :---: | :---: | :---: |
<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/kentcdodds/all-contributors) specification. Contributions of any kind welcome!
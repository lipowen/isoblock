# Using ReactDOM.hydrate() For Isomorphic Gutenberg Blocks

> An Isomorphic Gutenberg Block uses the same React components for its "view" no matter where it is being displayed -- editor, front-end or a client decoupled from WordPress.
> > Me

This plugin is an example of a block that provides a form with one field. The block has a UI to set the defult value of the form. The form's HTML is saved to post content.

When a post with this block is loaded in the front-end, and the plugin is still active and JavaScript is enabled, then [`ReactDom.hydrate()`](https://reactjs.org/docs/react-dom.html#hydrate) is used to mount an app on the same DOM element. This allows the form to become interactive and have state manged by React, when possible. If the JavaScript isn't there, its just HTML.


## Notes
* State is managed in the editor by Gutenberg and in the front-end using Context API
    - [React Context TL;DR](https://codesandbox.io/s/react-context-tldr-bey3y)
* All dependencies are from [@wordpress](https://www.npmjs.com/org/wordpress)

## Development
* Clone
    - `git clone ... && cd ___`
* Install
    - `yarn`
* Start
    - `yarn start`
* Build For Production
    - `yarn build`

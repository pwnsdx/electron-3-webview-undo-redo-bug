# Electron 3 Webview Undo/Redo Issue

Calling `.undo()` or `.redo()` on a webview does not have any effect in Electron 3.

## Reproduction

Start this demo with Electron version 2.0.13 to see how things are supposed to work.

```
npm install
npm start
```

Put you cursor in the text input in child1.html. Type something and press Cmd+Z. The text revert to its previous state. Do Shift+Cmd+Z and the text you typed will reappear.

Change the Electron version in package.json to 3.0.9 then

```
npm install
npm start
```

Type something and press Cmd+Z. The text should revert but it does not.
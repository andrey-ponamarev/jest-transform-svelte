# Jest Transformer for Svelte
In order to unit test [Svelte](https://svelte.technology) components with the [Jest](https://jestjs.io) test framework, you need to use a transformer to ensure the Svelte component properly resolves its own component dependencies.

# Installation
```
$ npm install --save-dev jest-transform-svelte
```

# Usage
Simply add the component to the [Jest transform configuration](https://jestjs.io/docs/en/configuration#transform-object-string-string)

```
transform: {
	...
	'^.+\\.svelte$': 'jest-transform-svelte'
},
```

# Known issues

- The reported paths in the coverage summary may become lengthy
- The exclusing of modules may not work correctly, if this happens it may be because the `babel-plugin-istanbul` is active, which overrides your configuration (as it is a dependency to `babel-jest`), refer to the [related issue](https://jestjs.io/docs/en/troubleshooting#coveragepathignorepatterns-seems-to-not-have-any-effect)


# License

MIT License Copyright (c) 2018 Rogier Spieker

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
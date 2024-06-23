# ResqNetLoader

ResqNetLoader is a minimalist project demonstrating the use of the Request Network library. It includes practical examples to help developers quickly integrate Request Network functionalities into their applications, enabling secure and transparent financial transactions on the blockchain.

## Vision

ResqNetLoader aims to provide practical and easy-to-understand examples for using the Request Network library. By offering clear, working code samples, ResqNetLoader seeks to empower developers to integrate blockchain-based financial transactions into their projects seamlessly, promoting the adoption of decentralized finance technologies.

## Included Examples

### Node.js: `local.js`

This example demonstrates creating a request, paying it, and retrieving data from it on a local blockchain.

#### Usage:

```bash
node local.js
```

#### Setup:

You'll need the Request Network contracts on a local Ganache instance:

1. Clone the [Request Network repository](https://github.com/RequestNetwork/requestNetwork).
2. Navigate to the `requestNetwork.js` package:
    ```bash
    cd packages/requestNetwork.js
    ```
3. Run Ganache in a separate console:
    ```bash
    npm run ganache
    ```
4. Deploy the contracts using the provided script:
    ```bash
    npm run testdeploy
    ```

### Node.js: `rinkeby.js`

This example retrieves a request from the Rinkeby blockchain.

#### Usage:

```bash
node rinkeby.js
```

### Browser with Webpack

The library isn't shipped in a form ready to be used in a browser. Webpack is used here to build it for the browser. Run the example from an HTTP server (not using the `file:` protocol).

#### Setup for Browser Example:

1. Install Webpack:
    ```bash
    npm install --save-dev webpack webpack-cli
    ```
2. Create a `webpack.config.js` file:
    ```javascript
    const path = require('path');

    module.exports = {
        entry: './browser.js',
        output: {
            filename: 'bundle.js',
            path: path.resolve(__dirname, 'dist')
        },
        mode: 'development'
    };
    ```
3. Create `browser.js` with your browser code for Request Network.
4. Build the project:
    ```bash
    npx webpack
    ```
5. Serve the project using an HTTP server, such as `http-server`:
    ```bash
    npx http-server ./dist
    ```

## Resources

- [Request Network main repository](https://github.com/RequestNetwork/requestNetwork)
- [Join the Request Hub](https://request-slack.herokuapp.com/)
- [Documentation website](http://docs.request.network)

By offering these examples and resources, ResqNetLoader aims to support developers in building innovative solutions using the Request Network, fostering the growth of decentralized financial applications.
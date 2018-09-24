# Polymer-NFC

<!-- [![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/freudFlintstone/polymer-nfc) -->

Polymer 2 Web Component for NFC reading and writing using [WebNFC W3C Draft Standard](https://w3c.github.io/web-nfc/).
## Installation

```
bower install --save polymer-nfc
```
## Usage

Import it:
```
<link rel="import" href="../bower_components/polymer-nfc/polymer-nfc.html">
```

Use it:
```
    <polymer-nfc data="{{nfcData}}"></polymer-nfc>
```

You can also turn reading on and off in two ways:

 - Add a boolean __watch__ attribute and bind it to a local variable
```
    <polymer-nfc watch="{{flag}}" data="{{nfcData}}"></polymer-nfc>
```

 - Using javascript

```
    this.$.nfc.readOn();
    this.$.nfc.readOff();
```

You can also write data to a NFC Tag. For this to work, your data must be a valid json object. 
You'll need to explicitly turn writng on, and provide the data via the __data__ data binding:

```
    this.$.nfc.writeOn();
    var nfcData = {someId: 1, someValue: 'WebNFC rulez!'};
```

After a successful write, write mode is automatically turned off. If there's an error, the component keeps writing enabled, 
waiting for a new attempt.
## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## License

[MIT License](https://github.com/freudFlintstone/polymer-nfc/blob/master/LICENSE)

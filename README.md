# assign-obj-params

[![npm version](https://badge.fury.io/js/assign-obj-params.svg)](https://badge.fury.io/js/assign-obj-params)

## About

This is a function I've been using for a while in other bits of code (my library code, as well as some other code I've been doing for clients).

I did it to make things a bit more efficient.

## Installing

```bash
npm i assign-obj-params
```

or in a npm package

```bash
npm i assign-obj-params --save
```

## Where its used (Open Source)

* [nl-bxth](https://github.com/nolim1t/nl-bxth)
* [nl-bitmex](https://github.com/nolim1t/nl-bitmex)

## Examples

### Case - Designing an API interface to an API

I know all the API interface parameters, however I'd like to hide it away a bit more neatly in the library itself

```javascript
var requestinfo = {}; // This comes from the function or method

const assignFormParamsIfExist = require('assign-obj-params');
var formParams = {
    apikey: "apikey"
};

assignFormParamsIfExist(formParams, requestinfo, 'order_id');
assignFormParamsIfExist(formParams, requestinfo, 'pairing');

// After this formParams is built which can be used in the request.js library to send as an API request

```



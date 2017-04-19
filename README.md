defer
=====

A simple deferred object using native promises

Usage
-----

```
const db = require(...);
const defer = require('@coverslide/defer');

const deferred = defer();
const something = {};

async function getValue () {
  await deferred.promise;
  console.log(something.value);
}

async function loadValue () {
  const value = await db.get(query);
  something.value = value;
  deferred.resolve();
}

loadValue();
getValue();

```
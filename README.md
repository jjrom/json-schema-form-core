# json-schema-form-core
Core library for working with JSON-Schema with a UI-Schema (Form) definition that doesn't depend on a framework.

Work-In-Progress!

This library, through the use of its merge module, combines the schema and ui-schema
into a canonical schema for use by its services and external libraries.

## Testing it

There is a branch in angular-schema-form called `feature/webpack-babel` that integrates the core.
To use it roughly follow these steps:

* Get angular-schema-form and switch to branch `feature/webpack-babel`
* `npm install` to install dependencies, this will install json-schema-form-core as well
* `npm run build` to build with the core.
* Use dist/schema-form.js, now with core. *No need to also load ObjectPath since it is already included*

## Tests
Tests are written in mocha + chai and run trough `npm test`.

## Notes
* ObjectPath is bundled with json-schema-form-core
* angular-schema-form bundles json-schema-form-core so the user doesn't have to include it as an dependency.
* The code for not using ObjectPath on Angular 1.2 is removed. Could maybe be fixed but I (davidlgj) strongly believe its time to drop Angular 1.2 support since it complicates validation code as well.

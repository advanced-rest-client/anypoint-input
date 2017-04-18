[![Build Status](https://travis-ci.org/advanced-rest-client/anypoint-input.svg?branch=stage)](https://travis-ci.org/advanced-rest-client/anypoint-input)  

# anypoint-input

## anypoint-input

`<anypoint-input>` adds two-way binding and custom validators using `Anypoint.AnypointValidatorBehavior`
to `<input>`.

*Note: This is copy of the Polymer's `<iron-input>` but implementing `Anypoint.AnypointValidatableBehavior`
instead of `Polymer.IronValidatableBehavior`. All credits to the Polymer team.**

### Two-way binding

By default you can only get notified of changes to an `input`'s `value` due to user input:

```html
<input value="{{myValue::input}}">
```

`iron-input` adds the `bind-value` property that mirrors the `value` property, and can be used
for two-way data binding. `bind-value` will notify if it is changed either by user input or by script.

```html
<input is="anypoint-input" bind-value="{{myValue}}">
```

### Custom validators

You can use custom validators that implement `Anypoint.AnypointValidatorBehavior` with `<anypoint-input>`.

```html
<input is="anypoint-input" validator="my-custom-validator">
```

### Stopping invalid input

It may be desirable to only allow users to enter certain characters. You can use the
`prevent-invalid-input` and `allowed-pattern` attributes together to accomplish this. This feature
is separate from validation, and `allowed-pattern` does not affect how the input is validated.

```html
<input is="anypoint-input" prevent-invalid-input allowed-pattern="[0-9]">
```

### Example
```
<input is="anypoint-input"/>
```



### Events
| Name | Description | Params |
| --- | --- | --- |
| iron-input-validate | The `iron-input-validate` event is fired whenever `validate()` is called. | __none__ |

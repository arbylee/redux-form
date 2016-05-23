# Material UI Example

This is a simple demonstration of how to connect all the standard
[material-ui](https://github.com/callemall/material-ui) form elements to `redux-form`.

For the most part, it is a matter of wrapping each form control in a `<Field>`
component as custom component.

For controls like `SelectField` we need to simulate the `onChange` manually. As props
have been exposed in `redux-form` you can fire `onChange` manually.
Read more [here](../../../docs/api/Field.md#usage).

The delay between when you click "Submit" and when the alert dialog pops up is intentional,
to simulate server latency.

### Field Adapters

Notice that we define simple functions, like `renderTextField`, `renderCheckbox`, and 
`renderSelectField` to act as adapters between `redux-form` and the Material UI input 
components. You would only need to define these in one place in your application and reuse
them in each form.

### How to use async validation in form:

* Emails that will _fail_ validation: `foo@foo.com`, `bar@bar.com`.

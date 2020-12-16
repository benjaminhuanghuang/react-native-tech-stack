

## Formik (Form)

- Why: Without Formik, we need creat state for each of the field and validate those fields

- How Formik works
```
<Formik>
  {({handleChange, handleSubmit}) => (
    <Input onChangeText={handleChange("name")}>

    <Button onPress={handleSubmit>
  )}
</Formik>

```
```
function AppForm({ initialValues, onSubmit, validationSchema, children }) {
  return (
    <Formik
      initialValues={initialValues}
      onSubmit={onSubmit}
      validationSchema={validationSchema}
    >
      {() => <>{children}</>}
    </Formik>
  );
}
```


## Yup (Validation)


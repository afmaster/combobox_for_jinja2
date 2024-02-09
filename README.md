# combobox_for_jinja2
Jinja2 template for creating a personalized ComboBox (datalist), avoiding browser interference)

To import the component into your project, use this template:

```
    {% from "components/inputs/query_box.html" import query_box with context %}
    {{ query_box("field01", "Busca Paciente", form.patient_name, "Digite aqui", False, item_list, True) }}
```

Arguments of the macro:
- **unique_id**: used to avoid javascript malfunctions if the macro is imported more than once in the same <form>.
- **label**: the label of the form field.
- **form_field**: the component of WTForms wich will be rendered. It should be declared inside the form Class. It should be `StringField()`.
- **place_holder**: The content presented as place holder of the input.
- **autofocus**: It permit configure the input to be in focus after page load. Avoid put more than one macro as `autofocus=True`.
- **item_list**: The option list for selection.
- **editable**: Chose if users can type or not (just select options) into the field. The standard is `True`.


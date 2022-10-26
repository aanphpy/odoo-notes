# Force Save Readonly Field

Jika field readonly dan ingin mentrigger `onchange` di field tersebut, tambahkan attribut `force_save="1"` di view:

```xml
<field name="field_name" readonly="1" force_save="1"/>
```

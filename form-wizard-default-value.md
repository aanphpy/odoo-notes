# Set Form Wizard Default Value From Python

```python
@api.model
def default_get(self, fields):
    res = super(PresentationWizard, self).default_get(fields)
    crm_lead_id = self.env.context.get('active_id')
    crm_lead = self.env['crm.lead'].browse(crm_lead_id)
    if 'attachment_doc' in fields:
        res.update({'attachment_doc': crm_lead.file_prospect})
        return res
```

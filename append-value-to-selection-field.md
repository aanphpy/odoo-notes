# Append Value to Selection Field

```python
class ModelA(models.Model):
  _name = "model.a"
  
  alias_contact = fields.Selection([
      ('everyone', 'Everyone'),
      ('partners', 'Authenticated Partners'),
      ('followers', 'Followers only')], default='everyone',
      string='Alias Contact Security', required=True,
      help="Policy to post a message on the document using the mailgateway.\n"
           "- everyone: everyone can post\n"
           "- partners: only authenticated partners\n"
           "- followers: only followers of the related document or members of following channels\n")

  
class ModelB(models.Model):
    _inherit = "model.a"
    
    alias_contact = fields.Selection(selection_add=[('employees', 'Authenticated Employees')])
```

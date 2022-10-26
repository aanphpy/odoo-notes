# Get Timezones

```python
date_tz = fields.Selection('_tz_get', string='Timezone', required=True,
         	default=lambda self: self.env.user.tz or 'UTC')

@api.model
def _tz_get(self):
    return [(x, x) for x in pytz.all_timezones]
```

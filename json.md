### TypeError: datetime.datetime(2018, 1, 7, 16, 39, 27, 171000) is not JSON serializable
The problem could be fixed by the following code:
```python
from bson import json_util
# document is a mongo query result
print(json.dumps(document, default=json_util.default))
```

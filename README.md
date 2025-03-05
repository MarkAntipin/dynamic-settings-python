# Dynamic Settings Client

Dynamic Settings Client is a python client for [dynamic-settings](https://github.com/MarkAntipin/dynamic-settings) project,
allowing you to update your application’s settings on the fly without redeploying code.

## Installation
```
pip install dynamic-settings
```

## Usage
```
docker run -d -p 18100:18100 -v db_data:/app/db -e API_KEY=api-key markantipin12/dynamic-settings
```

```python
from dynamic_settings import DynamicSettings

settings = DynamicSettings(
    api_key='api-key',
    url='http://localhost:18100'
)


hello_message = settings.get('HELLO_MESSAGE', default='Hello, World!')
is_enabled = settings.get('IS_ENABLED', default=False)
```

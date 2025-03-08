# Dynamic Settings Client

Dynamic Settings Client is a python client for [dynamic-settings](https://github.com/MarkAntipin/dynamic-settings) project,
allowing you to update your application’s settings on the fly without redeploying code.

## 📦 Installation

Install the package via pip:
```
pip install dynamic-settings
```

## 🛠 Running the Dynamic Settings Server

To use the client, you need to have the Dynamic Settings server running. You can start the server using Docker:
```
docker run -d -p 18100:18100 -v db_data:/app/db -e API_KEY=api-key markantipin12/dynamic-settings
```

## 📖 Usage

```python
from dynamic_settings import DynamicSettings

settings = DynamicSettings(
    api_key='api-key',
    url='http://localhost:18100'
)


hello_message = settings.get('HELLO_MESSAGE', default='Hello, World!')
is_enabled = settings.get('IS_ENABLED', default=False)
```


## 🔗 Resources

- **[Tutorial](https://medium.com/@mr.antipin/effortless-configuration-making-your-fastapi-app-dynamic-d8652b0b4d56)**
- **[Dynamic Settings](https://github.com/MarkAntipin/dynamic-settings)**
- **[Docs](https://markantipin.github.io/dynamic-settings/)**
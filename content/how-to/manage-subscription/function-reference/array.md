# Array functions

## render_array

Create a new event attribute or event data path.

### definition

["render_array", path, value]

### Parameters

- `"render_array"` – The name of the function.
- `path` – The name of event attribute or event data path. If the key exist, an error will be reported. The param must be event json path.
- `value` – The value of event attribute or event data path. The param support all param types.

### Example

```json
{"command":["render_array","$.data.name1","$.data.name2"]}
```

## unfold_array

Create a new event attribute or event data path.

### definition

["unfold_array", path, value]

### Parameters

- `"unfold_array"` – The name of the function.
- `path` – The name of event attribute or event data path. If the key exist, an error will be reported. The param must be event json path.
- `value` – The value of event attribute or event data path. The param support all param types.

### Example

```json
{"command":["unfold_array","$.data.name1","$.data.name2"]}
```

# notion-api-note

## Query Example
```bash
NOTION_API_KEY=<your secert>
curl -X POST 'https://api.notion.com/v1/databases/<your db id>/query' \
  -H 'Authorization: Bearer '"$NOTION_API_KEY"'' \
  -H 'Notion-Version: 2022-02-22' \
  --data @body.json
```
### Filter Checkbox Property
sample `body.json`
```json
{
    "filter": {
        "property": "status",
        "checkbox": {
            "equals": true
        }
    }
}
```
### Filter Select Property
sample `body.json`
```json
{
    "filter": {
        "property": "status",
        "select": {
            "equals": "wait"
        }
    }
}
```

### Download File

```bash
curl '<s3-getObject-link>' --output test.mp4
```

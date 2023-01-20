```bash
jq --arg bar "$PWD" -r '.foo |= $bar' tmp/test.json
```

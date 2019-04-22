# Testing

```
val=$(pbpaste); idtoken=$(curl 'https://test.glycocode.com/api/login' | json '.id_token'); curl 'https://test.glycocode.com/api/data/latest/ebigxa_gxa_slim_E_MTAB2770' -X POST -H "Authorization: Bearer $idtoken" -H 'x-api-key: c836UTr1RTWn3qxGNm5QiuP7ogSlGNrp' --data "{\"accs\" : [$val], \"filter\": { \"location\" : \"mkn\" } }" -H 'Content-Type: application/json'
```
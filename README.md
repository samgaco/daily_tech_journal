# daily_tech_journal
Here I will keep track of the things I learn daily related to tech

# January

### 14 of January

| Tools/Concepts        | Are           | Reference  |
| ------------- |:-------------:| -----:|
| jq     | command-line JSON processor. | https://stedolan.github.io/jq/ |
| Restful Api's / Http apis    | Representational state transfer | https://www.andrewhavens.com/posts/20/beginners-guide-to-creating-a-rest-api |
| Long polling    | Instant changes pushed to clients | https://en.wikipedia.org/wiki/Push_technology#Long_polling |



## JQ

Use cases:

```
curl -X GET localhost:3000/api/timers | jq '.'
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   253  100   253    0     0   247k      0 --:--:-- --:--:-- --:--:--  247k
[
  {
    "title": "Mow the lawn",
    "project": "House Chores",
    "elapsed": 5498030,
    "id": "0a4a79cb-b06d-4cb1-883d-549a1e3b66d7",
    "runningSince": null
  }
]
```

```
curl -X GET localhost:3000/api/timers | jq '.[] | {id}'
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   253  100   253    0     0   247k      0 --:--:-- --:--:-- --:--:--  247k
{
  "id": "0a4a79cb-b06d-4cb1-883d-549a1e3b66d7"
}
```

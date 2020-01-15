### 14 of January

Worked connecting the client side with the server side and related, On my [GoTalk](https://github.com/samgaco/gotalk) application.


| Tools/Concepts        | Are           | Reference  |
| ------------- |:-------------:| -----:|
| jq     | command-line JSON processor. | [More Info](https://stedolan.github.io/jq/) |
| Restful Api's / Http apis    | Representational state transfer | [More Info](https://www.andrewhavens.com/posts/20/beginners-guide-to-creating-a-rest-api) |
| Long polling    | Instant changes pushed to clients | [More Info](https://en.wikipedia.org/wiki/Push_technology#Long_polling) |
| Passing props to links | How to pass data on react routes | [More Info](https://tylermcginnis.com/react-router-pass-props-to-link/) |
| verify_authenticity_token | Controller protection (RoR) | [More Info](https://api.rubyonrails.org/classes/ActionController/RequestForgeryProtection.html) |


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


## Passing props to links

Use cases:

```
<Link to={{
  pathname: '/myroute',
  state: {
    newData: true
  }
}}>My route</Link>
```

The object state will be accessible within the component linked with `/myroute` as `this.props.location.state` and pathname will be accesible with ` this.props.match.params`


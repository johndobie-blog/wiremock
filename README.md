# wiremock
A simple wiremock example of stubbing data locally


# Running the server
```
$ git cd src
$ java -cp "slf4j-nop-1.7.9.jar;wiremock-standalone-2.25.1.jar" com.github.tomakehurst.wiremock.standalone.WireMockServerRunner --port 9999 --verbose
$ curl http://localhost:9999/details
{
  "results": [
    {
      "gender": "male",
      "name": {
        "title": "Mr",
        "first": "Ismael",
        "last": "Roman"
      },
      "location": {
        "street": {
          "number": 457,
          "name": "Avenida de Andalucía"
        },
        "city": "Alcobendas",
        "state": "Comunidad de Madrid",
        "country": "Spain",
        "postcode": 86304
      },
      "email": "ismael.roman@example.com"
    },
    {
      "gender": "male",
      "name": {
        "title": "Mr",
        "first": "Francisco",
        "last": "Wheeler"
      },
      "location": {
        "street": {
          "number": 9067,
          "name": "Hickory Creek Dr"
        },
        "city": "Bozeman",
        "state": "Connecticut",
        "country": "United States",
        "postcode": 44479
      },
      "email": "francisco.wheeler@example.com"
    }
  ]
}
```
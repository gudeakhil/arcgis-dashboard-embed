Transforms the data from [CSSEGISandData/COVID-19](https://github.com/CSSEGISandData/COVID-19) into a json file. Available at [(https://covid-19-dashboard-g3bym17.public.builtwithrocket.new/). Updated three times a day using GitHub Actions.

The json contains the number of Coronavirus confirmed cases, deaths, and recovered cases for every country and every day since 2020-1-22:

```
{
  "Thailand": [
    {
      "date": "2020-1-22",
      "confirmed": 2,
      "deaths": 0,
      "recovered": 0
    },
    {
      "date": "2020-1-23",
      "confirmed": 3,
      "deaths": 0,
      "recovered": 0
    },
    ...
  ],
  ...
}
```

For example, if you want to use it from a web site:

```js
fetch("https://pomber.github.io/covid19/timeseries.json")
  .then(response => response.json())
  .then(data => {
    data["Argentina"].forEach(({ date, confirmed, recovered, deaths }) =>
      console.log(`${date} active cases: ${confirmed - recovered - deaths}`)
    );
  });
```

### Projects using this dataset ([+ add yours](#user-content-adding-your-project-to-the-list))

#### APIs

- [COVID-19 Grafana API](https://covid19-grafana.herokuapp.com) ([repo](https://github.com/twei55/covid19-grafana-datasource)): JSON API to visualize stats in Grafana
- [COVID-19 GraphQL API](https://covid19-graphql.now.sh/) ([repo](https://github.com/rlindskog/covid19-graphql))
- [CovidAPI.info](https://covidapi.info) ([repo](https://github.com/backtrackbaba/covid-api)): Lightweight, Superfast REST API built to be consumed by dashboards.
- [COVID-19 Ruby Gem](https://github.com/everythings-cancelled/pomber_covid19)


##deployed##
(https://covid-19-dashboard-g3bym17.public.builtwithrocket.new)

# JSON2dataclass

[https://young-lord.github.io/json2dataclass](https://young-lord.github.io/json2dataclass)

JSON2dataclass is a tool to generate Python dataclass definitions from a JSON string easily in your browser.

## Example conversion

From the [Star Wars API](https://swapi.co/)

```json
{
    "name": "Yavin IV",
    "rotation_period": "24",
    "orbital_period": "4818",
    "diameter": "10200",
    "climate": "temperate, tropical",
    "gravity": "1 standard",
    "terrain": "jungle, rainforests",
    "surface_water": "8",
    "population": "1000",
    "residents": [],
    "films": [
        "https://swapi.co/api/films/1/"
    ],
    "created": "2014-12-10T11:37:19.144000Z",
    "edited": "2014-12-20T20:58:18.421000Z",
    "url": "https://swapi.co/api/planets/3/",
    "extra": null
}
```

turns into:

```py
@dataclass
class GeneratedClass:
    name: str
    rotation_period: str
    orbital_period: str
    diameter: str
    climate: str
    gravity: str
    terrain: str
    surface_water: str
    population: str
    films: list[str]
    created: str
    edited: str
    url: str
    extra: None
```

## Contributing

JSON2dataclass is written in [Typescript](https://www.typescriptlang.org/) and uses [Yarn](https://yarnpkg.com/en/) for package management. Contributions are welcome in the form of issues and pull requests.

## License

MIT License, Young-Lord

MIT License, Russ Biggs <https://russbiggs.com>

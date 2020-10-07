# Aetion SRE Coding Challenge

[PokeAPI](https://pokeapi.co/) is an opensource project that indexes all pokemon that ever existed.


### Your Mission:
We need you to query this API and fetch the following data about each pokemon listed there:

| Name | Type | Stats |
|------|------|-------|
| `string` | `list` | `map` |

Here's an example of the json output that we want to you to do:
```
[
  {
      "name": "bulbasaur",
      "type": [
          "grass",
          "poison"
      ],
      "stats": {
          "hp": "45",
          "attack": "49",
          "defense": "49",
          "special-attack": "65",
          "special-defense": "65",
          "speed": "45"
    }
  },
  {
      "name": "ivysaur",
      "type": [
          "grass",
          "poison"
      ],
      "stats": {
          "hp": "60",
          "attack": "62",
          "defense": "63",
          "special-attack": "80",
          "special-defense": "80",
          "speed": "60"
    }
  },
  [...]
    {
      "name": "zarude",
      "type": [
          "dark",
          "grass"
      ],
      "stats": {
          "hp": "105",
          "attack": "120",
          "defense": "105",
          "special-attack": "70",
          "special-defense": "95",
          "speed": "105"
    }
  }
]
```

## Quick tips

You can get a list of all pokemons paginating through this API endpoint:
`https://pokeapi.co/api/v2/pokemon`

For example:
```
curl --silent "https://pokeapi.co/api/v2/pokemon?limit=100&offset=0"
curl --silent "https://pokeapi.co/api/v2/pokemon?limit=100&offset=200"
```

You can fetch more info about a Pokemon through this API endpoint:
`https://pokeapi.co/api/v2/pokemon/${pokemon_id}`

For example:
```
curl --silent https://pokeapi.co/api/v2/pokemon/${pokemon_id}
```

## References
PokeAPI Documentation:
https://pokeapi.co/docs/v2

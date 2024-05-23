# World currencies

## Contents

- [About](#about)
- [Usage](#usage)
- [Contributing](#contributing)
- [Sources](#sources)
- [License](#license)

## About

While trying to setup a module that required handling of currency codes, but had trouble finding a complete up-to-date list that was also easily downloadable without having to get an account or pay somewhere. So I decided to roll my own. For now its just 3 datapoints (name, code and symbol), but if there's a good use case for other fields they can always be added in the future.

## Usage 

Either clone this repo using

```bash
git clone https://github.com/antiftw/world-currencies.git 
```

or directly download the file (e.g. using wget):

```bash
wget https://github.com/antiftw/world-currencies/blob/main/currencies.json 
```



## Contributing

Since things will inadvertedly change  - likely without me noticing because it's regarding a currency I do not use on a daily basis - (or if I've made a mistake) feel free to create a PR and I will make sure to merge it asap.

## Sources

- [FOREX Live](https://www.foreignexchangelive.com/currency-codes-symbols) - for a  list of currency codes
- [This stale repo](https://github.com/mhs/world-currencies) - for some of the missing codes.
- [Wikipedia](https://wikipedia.org) -  as a way to verify codes and symbols as well as look up countries that match the codes.

## License

MIT. Feel free to use this wherever. See `LICENSE` for more details.
# World currencies

## Contents

- [About](#about)
- [Usage](#usage)
- [Contributing](#contributing)
- [Sources](#sources)
- [License](#license)

## About

While trying to setup a module that required handling of currency codes, but had trouble finding a complete up-to-date list that was also easily downloadable without having to get an account or pay somewhere. So I decided to roll my own. For now its just these datapoints:

- `currency-code` : the ISO-4217 Currency code
- `symbol`        : a symbolic (UTF-8) representation of the currency if I was able to find one, the ISO code again otherwise.
- `display-name`  : Can be used to display the currency in a dropdown.
- `short-name`    : Same but shorter.
- `name`          : The name only with letters and w/o spaces.
- `numeric-code`  : ISO-4217 Numeric code (usually the same to ISO 3166-1 numeric code for the corresponding country)
- `digits`        : Number of digits after the decimal separator 
  - I got this from (https://en.wikipedia.org/wiki/ISO_4217#cite_ref-MinorUnits_6-1)[this] Wiki. 
  - It has numbers and dots (`.`). The dot means something like 'not applicable'. I just treat them like 0, but I thought I'd retain the information
- `type`         : Because there are some 'not-a-currency currencies', a type to filter them:
   - `cur`: Actual currency traded on forex and used by country.
   - `xch`: Exchange Codes - used to trade (e.g. Silver/Gold/Platinum/Palladium).
   - `bmu`: Bond Market Unit - Used to trade on bond markets, in which participants issue debt.
   - `uoa`: Unit of Account - used for accounting between state members.
   - `moe`: Medium of Exchange - usually reserved for commercial exchanges.
   - `cpi`: Consumer Price Indicator - used to check price change in consumer prices.
   - `tst`: Special case `reserved for testing`.
   - `noc`: Special case `no currency`.
   - ... (think I got em all? :))


 but if there's a good use case for other fields they can always be added in the future.

## Usage 

Either clone this repo using:

```bash
git clone https://github.com/antiftw/world-currencies.git 
```

or directly download the file (e.g. using wget):

```bash
wget https://github.com/antiftw/world-currencies/blob/main/currencies.json 
```

## Contributing

Since things will inadvertedly change  - likely without me noticing because it's regarding a currency I do not use on a daily basis - feel free to create a PR and I will make sure to merge it asap.

Note: When creating PR with new data-fields, please provide data filled in for all countries.

## Sources

- [FOREX Live](https://www.foreignexchangelive.com/currency-codes-symbols) - for a  list of currency codes
- [This stale repo](https://github.com/mhs/world-currencies) - for some of the missing codes.
- [Wikipedia](https://wikipedia.org) -  as a way to verify codes and symbols as well as look up countries that match the codes.

## License

MIT. Feel free to use this wherever. See [`LICENSE`](https://github.com/antiftw/world-currencies/blob/main/LICENSE) for more details.
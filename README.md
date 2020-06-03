# gekko-strategies
This repo contains some trading strategies to run using [gekko](https://github.com/askmike/gekko) trading bot. These are pretty simple strategies I use to test some concept with gekko backtesting features.

## How to install
1. Copy the strategy `.js` file to the strategy directory located in your gekko bot installation folder generally named as follow: `./gekko/strategies`
2. Copy the strategy configuration `.toml` file to the configuration directory located in your gekko bot installation folder generally named as follow: `./gekko/config/strategies`
3. If you want to be able to run the strategy with gekko in CLI mode, you will need to add on the following source code to the `config.js` file you use to run gekko strategy from the command line.

```
config.tradingAdvisor = {
  enabled: true,
  method: 'MACross',
  candleSize: 60,
  historySize: 50,
}

config.SimpleRebound = {
  rsiTimePeriod: 14,
  upperLimit: 70,
  lowerLimit: 30,
  percentDump: -2,
  tpPercentRatio: 0.5,
  slRR: 1
}

config.MACross = {
  shortMATimePeriod: 5,
  longMATimePeriod: 50,
  trendPersist: 3,
  lmaTrendPersist: 3,
} 
```

## Disclaimer
Trading is a risky activity and trading cryptocurrencies, as cryptocurrencies are extremely volatile assets, is an even more risky activity. These strategies are shared with the community and are in no way a sure mean to provide you positive return. Use them at your own risk. I shall not be responsible for and disclaims all liability for any loss, liability, damage (whether direct, indirect or consequential), personal injury or expense of any nature whatsoever which may be suffered by you or any third party (including your company), as a result of or which may be attributable, directly or indirectly, to your access and use of these trading strategies.

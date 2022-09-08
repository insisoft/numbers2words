numbers2words
=============
This is a general-purpose library meant for number spelling for use in, e.g. legal documents and bills.

[![License](https://poser.pugx.org/jurchiks/numbers2words/license)](https://packagist.org/packages/jurchiks/numbers2words)
[![Downloads](https://poser.pugx.org/jurchiks/numbers2words/downloads)](https://packagist.org/packages/jurchiks/numbers2words)

Supported languages (ISO 639-1 language codes):
* English (`en`)
* Estonian (`et`)
* Latvian (`lv`)
* Lithuanian (`lt`)
* Russian (`ru`)
* Spanish (`es`)
* Italian (`it`)
* Polish (`pl`)

Supported currencies (ISO 4217 currency codes):
* British Pounds (`GBP`)
* Euro (`EUR`)
* Latvian Lats (`LVL`)
* Lithuanian Lits (`LTL`)
* Russian Roubles (`RUR`)
* U.S. Dollars (`USD`)
* Polish Zloty (`PLN`)
* Tanzanian Shillings (`TZS`)

#### Installation:

```
composer require insisoft/numbers2words
```

#### Usage:
```php
use js\tools\numbers2words\Speller;

Speller::spellNumber(123, Speller::LANGUAGE_RUSSIAN);
// output: сто двадцать три
Speller::spellCurrency(123, Speller::LANGUAGE_ENGLISH, Speller::CURRENCY_EURO, false);
// output: one hundred twenty three euro
Speller::spellCurrency(123, Speller::LANGUAGE_ENGLISH, Speller::CURRENCY_EURO);
// output: one hundred twenty three euro and 0 cents
Speller::spellCurrency(123.45, Speller::LANGUAGE_ENGLISH, Speller::CURRENCY_EURO, true, true);
// output: one hundred twenty three euro and forty five cents
Speller::spellCurrencyShort(123.45, Speller::LANGUAGE_ENGLISH, Speller::CURRENCY_EURO);
// output: one hundred twenty three EUR 45/100
```

#### Twig:
There is a Twig extension available for this library: [jurchiks/numbers2words_twig](https://github.com/jurchiks/numbers2words_twig)

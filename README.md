# Android developer tech excercise

## Instructions

Start by cloning/downloading this repo. Then open either `xml-versior` or `compose-versionx` project in Android Studio, depending on the technology you want to use.

## Functionality

The idea of this excercise is to develop a small currency converter application. This app will consist in one screen with 4 different screen states:

<img width="1221" alt="image" src="https://user-images.githubusercontent.com/13813905/202261187-d2fd894f-ddb6-4d26-aeea-1cda181c231a.png">

* Default: default state of the app. This state will be shown as soon as the app is run.
* Loading: after clicking the "Trade" button, an API request should be made to get exchange rate, and therefore, make the conversion.
* Success: if API request was successful, then we show the converted amount to the user.
* Error: if API request was not successful, we show an error to the user. You can use a toast, snackbar or a label.

### Where do we get the data from?

There's already a file called `Currencies.kt` under the `data` folder that contains the list of currency we can convert to, so that you don't need to worry about fetching them.

To get the exchange rate between Euros and the choosen currency, you will need to call this public endpoint: 
* https://cdn.jsdelivr.net/gh/fawazahmed0/currency-api@1/latest/currencies/{baseCurrency}/{toCurrency}.json

So, if our base currency is `eur` and we want to convert it to `usd`, the URL will be this:
* https://cdn.jsdelivr.net/gh/fawazahmed0/currency-api@1/latest/currencies/eur/usd.json

and this will be the response

```json
{
    "date": "2022-11-16",
    "usd": 1.034303
}
```


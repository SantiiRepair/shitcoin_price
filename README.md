## Package Info
This package uses the pool contract of each router & different cryptocurrency exchange platforms to take the price of any token even if it's not verified, it's free and without any kind of api key or registration required. 😎

<div style="display: flex; justify-content: center;">
  <img src="https://img.shields.io/pub/v/shitcoin_price?color=green">
  <img src="https://img.shields.io/pub/points/shitcoin_price">
  <img src="https://img.shields.io/pub/popularity/shitcoin_price?color=green">
  <img src="https://img.shields.io/badge/maintenance%20status-actively%20developed-brightgreen">
  <img src="https://img.shields.io/badge/coverage-100%25-orange">
</div>

## Features

Get the price in his token pair of any token on the Ethereum network and its subnets such as Binance Smart Chain, Polygon and others more.

## Getting Started

Add the package to your pubspec.yaml file as shown below.
```dart

dependencies:

  shitcoin_price: any

```

Then import the package into your code like this.
```dart

import 'package:shitcoin_price/shitcoin_price.dart';

```
## Usage

You can call the function and give it the parameters it wants to query, for example:


```dart
  String rpc = 'https://bsc-dataseed1.binance.org/';
  String router = '0x10ed43c718714eb63d5aa57b78b54704e256024e';
  String token0 = '0x0e09fabb73bd3ade0a17ecc321fd13a19e81ce82';
  String token1 = '0xe9e7cea3dedca5984780bafc599bd69add087d56';
  final httpClient = Client();
  final provider = Web3Client(rpc, httpClient);
  final priceDouble = await ShitCoinPrice().asDouble(provider, router, token0, token1);
  print(priceDouble); // 1.7973780251387401 CAKE
```

Or

```dart
String rpc = 'https://bsc-dataseed1.binance.org/';
String router = '0x10ed43c718714eb63d5aa57b78b54704e256024e';
String token0 = '0x0e09fabb73bd3ade0a17ecc321fd13a19e81ce82';
String token1 = '0xe9e7cea3dedca5984780bafc599bd69add087d56';
final httpClient = Client();
final provider = Web3Client(rpc, httpClient);
final priceBigInt = await ShitCoinPrice().asBigInt(provider, router, token0, token1);
print(priceBigInt); // 1797378025138740195 CAKE
```

In this example we import the package function and use it to get the price of a token, in this case CAKE and it returns a double or bigint number depending on how you handle the logic of the function.

- rpc: The rpc url on the network that we want to query.
- router: The address of the router, Uniswap, Pancakeswap, SushiSwap, or other.
- token0: The address of the contract of the token that we want to consult the price.
- token1: The address of the contract of the token pair that we want to consult.

NOTE: Check the test folder for an example implementation.

## Additional Information

- [Check for rpc url here 🚨](https://rpc.info)

This package will be updated and added more features and utilities related to free price queries and market capitalization data, feel free to contribute!

Greetings. ⚡

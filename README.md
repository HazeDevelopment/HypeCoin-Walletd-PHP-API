# HypeCoin-Walletd-API-PHP
HypeCoin Walletd API Wrapper in PHP


## Usage:

1. Create a Walletd Config File:

```
// .wallet File for walletd to use
container-file = walletd.wallet
// .wallet Password
container-password = YourWalletPassword
// Bind Port and Address
bind-port = 11169
bind-address = 0.0.0.0
```


2. Start Walletd with your Walletd Config

```
./walletd -c path/to/walletd.conf
```


3. Connect Front-End to Walletd-API

Find your coin's rpc port in the config file. ( i.e. rpc-bind-port = 11169 )

```vim
<?php
include 'HypeWalletdAPI.php';

// Create instance of HypeCoin Walletd
$hype = New HypeWalletd("http://127.0.0.1:11169");

// Get Addresses
$addr = $hype->getAddresses();

// Get Balance
$bal = $hype->getBalance();

?>
```

## NOTES:

- Still in testing Phase
- Some commands may need to be looked over
- Some commands have not been added yet

## DEVELOPMENT:
Edited for HazeDevelopment
Forked from https://github.com/KittyCatTech/forknote-api-php/blob/master/forknoteWalletdAPI.php

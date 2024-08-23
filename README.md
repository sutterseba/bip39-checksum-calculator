# BIP-39 checksum calculator

BIP-39 mnemonic phrases contain a checksum, appended to the raw entropy as part of the last word. This helps to identify mistakes when creating and restoring backups. Using this tool, you can quickly calculate which words would create a valid mnemonic or simply verify a given mnemonic is valid.

## Be careful

The implementation is very simple, may contain mistakes and was not designed with security in mind. It is meant for testing and learning purposes to offer a way to play around with mnemonic phrases. If you roll your own seed and want to complete your mnemonic phrase, there are hardware wallets allowing you to do just that in a more secure way. 

If you insist on using this tool for your own keys, make sure to run it offline on a secure and isolated operating system!

## Why does the amount of words differ?

The checksum length depends on the amount of words, e.g. for 12 words the checksum is 4 bit, while for 24 words the checksum is 8 bit. As a BIP-39 word is just an encoded 11 bit index, the checksum length determines how many bits of the final word can be chosen. 

For 12 words, the final word contains a 4 bit checksum, leaving 7 bit up for choice, resulting in 128 total options. For 24 words, the options come down to just eight, as the checksum now takes up the last 8 bit of the word.

This calcualtor is also availalbe [here](https://sutterseba.de/bip39-checksum-calculator).
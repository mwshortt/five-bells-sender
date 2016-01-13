# Five Bells Sender [![npm][npm-image]][npm-url] [![circle][circle-image]][circle-url] [![coveralls][coveralls-image]][coveralls-url]

[npm-image]: https://img.shields.io/npm/v/five-bells-sender.svg?style=flat
[npm-url]: https://npmjs.org/package/five-bells-sender
[circle-image]: https://circleci.com/gh/interledger/five-bells-sender.svg?style=shield
[circle-url]: https://circleci.com/gh/interledger/five-bells-sender
[coveralls-image]: https://coveralls.io/repos/interledger/five-bells-sender/badge.svg?branch=master
[coveralls-url]: https://coveralls.io/r/interledger/five-bells-sender?branch=master

> A reference implementation of an [Interledger](https://interledger.org) sending client

You can see the visualization in action as part of the [`five-bells-demo`](https://github.com/interledger/five-bells-demo)!

# Example: Universal Mode

    send({
      source_ledger:        'http://localhost:3001',
      source_username:      'alice',
      source_password:      'alice',
      destination_ledger:   'http://localhost:3002',
      destination_username: 'bob',
      destination_amount:   '1',
    }).then(function() {
      console.log('success')
    })

# Example: Atomic Mode

    send({
      source_ledger:        'http://localhost:3001',
      source_username:      'alice',
      source_password:      'alice',
      destination_ledger:   'http://localhost:3002',
      destination_username: 'bob',
      destination_amount:   '1',
      notary:               'http://localhost:6001',
      notary_public_key:    'QD/UBKyptEXcu6mZThsfnE/2ZZGsrpokKqaLMUrTUqo=',
      //receipt_condition:  {message_hash, signer, public_key, type},
    }).then(function() {
      console.log('success')
    })


```
gh api repos/cartridge-gg/sharding-operator/contents/install.sh -q .content | base64 -d | sh
```

```
sharding_operator deploy-sharding  --sharding-class-path ~/.local/bin/contract-classes/sharding_tests_sharding.contract_class.json
```

```
sharding_operator deploy-test-contract --sharding-address <CONTR ADDR> --game-class-path ~/.local/bin/contract-classes/sharding_tests_test_contract.contract_class.json
```

```
sharding_operator request-sharding --storage-slots-file config/storage_slots.json \
  --event-name GameFinished
```

```
sharding_operator send-transactions --socks-proxy "" --provider-url <URL>
```


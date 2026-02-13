```
gh api repos/cartridge-gg/sharding-operator/contents/install.sh -q .content | base64 -d | sh
```

```
sharding_operator deploy-sharding  --sharding-class-path contracts/sharding_tests_sharding.contract_class.json
```

Deploy test-contract
```
sharding_operator deploy-test-contract --contract-class-path contracts/sharding_tests_test_contract.contract_class.json
```

Deploy tournament
```
sharding_operator deploy-test-contract --contract-class-path contracts/sharding_tests_tournament.contract_class.json
```

With slots for test contract
```
sharding_operator request-sharding --shard-contract-address <CONTR_ADDR> --storage-slots-file config/storage_slots.json
```

With slots for tournament

```
sharding_operator request-sharding --shard-contract-address <CONTR_ADDR> --storage-slots-file /home/michal/Repos/sharding_template/config/tournament_storage_slots.json
```

Emit Finishing event for test contract
```
sharding_operator send-transactions
```

Emit Finishing event for tournament

```
sharding_operator simulate-game --rounds 2 # Specify how many rounds
```
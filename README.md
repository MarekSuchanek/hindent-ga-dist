# hindent builds for GitHub Actions

This repository is used to build and host [hindent](https://github.com/mihaimaruseac/hindent) for use within GitHub Actions

## Script for GitHub Actions

```sh
FILES=$(find myapp/src myapp/test myapp/app -name '*.hs')
RET=0
for FILE in $FILES; do
  if ! hindent --validate $FILE; then
    RET=1
  fi
done
exit $RET
```

## Contributing

Any forks and issues are highly appreciated.

## License

* This repository (GitHub workflow) is licensed under MIT [LICENSE](LICENSE)
* Distributed binaries stays under the original [LICENSE](HINDENT-LICENSE)

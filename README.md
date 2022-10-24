# Install Sphinx with Postgresql support

1. `brew update && brew install sphinx`
2. `brew edit sphinx`
3. change
```
  depends_on "mysql@5.7"
  depends_on "openssl@1.1"
```
to
```
  depends_on "mysql@5.7"
  depends_on "postgresql@14"
  depends_on "openssl@1.1"
```
and
```
  --without-pgsql
```
to
```
  --with-pgsql
```
4. `brew reinstall --build-from-source --verbose --debug sphinx`

# Kemal Github API

Mock Github API implemented with Kemal to be used as a benchmark suite.

Crystal Version: 0.27.1
Kemal Version: 0.25.1

Ruby Version: 2.5.3p101
Sinatra Version: v2.0.4
Puma: 3.12.0

## Install

Clone the repo

```
git clone https://github.com/sdogruyol/kemal-github-api
cd kemal-github-api
```

### Crystal


```
crystal build --release src/kemal-github-api.cr -o bin/kemal-github-api
./bin/kemal-github-api
```

### Ruby

```
gem install sinatra puma
ruby sinatra-github-api.rb -s Puma
```

## Benchmarks

*Kemal*

```
~ wrk -c 100 -d 40 http://localhost:3000/applications/123/tokens/123
Running 40s test @ http://localhost:3000/applications/123/tokens/123
  2 threads and 100 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency     2.18ms  716.18us  15.30ms   83.69%
    Req/Sec    23.17k     2.30k   27.74k    72.88%
  1844181 requests in 40.02s, 189.94MB read
Requests/sec:  46085.66
Transfer/sec:      4.75MB
```

*Sinatra*

```
➜  ~ wrk -c 100 -d 40 http://localhost:3000/applications/123/tokens/123
Running 40s test @ http://localhost:3000/applications/123/tokens/123
  2 threads and 100 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency     4.06ms    3.08ms  46.54ms   80.29%
    Req/Sec     1.98k   810.65     3.32k    58.12%
  157497 requests in 40.03s, 25.83MB read
Requests/sec:   3934.54
Transfer/sec:    660.88KB
```

## Contributing

1. Fork it ( https://github.com/sdogruyol/kemal-github-api/fork )
2. Create your feature branch (git checkout -b my-new-feature)
3. Commit your changes (git commit -am 'Add some feature')
4. Push to the branch (git push origin my-new-feature)
5. Create a new Pull Request

## Contributors

- [sdogruyol](https://github.com/sdogruyol) sdogruyol - creator, maintainer

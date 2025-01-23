# Kemal Github API

Mock Github API implemented with Kemal to be used as a benchmark suite.

##  What's used?

*Crystal: 1.15.0 Kemal: 1.16.0*

*Ruby Version: 3.4.0 Sinatra Version: 4.1.1 Puma: 6.5.0*

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
    Latency   451.14us  341.44us  24.29ms   97.61%
    Req/Sec    87.90k     7.82k  114.93k    92.26%
  7004695 requests in 40.10s, 0.95GB read
Requests/sec: 174671.67
Transfer/sec:     24.15MB
```

*Sinatra*

```
➜  ~ wrk -c 100 -d 40 http://localhost:3000/applications/123/tokens/123
Running 40s test @ http://localhost:3000/applications/123/tokens/123
  2 threads and 100 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency    46.74ms   55.56ms 231.71ms   78.35%
    Req/Sec     3.02k   263.67     3.58k    73.75%
  240641 requests in 40.01s, 39.91MB read
Requests/sec:   6014.40
Transfer/sec:      1.00MB
```

## Contributing

1. Fork it ( https://github.com/sdogruyol/kemal-github-api/fork )
2. Create your feature branch (git checkout -b my-new-feature)
3. Commit your changes (git commit -am 'Add some feature')
4. Push to the branch (git push origin my-new-feature)
5. Create a new Pull Request

## Contributors

- [sdogruyol](https://github.com/sdogruyol) sdogruyol - creator, maintainer

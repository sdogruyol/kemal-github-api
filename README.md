# Kemal Github API

Mock Github API implemented with Kemal.

## Installation

```
git clone https://github.com/sdogruyol/kemal-github-api
cd kemal-github-api
crystal build --release src/kemal-github-api.cr -o bin/kemal-github-api
./bin/kemal-github-api
```

## Benchmarks

Kemal

```
~ wrk -c 100 -d 40 http://localhost:3000/applications/123/tokens/123
Running 40s test @ http://localhost:3000/applications/123/tokens/123
  2 threads and 100 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency     3.77ms  371.76us  11.22ms   77.99%
    Req/Sec    13.31k     1.01k   14.70k    51.88%
  1060074 requests in 40.01s, 109.18MB read
Requests/sec:  26494.53
Transfer/sec:      2.73MB
```

Sinatra

```
➜  ~ wrk -c 100 -d 40 http://localhost:3000/applications/123/tokens/123
Running 40s test @ http://localhost:3000/applications/123/tokens/123
  2 threads and 100 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency     6.38ms    5.12ms  84.48ms   78.61%
    Req/Sec     1.26k   514.25     2.07k    58.25%
  100189 requests in 40.03s, 16.43MB read
Requests/sec:   2502.72
Transfer/sec:    420.38KB
```

## Contributing

1. Fork it ( https://github.com/sdogruyol/kemal-github-api/fork )
2. Create your feature branch (git checkout -b my-new-feature)
3. Commit your changes (git commit -am 'Add some feature')
4. Push to the branch (git push origin my-new-feature)
5. Create a new Pull Request

## Contributors

- [sdogruyol](https://github.com/sdogruyol) sdogruyol - creator, maintainer

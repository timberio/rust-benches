rust-benches
============

This repo contains standalone benches using criterion for various Rust
components to understand their performance profiles. So far this is just
channels.

They can be run via:

```
$ cargo bench
```

Results on OSX with 2.3 GHz Quad-Core Intel Core i7.

```
group                                          base
-----                                          ----
channels/data_size/async-std 1.9/100000x1      1.00     28.4±1.53ns 3274.1 GElem/sec
channels/data_size/async-std 1.9/100000x10     1.00     28.9±2.03ns 32190.7 GElem/sec
channels/data_size/async-std 1.9/100000x100    1.00    30.8±11.97ns 302132.2 GElem/sec
channels/data_size/async-std 1.9/1000x1        1.00     22.4±3.24ns 41.5 GElem/sec
channels/data_size/async-std 1.9/1000x10       1.00     21.6±2.68ns 430.9 GElem/sec
channels/data_size/async-std 1.9/1000x100      1.00     21.2±3.87ns 4395.5 GElem/sec
channels/data_size/futures 0.3/100000x1        1.00    31.9±17.70ns 2922.9 GElem/sec
channels/data_size/futures 0.3/100000x10       1.00     30.2±1.44ns 30876.5 GElem/sec
channels/data_size/futures 0.3/100000x100      1.00     30.1±2.82ns 309821.2 GElem/sec
channels/data_size/futures 0.3/1000x1          1.00     24.4±3.21ns 38.2 GElem/sec
channels/data_size/futures 0.3/1000x10         1.00     23.9±4.78ns 389.5 GElem/sec
channels/data_size/futures 0.3/1000x100        1.00    24.7±10.32ns 3768.6 GElem/sec
channels/data_size/tokio 0.2/100000x1          1.00     19.1±1.70ms  5.0 MElem/sec
channels/data_size/tokio 0.2/100000x10         1.00     21.3±2.66ms 44.7 MElem/sec
channels/data_size/tokio 0.2/100000x100        1.00     46.7±2.68ms 204.2 MElem/sec
channels/data_size/tokio 0.2/1000x1            1.00   175.1±19.64µs  5.4 MElem/sec
channels/data_size/tokio 0.2/1000x10           1.00   177.8±23.76µs 53.6 MElem/sec
channels/data_size/tokio 0.2/1000x100          1.00   181.8±26.66µs 524.5 MElem/sec
channels/data_size/tokio 1.1/100000x1          1.00     22.5±2.59ms  4.2 MElem/sec
channels/data_size/tokio 1.1/100000x10         1.00     23.6±1.65ms 40.5 MElem/sec
channels/data_size/tokio 1.1/100000x100        1.00     48.4±2.39ms 197.1 MElem/sec
channels/data_size/tokio 1.1/1000x1            1.00   196.5±21.58µs  4.9 MElem/sec
channels/data_size/tokio 1.1/1000x10           1.00   214.9±33.27µs 44.4 MElem/sec
channels/data_size/tokio 1.1/1000x100          1.00   214.1±23.91µs 445.4 MElem/sec
```

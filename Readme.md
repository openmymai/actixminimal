# Minimal Actix

Minimum Rust code in Actix that can run Web Server to serve static files.

### Run web server

Assume that you have installed Rust on your computer.<br>
Clone the repo, get into the directory and run it.
```
git clone https://github.com/openmymai/actixminimal.git
cd actixminimal
cargo run
``` 
Browse to http://localhost:8000
Then you can see that it serve index.html from public folder.

This test run on the same machine, actix use CPU less than 10%
Update to Rust 1.65.0, more robust.

### Siege Test on Apple M1 MackBook Pro Ram 8G
```
% siege http://localhost:8000
siege aborted due to excessive socket failure; you
can change the failure threshold in $HOME/.siegerc

Transactions:		        6279 hits
Availability:		       95.21 %
Elapsed time:		       45.79 secs
Data transferred:	       71.81 MB
Response time:		        0.28 secs
Transaction rate:	      137.13 trans/sec
Throughput:		        1.57 MB/sec
Concurrency:		       38.55
Successful transactions:        6279
Failed transactions:	         316
Longest transaction:	        3.21
Shortest transaction:	        0.00
```

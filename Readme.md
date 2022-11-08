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
### Siege Test on Apple M1 MackBook Pro Ram 8G, upgrade to Macos Ventura 13.0
Actix use CPU less than 10%
Update to Rust 1.65.0, more robust.
#### This test has to break because of longer run.
```
Lifting the server siege...
Transactions:		      154862 hits
Availability:		       99.91 %
Elapsed time:		      499.55 secs
Data transferred:	     1472.58 MB
Response time:		        0.12 secs
Transaction rate:	      310.00 trans/sec
Throughput:		        2.95 MB/sec
Concurrency:		       37.13
Successful transactions:      154864
Failed transactions:	         137
Longest transaction:	       19.17
Shortest transaction:	        0.00
 
```

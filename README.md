# forking-ELK

This is quick and dirty setup of ELK using Docker. I put this together for testing and sandboxing purposes, such as forking logs in Logstash to ELK and Observe. 

## Setup 
1. Clone this repo
2. If you'd like to send logs to Observe then add your credentials in `logstash.conf`, otherwise comment lines 22-29.
3. run `docker-compose up --build` from this directory

## Usage

1. Run

`curl -X POST "http://localhost:5044" -H 'Content-Type: application/json' -d '{"message": "127.0.0.1 - - [21/Jun/2024:14:32:05 +0000] \"GET / HTTP/1.1\" 200 612 \"-\" \"Mozilla/5.0 (compatible; Googlebot/2.1; +http://www.google.com/bot.html)\""}'`

2. Check for logs in [localhost:5601](http://localhost:5601/)
3. Profit
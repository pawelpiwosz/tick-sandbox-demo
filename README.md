### Continuous Monitoring and introduction to TICK stack

This repository contains exercises and links I perform during 
the talk about Continuous Monitoring, MEAL and TICK stack as a 
example of my idea of future monitoring.

### Why TICK stack?

The nswer is short. Time series database. What can be better for 
metrics and logs? 

### Other advantages on TICK

__Lightweight__. Written in Golang, doesn't need that much of 
resources. no comparision  to ELK, sorry :)

__Easy to config__. To start playing with TICK stack, 5 minutes is needed. Not more.  
Of course, proper , secure config will take time, but this is obvious.

__Complex__. All elements of the TICK stack combined are building great tool for monitoring.

__Telegraf and InfluxDB are well known already__. Those two elements of TICK stack are known on the market. Telegraf is well recognized shipper, considered and used in many solutions, and InfluxDB is very popular DB for monitoring solutions. As backend for Grafana, Promoetheus and others.
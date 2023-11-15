# Example of an effective dnf.conf 
Have you ever used dnf and felt it works slowly?
This is Just a simple and effective config file for dnf that sets a minimum speed rate for downloading from the chosen server.
## Explaination
`max_parallel_downloads=[decimal]` sets the number of package downloads you want to have at the same time; if you have a slow internet connection like me, I recommend you to put it between 2 to 5.

`timeout=[seconds]` sets the time that dnf tries to download from the server; if this time exceeds and download rate is less than `minrate`, dnf changes mirror automatically.

`minrate=[decimal]k` sets the minimum speed that is accepted for downloading server, if downloading speed from the server is less than this value, dnf changes mirror automatically after the `timeout`

`fastestmirror` option does'nt really help that much, since it uses ping speed for the best server, and that has little to do with bandwidth and download speed; so I did not include that. 


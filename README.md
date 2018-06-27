# IIS-Activity-Blinker
IIS activity indicator that uses physical hardware, software, or both to display the level of activity your mission-critical IIS server is encountering.  

Displays critical flashing red light if site is unresponsive/down, or it will show a blinking indicator whenever someone performs a web request against your server:
-green single blink represents a single IP address performing a web request (healthy usage)
-color gradient upwards to show more users and heavier load
    -blue is a step up from green, yellow a step up from blue, orange from yellow, and red from orange

Will include a number of performance metrics to show if performance is degrading/degraded
-script will take a baseline performance check of all links/endpoints from your application pool
    -if a request takes more than 3 times as long as it should, and there are not many users connected, a custom color will be displayed
    -if cpu, memory, requests per second, or any other custom metric goes above a threshold, a custom color will be displayed
    
The goal is to provide server administrators with a convenient representation of server health, to prompt further investigation when necessary.

# CN-Switch-Log-Sniffer
A shell script to sniff local (gateway switch's) logs and save them locally using ssh

Switch logs are accessible in three ways -
1. ssh or telnet to switch server / login to http port 80 and download logs( tar.gz file)
2. connect directly to switch over a COM port
3. maintain a syslog server from which logs can be fetched

so, we use a remote desktop connection SSH to login to our CORE SWITCH 

show log is used to show the console logs at the default informational level, the levels can be set according to our requirements( debugging, informational etc.)

the logs show the recently connected hosts, system up time, system failures, reboots etc. failed/successful login attempts and the respected username
it also shows the client's IP, last login time

we use the 'script' command to save the file into a specified filename into our disk

terminal length 0 - used to show full length of terminal output

USAGE EXAMPLE - 

goto the directory where the file (switch_log_sniffer.sh) is,
type './switch_log_sniffer.sh' into a bash shell and the command line argument are optional (

	1. "specify custom username for ssh login in 1st commandline-argument \nor by default 'admin' will be used for cisco routers"
	2. "specify custom switch ip address for ssh login in 2nd commandline-argument \nor by default system's default gateway will be used"
	3. "default password is 'cisco'" )

after the command successfully executes, a file 'switch.log' is created in the current user's directory containing the switch logs
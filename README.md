Install instructions for linux:

	1.	Copy all of the files located in the Files folder to the Bin directory.
	2.	Edit the file notifynest.sh
	3.	Substitute your information on line number 7 ($BIN/nest.py --user YOURNESTACCOUNTUSERNAMEHERE --password YOURNESTACCOUNTPASSWORDHERE away $1) and save the file.
	4.	Edit the file autoaway.sh
	5.	Substitute your information on line number 10  ($BIN/autoaway.py --devices DEVICEIPSHERE --offpeakstart 23:00 --offpeakend 06:30 --grace 1 --check-every 1 --notify $BIN/notifynest.sh --verbose) and save the file.
	6.	To manually execute the program run ./autoaway.sh

To set up auto startup and running in the background:

	1.	Install Screen if its not already installed
	2.	Edit the file /etc/rc.local
	3.	Add the line (su - ACCOUNTUSERNAME -c "screen -dmS test bash -c '/bin/autoaway.sh; exec bash’”) replacing ACCOUNTUSERNAME
	4.	Reboot the computer
	5.	To see if the script has started run the command ’screen -list’ then ‘screen -r’

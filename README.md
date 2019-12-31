# Chantel UAV
## Build, test, run
./run.py # need sudo to access i2c on rpi

## Dependencies
### SimpleWebSocketServer
sudo pip install git+https://github.com/dpallot/simple-websocket-server.git

## Crontab
### sudo crontab -e:
```
* * * * * cd /home/pi/git/chantel && ./run.sh > /home/pi/chantel-run.log 2>&1
@reboot root cd /home/pi/git/chantel && ./run.sh > /home/pi/chantel-run.log 2>&1
```

### crontab -e:
```
*/5 * * * * cd /home/pi/git/chantel && /usr/bin/git pull origin master > /home/pi/git.log 2>&1
```
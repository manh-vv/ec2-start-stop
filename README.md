# ec2 start stop

Start and Stop AWS EC2 Instances from another always active Instance

Use it for server development / test / stage that should not always be running.

1. Install [aws-cli](https://aws.amazon.com/it/cli/) into another EC2 instance that is always running 24 hours on 24, write a script like this [ec2cmd.sh](./ec2cmd.sh) provided.
2. Put the script into cron (crontab -e) on this instance always active, for example using the [cron.txt](./cron.txt) provided.

## NOTE

Check the current timezone

```sh
timedatectl

#                Local time: Mon 2023-07-03 09:42:16 +07
#            Universal time: Mon 2023-07-03 02:42:16 UTC
#                  RTC time: Mon 2023-07-03 02:42:16    
#                 Time zone: Asia/Bangkok (+07, +0700)  
# System clock synchronized: yes                        
#               NTP service: active                     
#           RTC in local TZ: no 
```

Change the current timezone if necessary

```sh
sudo timedatectl set-timezone Asia/Bangkok
```

**ATTENTION**: always make a backup and test first using it!

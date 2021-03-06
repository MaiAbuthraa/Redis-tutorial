# Redis-tutorial
The main points to start learning

### 1- Install Resdis:

#### On Mac-OS:
> brew install redis

Uninstall: 
> brew uninstall redis
> rm ~/Library/LaunchAgents/homebrew.mxcl.redis.plist

Launch Redis on computer starts
> ln -sfv /usr/local/opt/redis/*.plist ~/Library/LaunchAgents

Start Redis server via “launchctl”
> launchctl load ~/Library/LaunchAgents/homebrew.mxcl.redis.plist

Location of Redis configuration file.
> /usr/local/etc/redis.conf

Also you can use brew service:

Start Redis server:
> brew services start redis

Stop Redis server:
> brew services stop redis

Restart Redis server:
> brew services restart redis

Shutdown
> redis-cli shutdown

#### On Ubuntu
To install Redis on Ubuntu, it’s a lot of works to do, check this link
[Install Redis on Ubuntu](https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-redis-on-ubuntu-16-04)


To start Redis automatically when your server boots:
> sudo systemctl start redis

To restart Redis server:
> sudo systemctl enable redis

To restart Redis server:
> sudo systemctl restart redis

To stop Redis server:
> sudo systemctl stop redis

OR:

> /etc/init.d/redis-server start
> /etc/init.d/redis-server restart
> /etc/init.d/redis-server stop

On modern Ubuntu:
> sudo service redis-server start|run redis  
> sudo service redis-server restart 
> sudo service redis-server stop 

list all `redis-server` process 
> ps aux | grep redis-server

#### 2- CLI
Test if Redis server is running.
> redis-cli ping
// Pong

> redis-cli

Print message
> ECHO "wirte your message"

Set variable
> SET foo 100 // OK

Get variable
> GET foo 100 // "100"

Increment number:
> INCR foo // (integer) 101

Decrement number:
> DECR foo // (integer) 100

Check existing:
> EXISTS foo // 1 if yes, 0 if no

Delete the variable
> DEL foo
then if you call get
> GET foo 100 // (nil)
> EXISTS foo //  0 

Delete all the variables
> FLUSHALL




Side Note, for me
Ubuntu:
```

cd /lib/systemd/system
I will find redis-server.service

```


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



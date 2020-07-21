°²×°RabbitMQ

1.ErlangÓïÑÔ 64Î» https://www.erlang.org/downloads

2.RabbitMQ·şÎñ¶Ë°²×° http://www.rabbitmq.com/

3.Ê¹ÓÃRabbitMQÒÔwindowsServiceµÄ·½Ê½ÔÚºóÌ¨ÔËĞĞ£¬´ò¿ªcmd£¬ÇĞ»»µ½sbinÄ¿Â¼ÏÂÖ´ĞĞ
 rabbitmq-service install
 rabbitmq-service enable 
 rabbirmq-service start

4.²é¿´·şÎñ¶ËµÄ×´Ì¬ rabbitmqctl½Å±¾¡¢
 rabbitmqctl status 

*¼ÙÈçÏÔÊ¾nodeÃ»ÓĞÁ¬½ÓÉÏ£¬ĞèÒªµ½C:\WindowsÄ¿Â¼ÏÂ£¬½«.erlang.cookieÎÄ¼ş£¬¿½±´µ½ÓÃ»§Ä¿Â¼ÏÂ C:\Users\{ÓÃ»§Ãû}£¬ÕâÊÇErlangµÄCookieÎÄ¼ş£¬ÔÊĞíÓëErlang½øĞĞ½»»¥¡£

5.Ê¹ÓÃÃüÁî²é¿´ÓÃ»§
rabbitmqctl list_users

*RabbitMQ»áÎªÎÒÃÇ´´½¨Ä¬ÈÏµÄÓÃ»§ÃûguestºÍÃÜÂëguest£¬guestÄ¬ÈÏÓµÓĞRabbitMQµÄËùÓĞÈ¨ÏŞ¡£

¡¡¡¡Ò»°ãµÄ£¬ÎÒÃÇĞèÒªĞÂ½¨Ò»¸öÎÒÃÇ×Ô¼ºµÄÓÃ»§£¬ÉèÖÃÃÜÂë£¬²¢ÊÚÓèÈ¨ÏŞ£¬²¢½«ÆäÉèÖÃÎª¹ÜÀíÔ±£¬¿ÉÒÔÊ¹ÓÃÏÂÃæµÄÃüÁîÀ´Ö´ĞĞÕâÒ»²Ù×÷£º
	1.rabbitmqctl add_user JC jayChou  ´´½¨ÓÃ»§JC ¸³ÓèÃÜÂëjayChou
	
	2.rabbitmqctl set_premissions JC ".*" ".*" ".*" //¸³ÓèJC¶ÁĞ´ËùÓĞÏûÏ¢¶ÓÁĞµÄÈ¨ÏŞ

	3.rabbitmqCtl set_user_tags JC adminstractor //·ÖÅäÓÃ»§×é

	4.rabbitmqctl change_password JC 123  //¸Ä±äÓÃ»§JCµÄÃÜÂëÎª123
	
	5.rabbitmqctl delete_user JC É¾³ıÓÃ»§
	
       Ò²¿ÉÒÔ¿ªÆôrabbitmqctl_management²å¼ş ÔÚweb½çÃæ²é¿´ºÍ¹ÜÀíRabbitMQ·şÎñ

	rabbitm-plugins enable rabbitmq_management
	
Erlang 23.0
RabbitMQ 3.8.5


rabbitmqctl status  ×´Ì¬ÏÔÊ¾


Status of node rabbit@DESKTOP-2AB32DI ...
[1mRuntime[0m

OS PID: 12336
OS: Windows
Uptime (seconds): 215
RabbitMQ version: 3.8.5
Node name: rabbit@DESKTOP-2AB32DI
Erlang configuration: Erlang/OTP 23 [erts-11.0] [64-bit] [smp:4:4] [ds:4:4:10] [async-threads:64]
Erlang processes: 298 used, 1048576 limit
Scheduler run queue: 1
Cluster heartbeat timeout (net_ticktime): 60

[1mPlugins[0m

Enabled plugin file: c:/Users/ML/AppData/Roaming/RabbitMQ/enabled_plugins
Enabled plugins:


[1mData directory[0m

Node data directory: c:/Users/ML/AppData/Roaming/RabbitMQ/db/rabbit@DESKTOP-2AB32DI-mnesia
Raft data directory: c:/Users/ML/AppData/Roaming/RabbitMQ/db/rabbit@DESKTOP-2AB32DI-mnesia/quorum/rabbit@DESKTOP-2AB32DI

[1mConfig files[0m

 * c:/Users/ML/AppData/Roaming/RabbitMQ/advanced.config

[1mLog file(s)[0m

 * c:/Users/ML/AppData/Roaming/RabbitMQ/log/rabbit@DESKTOP-2AB32DI.log
 * c:/Users/ML/AppData/Roaming/RabbitMQ/log/rabbit@DESKTOP-2AB32DI_upgrade.log

[1mAlarms[0m

(none)

[1mMemory[0m

Calculation strategy: rss
Memory high watermark setting: 0.4 of available memory, computed to: 6.8156 gb
other_proc: 0.0368 gb (32.88 %)
code: 0.0289 gb (25.87 %)
allocated_unused: 0.0157 gb (14.03 %)
other_system: 0.0134 gb (11.97 %)
reserved_unallocated: 0.0073 gb (6.56 %)
plugins: 0.0047 gb (4.23 %)
other_ets: 0.0031 gb (2.79 %)
atom: 0.0013 gb (1.19 %)
metrics: 0.0002 gb (0.18 %)
binary: 0.0002 gb (0.16 %)
mnesia: 0.0001 gb (0.07 %)
quorum_ets: 0.0 gb (0.04 %)
msg_index: 0.0 gb (0.03 %)
connection_channels: 0.0 gb (0.0 %)
connection_other: 0.0 gb (0.0 %)
connection_readers: 0.0 gb (0.0 %)
connection_writers: 0.0 gb (0.0 %)
mgmt_db: 0.0 gb (0.0 %)
queue_procs: 0.0 gb (0.0 %)
queue_slave_procs: 0.0 gb (0.0 %)
quorum_queue_procs: 0.0 gb (0.0 %)

[1mFile Descriptors[0m

Total: 2, limit: 65439
Sockets: 0, limit: 58893

[1mFree Disk Space[0m

Low free disk space watermark: 0.05 gb
Free disk space: 40.2112 gb

[1mTotals[0m

Connection count: 0
Queue count: 0
Virtual host count: 1

[1mListeners[0m

Interface: [::], port: 52275, protocol: clustering, purpose: inter-node and CLI tool communication
Interface: [::], port: 5672, protocol: amqp, purpose: AMQP 0-9-1 and AMQP 1.0
Interface: 0.0.0.0, port: 5672, protocol: amqp, purpose: AMQP 0-9-1 and AMQP 1.0


 rabbitmqctl list_users ²é¿´ÓÃ»§
Listing users ...
user    tags
guest   [administrator]

rabbitmqctl add_user sff sff Ìí¼ÓÓÃ»§ÃÜÂëÎªsff

Adding user "sff" ...


rabbitmqctl set_user_tags sff administrator ·ÖÅäÓÃ»§×é

Setting tags for user "sff" to [administrator] ...



>rabbitmq-plugins enable rabbitmq_management ÆôÓÃ²å¼ş

Enabling plugins on node rabbit@DESKTOP-2AB32DI:
rabbitmq_management
The following plugins have been configured:
  rabbitmq_management
  rabbitmq_management_agent
  rabbitmq_web_dispatch
Applying plugin configuration to rabbit@DESKTOP-2AB32DI...
The following plugins have been enabled:
  rabbitmq_management
  rabbitmq_management_agent
  rabbitmq_web_dispatch

started 3 plugins.


http://localhost:15672/#/





<img align="right" src="https://raw.githubusercontent.com/sanidgmbh/debugghost/master/debugghostlib/src/main/res/mipmap-xxxhdpi/ic_ghost.png" />
# DebugGhost
Android Debugging Tool for Developers

## Getting started
The following lines will start the service:
```java
Intent serviceIntent = new Intent(this, DebugGhostService.class);
serviceIntent.putExtra(DebugGhostService.INTENT_EXTRA_DB_NAME, MyDB.DATABASE_NAME);
serviceIntent.putExtra(DebugGhostService.INTENT_EXTRA_DB_VERSION, MyDB.DATABASE_VERSION);
startService(serviceIntent);
```
A notification will be shown, if the service is running. You can stop it every time by clicking on the notification.

## Not for production
DebugGhost is for developers and not for production purpose. Be aware of, that this project has **no focus on security or performance**. It's meant to be used while developing your app.

*TODO: example on how to setup app-project to compile DebugGhostLib only in a development-flavour*

## Versions
### v0.1b
Currently, DebugGhost only supports browsing through your projects sqlite database through a webbrowser on a machine in the same network.
*At this state, this was only tested using a Mac (Sierra) with Chrome.*

## SQLite-Browser
Starting the service will open a ServerSocket on your android device and lets you connect to the device in **the same local network**.
The IP address will be shown in the log.
Connect with your browser on port 8080.
```bash
http://<my-ip>:8080
```
## License

This project is licensed under the Apache 2 License - see the [LICENSE](LICENSE) file for details

# Getting started

[This repository](https://github.com/ahajji-microej/Example-Java-Widget) was made to be able to be tested directly on your browser, here's a step by step guide on how to test it.

1. Log in to GitHub.

2. Go to the [Example Java Widget](https://github.com/ahajji-microej/Example-Java-Widget) repository.

3. Click on the `Code` button, then select the `Codespaces` tab, and finally click `Create codespace on master` (You should see a popup with `Setting up ...`, it may take a while to start..). 

![The Codespaces tab in the Code window](https://hackmd.cross/uploads/upload_e06648ed280ec3336f35488887d6e194.png)

4. If you are on Firefox it may not work due to your browser privacy settings. You can either switch browser or remove the tracking content in your settings to make it work, but it may reduce security protections so be careful!

![Firefox settings page](https://hackmd.cross/uploads/upload_4f68ef2a5bb4ee3320eff5dd8a268dba.png)

5. The IDE ``Opening Java Project`` phase is quite long, so you will need to wait for it to finish loading.. But once started, click on `Yes` in the upcoming popup in the left corner to accept the [MicroEJ SDK EULA](https://developer.microej.com/license-agreement-sdk/), after reading them obviously, and build the MicroEJ project.

![The MicroEJ SDK EULA choice window](https://hackmd.cross/uploads/upload_0f26382d618d4f1278da6eedac193b72.png)

6. Then click on the `Reload project` button.

7. When the project has reloaded, you can go to the `PORTS` tab.

8. On the 6080 port, click on the preview in editor button (the little button that looks like a divided window with a magnifier).

9. It will open a Simple Browser, like the one in the screenshot below, and you will need to click on connect. This is where the simulator will be featured, so be sure to keep it open!

![Simple Browser and 6080 preview button](https://hackmd.cross/uploads/upload_4993902d79420d662c545183dd5d313f.png)

10. By now, the project must have been successfully loaded, you can verify this by looking at the bottom-left corner. You should only see `Java: Ready`. If you have an error you should see `Java: Error` or `Gradle: Build Error`, you can click on it to see the details. (See [Troubleshooting](#Troubleshooting))

8. If everything is good, go to the `Gradle` tab (the elephant icon on the left of the editor). 

9. Double click on the `Tasks > microej > runOnSimulator` task to run the project in the Simulator.

![Gradle tab](https://hackmd.cross/uploads/upload_24b4304a9ba5d77de8326c0a66689ff1.png)

10. After a few seconds you should see the Example Java Widgets Application running:

![Simulator shown in the Simple Browser](https://hackmd.cross/uploads/upload_26c31b9491e83bf9136d3bdbfebe461f.png)

11. You can now easily update the Application and quickly test your changes. For example, go to `src/main/java/com/microej/demo/widget/main/MainPage.java` and change the value of the `GRAY` variable (to the color red for example: `0xff0000`), then click on the refresh icon next to the `runOnSimulator` task to restart the simulator to see the result in the Simple Browser. 

12. That's it! Have fun with the MicroEJ SDK.

## Troubleshooting

- When you have `Java: Error` or `Gradle: Error`, click on it to see the logs. One of the most common errors is Gradle not succesfully building due to the SDK EULA not correctly accepted. You can try to reload your Codespace and start again.

- This can happen when you stop and start a task, you may think a new execution process is added.. But don't worry in reality only the logs are duplicated:

	```
	<-------------> 0% CONFIGURING [90ms]
	> root project > Resolve dependencies of :classpath
	<-------------> 0% CONFIGURING [90ms]
	> root project > Resolve dependencies of :classpath
	<-------------> 0% CONFIGURING [90ms]
	> root project > Resolve dependencies of :classpath
	=============== [ Initialization Stage ] ===============
	=============== [ Initialization Stage ] ===============
	=============== [ Initialization Stage ] ===============
	=============== [ Initialization Stage ] ===============
	=============== [ Converting fonts ] ===============
	=============== [ Converting fonts ] ===============
	=============== [ Converting fonts ] ===============
	=============== [ Converting fonts ] ===============
	=============== [ Converting images ] ===============
	=============== [ Converting images ] ===============
	=============== [ Converting images ] ===============
	=============== [ Converting images ] ===============
	=============== [ Launching on Simulator ] ===============
	=============== [ Launching on Simulator ] ===============
	=============== [ Launching on Simulator ] ===============
	=============== [ Launching on Simulator ] ===============
	<===========--> 87% EXECUTING [16s]
	> :runOnSimulator
	```
 
---
_Markdown_  
_Copyright 2025 MicroEJ Corp. All rights reserved._  
_Use of this source code is governed by a BSD-style license that can be found with this software._
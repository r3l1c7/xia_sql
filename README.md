# xia SQL (blind note)

> This plugin only inserts single quotes, no other blind injections, and the returned results need manual intervention to determine whether there is injection. If you need to test all injections, please forward the burp traffic to xray.

* burp plugin.
* Add a single quotation mark, two single quotation marks after each parameter, if the value is a pure number, add one more -1, -0.
* Since you don't know java, and it's written in java, the code is too bad, don't spray it. `
* List of thanks: Moonlit, Amao Agou, Shincehor, Xm17

************

## Plugin usage description
* Returning `✔️` means that the length of two single quotes is inconsistent with the length of one single quote, `indicating that there may be injection`.
* return `✔️ ==> ? ` means that the length of the original packet is the same as the length of two single quotes and different from the length of one single quote, ` indicates that it is likely to be injected`.
* Return `diy payload` representing the custom payload.
* Returning `time > 3` means that the time to visit the website is greater than 3 seconds. You can use this function to test the `time blind note` with the custom payload function.
* Supports json format, V1.9 and above `supports json multi-layer nesting`.
* The supported parameter values ​​are `pure numbers -1, -0`.
* Support `Send to plugin scan by right-clicking` (even if it has been scanned before, you can still scan it again by right-clicking) Remarks: A response packet must be sent to right-click, otherwise it cannot be sent, so that the length of the original data packet can be compared.
* Support for `custom payload`.
* Support parameter value `null` in custom payload.
* Monitor Proxy traffic.
* Monitor Repeater traffic.
* The same data packet is scanned only once, algorithm: `MD5 (url without parameters + parameter name + POST/GET)`.

*********
### 2022-5-24
#### xia SQL 2.3
* Added a new status column, `run...` indicates that the relevant payload is being sent, `end!` indicates that the scan has been completed, and `end! ✔️` indicates that the scan is completed and the result may be injected.

![image](https://user-images.githubusercontent.com/30351807/169846432-106a0764-7f20-466e-831d-8b8615c9dda7.png)


*********
### 2022-5-20
#### xia SQL 2.2
* Optimize proxy mode and sometimes the traffic does not come to the problem.
* Under optimized Proxy and Repeater modes, static resources are not processed. Suffix: jpg, png, gif, css, js, pdf, mp3, mp4, avi` (right-click sending does not affect)`

![image](https://user-images.githubusercontent.com/30351807/169476496-e2a7351b-f701-42f8-b56b-a8d411ab6eca.png)


*********
### 2022-5-12
#### xia SQL 2.1
* Added empty parameter value in custom payload

![image](https://user-images.githubusercontent.com/30351807/168087873-1e57c10d-cf66-4783-af1e-3d075f629c4d.png)

*********
### 2022-4-25
#### xia SQL 2.0
* UI interface optimization
* Add custom payload function
* If the custom payload accesses the website for more than 3 seconds, time > 3 will be displayed.

![image](https://user-images.githubusercontent.com/30351807/165055862-c0a3a72e-918c-47b7-84ad-f74b1cb2f365.png)

![image](https://user-images.githubusercontent.com/30351807/165055655-1ac9b40a-4c68-424a-b73e-f31b3b5f1162.png)

*********
### 2022-4-11
#### xia SQL 1.9
* Support json multi-level nesting
* New column: time, used to update the custom payload later, you can view the time used by each data packet.
![image](https://user-images.githubusercontent.com/30351807/162653146-5caaf300-3b1c-4680-af06-e84364a5e3b4.png)


*********
### 2022-4-8
#### xia SQL 1.8
* Added right click to send to plugin scan
* Optimized the return speed of data packets in Monitor Repeater mode.
![image](https://user-images.githubusercontent.com/30351807/162444663-ecc491e2-9a74-4d0f-8b1f-c6ce8f61546a.png)


*********
### 2022-4-2
#### xia SQL 1.7
* Fix the bug of displaying content in poxry mode under burp2.x version
![image](https://user-images.githubusercontent.com/30351807/161375553-cee2df69-5681-4818-95ae-0ed389795ea4.png)


*********
### 2022-3-31
#### xia SQL 1.6
* Update the algorithm that the same data packet is scanned only once, algorithm: MD5 (url without parameters + parameter name + POST/GET)
![image](https://user-images.githubusercontent.com/30351807/161045937-d0e3584a-d610-4b26-ba33-6cc08dd9e8fa.png)


*********
### 2022-3-29
#### xia SQL 1.5
* Uncheck "Monitor Repeater" by default, and increase the default check "If the value is a number, perform -1, -0".
* Change the monitoring proxy mode to passive mode to improve the interactive experience.
* Added the same data packets are scanned only once. Algorithm: MD5 (url + parameter name), if it is a post package, the value change will not be rescanned, and the parameter name change will be required to scan again.


*********
### 2022-2-13
#### xia SQL 1.4
* Updated an option to perform -1, -0 if the value is a pure number
![image](https://user-images.githubusercontent.com/30351807/153725862-8ec9e92f-66b5-4d5c-9c3e-fb18f5afaa94.png)


*********
### 2022-2-11
#### xia SQL 1.3
* Updated the length of the original package to return ✔️ ==> ?

![image](https://user-images.githubusercontent.com/30351807/153590052-42293c4a-7a85-4740-b29e-209a7c27d403.png)


*********
### 2022-2-11
#### xia SQL 1.2
* Updated to support json format

![image](https://user-images.githubusercontent.com/30351807/153567877-479a0e15-9d6c-43f5-84d9-80c5dfb6fd03.png)


*********
### 2022-2-10
#### xia SQL 1.1
* Updated serial number
* Updated with changes tick
* Updated to ignore if that packet has no parameters. In this way, the proxy mode will not be a bunch of packages.

![image](https://user-images.githubusercontent.com/30351807/153390045-2b3769f6-151b-45c0-a555-53cda4fef2f2.png)


*********
# image display

![image](https://user-images.githubusercontent.com/30351807/153139897-08e6b69b-f129-4fab-a62e-037351d7c60f.png)

![image](https://user-images.githubusercontent.com/30351807/153139950-a4f51f4b-e39d-459d-91b8-e326c2c74c29.png)


![image](https://user-images.githubusercontent.com/30351807/153139522-b9af5d35-36a3-4204-b2f4-7b6a11253d41.png)

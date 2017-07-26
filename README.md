---
title: Zodiva Chat SDK
description: Open Zodiva Chat in a cordova/phonegap based app.
---
<!--
# license: Licensed to the Apache Software Foundation (ASF) under one
#         or more contributor license agreements.  See the NOTICE file
#         distributed with this work for additional information
#         regarding copyright ownership.  The ASF licenses this file
#         to you under the Apache License, Version 2.0 (the
#         "License"); you may not use this file except in compliance
#         with the License.  You may obtain a copy of the License at
#
#           http://www.apache.org/licenses/LICENSE-2.0
#
#         Unless required by applicable law or agreed to in writing,
#         software distributed under the License is distributed on an
#         "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
#         KIND, either express or implied.  See the License for the
#         specific language governing permissions and limitations
#         under the License.
-->

 
# cordova-plugin-zodiva

This plugin launches Zodiva's Chat SDK when calling `cordova.zodiva.open()`.

# Installation


```sh
cordova plugin add https://github.com/rajnandan1/zodiva
```
    
# How to Use

### Basic Use
	cordova.zodiva.open('app_id','secret_key');
> Zodiva SDK will ask for the user's _email, name and gender_	
### Advanced Use
For now zodiva lets you set the current user. All you have to do is pass the current users email, gender and name. Something like this -

    cordova.zodiva.open('app_id','secret_key','device token','email=test@gmail.com,dn=Test Sdk,gender=male');

> Zodiva SDK will use the  _email, name and gender_	provided by the app. Gender can be only `male` or `female`
	
This third and fourth paremeters are optional. 

Third parameter is the device token for the user. This will be used to send push notification to the user. You can set it up in your [Dashboard](https://zodiva.com/psa/#/sdk)

In case you do not use the fourth parameter the SDK will ask for the user's email, name and gender. If you pass this string as the fourth parameter the sdk will start the session automatically.

# Getting `app_id` and `secret_key`

To get the app_id and secret_key you will have to first [Sign up](https://zodiva.com/psa) on Zodiva. You will find the app id and app secret in the `account details section`.

# Customizing the SDK

Select `Customize` from left side menu. Most of the things here are for the JS widget. 

### Important Parameters to be modified

- __Your Texts__: These are the options that are shown when a user starts a session for the first time. It helps to understand the need of the user. _(what are the services offered)_. You can edit the predefined options or add your own. To add type down the `text` and give it a `priority value`
- __Primary Color__: This is the primary color of the SDk. Any Color here will change the color of elements like `Navigation Bar` etc.
- __Secondary Color__: This is the secondary color of the SDk. Any Color here will change the color of elements like `Primary Buttons` etc.

# QUESTION SET 

Under `Customize` from left side menu. These are the questions _(option based)_ that are shown to the user to capture additional information before even a stylist connetcs with him

- __Choose a Question__: Select an option that you have already entered in the section above.
- __Add a Question__: Use this to add questions under that option for the user, to be asked by the zodiva bot just after the session starts.
- __Enter  a Question__: Use the box on the left to enter question. You can add as many questions as you want.
- __Enter  Options__: Use the box on the right to enter the options. Give a comma between each option. Only `text` options are supported as of now. User can only pick one option.
 
# Notification Settings 

Under `SDK Settings` from left side menu. For now only _(option based)_ android is supported

- __Server Key__: (Required)This is the server key in the google developer console. Go to console > Credentials.
- __Sound Name__: (Optional)Sound to be played when a notification comes in. The file should be already added by in your app.
- __Icon Name__: (Optional)Icon to be shown in the status bar. The file should be already added by in your app.
- __Color__:(Optional) Color of the background image for the icon. Needs HEX vlaue eg #111111.
 
 

 
> For additional information or any queries wrtie to `rnsharma@zodiva.com`
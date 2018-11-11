# Week7
# Project 7 - WordPress Pentesting

Time spent: **10** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

## 1. Authenticated Stored Cross-Site Scripting via Image Filename
  - [ ] Summary: 
    - Vulnerability types:XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.10
  - [ ] GIF Walkthrough: ![](https://github.com/dixon31896/assignments/blob/master/XSS1.gif)
  - [ ] Steps to recreate: Have a media file with example name ```example<img src=a onerror=alert(document.cookie)>.jpg``` and upload it to wordpress. 
                            Then check the attachment page of the media file. 
  - [ ] Affected source code:
    - [Link 1](https://github.com/WordPress/WordPress/commit/c9e60dab176635d4bfaaf431c0ea891e4726d6e0)
## 2. (Required) Username Enumeration
  - [ ] Summary: 
    - Vulnerability types: Username Enumeration
    - Tested in version: 4.2 
    
  - [ ] GIF Walkthrough: ![](https://github.com/dixon31896/assignments/blob/master/UserEnum.gif)
  - [ ] Steps to recreate: On wordpress you can try all kinds of usernames and passwords. If you find a correct username wordpress will give you a message saying that the username is correct but the password is not. Now someone can keep using that username and keep trying different kinds of passwords until they can find the correct one.
  
## 3. (Required) Authenticated Stored XSS in YouTube URL Embeds
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.13
  - [ ] GIF Walkthrough: ![](https://github.com/dixon31896/assignments/blob/master/XSSutube.gif)
  - [ ] Steps to recreate: Using this format ```[embed src='https://www.youtube.com/embed/12345\x3csvg onload=alert(1)\x3e'][/embed]``` a user will try to visit the youtube video on the post but the pop up will appear.
  - [ ] Affected source code:
    - [Link 1](https://github.com/WordPress/WordPress/commit/419c8d97ce8df7d5004ee0b566bc5e095f0a6ca8)


## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [2018] [Dixon Lu]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

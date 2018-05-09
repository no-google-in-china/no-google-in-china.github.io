
# There is no Google in China.

Explaining situation from technical perspective

You may have heard that there is no Google( as well as Facebook, Twitter ) in China.
Of course there is Google China as business entity, and of 2017-2018 it is even expending its presense. 

However since about 2013 there is no Google servers within China, that already make requests travel over longer distance,
and not as much instant as most are used now.

Next, all services are blocked. There is no google.com, any google*.com, android.com, Google Play Android application market. (go lang site)
Absotely all services and products are not available.

## Problems as Consequances

1. Publishing Android app only to Google Play, you miss 30% (700 000 000) smartphone users [1](https://en.wikipedia.org/wiki/List_of_countries_by_smartphone_penetration) (Yes world population is over 7 billion, and China has 1.3)  
[2](https://en.wikipedia.org/wiki/List_of_countries_by_number_of_Internet_users)  
Consider giving a way to get apk for side-loading or publishing to other stores as well: Amazon Store, F-droid (https://f-droid.org/) for open source project, Samsung makretplace and Chinese-based XiaoMi Market, Huawei Market, Tencent Market

2. Some site fails to load over jQuery not available from Google CDN.



Some companies may be anaware, some may not care. The result is worse experience of Internet users in China.  
And this article tries to solve problem technically: what developers should know and do.

## Solutions

### For project/site owner

Know, act.

### For users

1. Use VPN
That is solution to name to a one person but not to all. And there is no stable VPN service in China.
2. Search alternatives: Microsoft https://bing.com/, Russian Yandex https://yandex.com. ( ~~https://duckduckgo.com~~ returns the same results as Google and is not available.)
3. NoScript browser plugin, that can block JS resource from specific site, becomes handy. Adding google site into as blacklisted/untrusted site solves long loading issue. But of course not jQuery on Google CDN issue.
3. It should be possible to create browser plugin, that would dynamically replace Google CDN with customizable alternative, but not yet known.

## List

List of projects affected

1. eclipse.org had once website uupdate that made eclipse.org page loading long. Issue was raised, but consequently similar issues appeared.
2. maven.org site was long to load, after their upgrade of skin, that started using jQuery on google CDN. Was resolved.
3. https://projectlombok.org/ newer site. (Raise an issue point to this site, if you can see their bug tracker )
4. http://struts.apache.org/ solved by https://github.com/apache/struts-site/pull/53 "Use http://code.jquery.com instead of googleapis.com"

## Recent warming up

1. Some resources are available from `*.google.cn` mirrows
- https://developers.google.cn/
- https://developer.android.google.cn/
2. Google is opening offices in Shenzhen and other major cities. Still active in Developer relations.

## Help

The problem re-appears as some frameworks add Google CDN resource assuming that they are always available,
and always quick. 

- Please file an issue explaining, this site should be helpful for reference.
- [Edit/extend this page](https://github.com/no-google-in-china/no-google-in-china.github.io/edit/master/README.md)



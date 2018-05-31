
# There is no Google in China.

Explaining situation from technical perspective

You may have heard that there is no Google( as well as Facebook, Twitter ) in China.
Of course there is Google China as business entity, and of 2017-2018 it is even expending its presense. 

However since about 2013 there is no Google servers within China, that already make requests travel over longer distance,
and not as much instant as most are used now.

Next, all services are blocked. There is no google.com, any google*.com, android.com, Google Play Android application market, Youtube. (go lang site)
Absotely all services and products are not available.

## Problems as Consequances

1. Publishing Android app only to Google Play, you miss 30% (700 000 000) smartphone users 
[1](https://en.wikipedia.org/wiki/List_of_countries_by_smartphone_penetration) 
[2](https://en.wikipedia.org/wiki/List_of_countries_by_number_of_Internet_users)
(Yes world population is over 7 billion, and China has 1.3)  
Consider giving a way to get apk for side-loading or publishing to other stores as well: Amazon Store, F-droid (https://f-droid.org/) for open source project, Samsung makretplace and Chinese-based XiaoMi Market, Huawei Market, Tencent Market
2. Long waiting for page to load. Google is blocked not in a way that instantly returns error, but requests just finish by timeout, that are often about 1 minute. That is for 1 minute or so a web page is blank in browser.
3. Some sites fail to display UI elements like menu over jQuery not available from Google CDN. That is while UI is shown, interaction is not possible.
4. embedded Youtube videos are not shown. If video materials are key way for introduction, consider giving and alternative way to get it.


Some companies may be unaware, some may be not caring. The result is worse experience of Internet users in China.  
And this article tries to solve problem technically: what developers should know and do.

Why you may not heard before? Because 90% of Chinese developers cannot express themselves in English. Relatively more are shy, passive, not really know that can affect open source project. (This is however changing and fast.)

## Solutions

1. For web site owners: never think that Internet resources are always available (it can be DNS error, 1 minute downtime, whatever...), so 
- load JS resources **asynchronosly**: the page is shown while some JS may need some more time to load.
- do not use CDN: if you site is already published on some sort of CDN like GitHub pages, why to have part of resources on other CDN? That would only make complecation (more names to be resolved via DNS, more servers contacted and so on)

### For project/site owner

Know, act.

### For users

1. Use VPN
That is solution to name to a one person but not to all. And there is no stable VPN service in China.
2. Search alternatives: Microsoft https://bing.com/, Russian Yandex https://yandex.com. ( ~~https://duckduckgo.com~~ returns the same results as Google and is not available.)
3. NoScript browser plugin, that can block JS resource from specific site, becomes handy. Adding google site into as blacklisted/untrusted site solves long loading issue. But of course not jQuery on Google CDN issue.
4. Ghostery browser plugin can block Google analitics and save time on page load.
5. It should be possible to create browser plugin, that would dynamically replace Google CDN with customizable alternative, but not yet known.

## List

List of projects affected

1. [v] <eclipse.org> had once website uupdate that made eclipse.org page loading long. Issue was raised, but consequently similar issues appeared.
2. [v] <maven.org> site was long to load, after their upgrade of skin, that started using jQuery on google CDN. Was resolved.
3. [ ] <https://projectlombok.org/> newer site is now having not accessing menus. (Raise an issue point to this site, if you can see their bug tracker )
4. [v] <http://struts.apache.org/> solved by [apache/struts-site#53](https://github.com/apache/struts-site/pull/53) "Use http://code.jquery.com instead of googleapis.com"

## Recent warming up

1. Some resources are available from `*.google.cn` mirrows
- <https://developers.google.cn/>
- <https://developer.android.google.cn/>
- <https://golang.google.cn/>
2. Google is opening offices in Shenzhen and other major cities. Still active in Developer relations.

## Help

The problem re-appears as some frameworks add Google CDN resource assuming that they are always available,
and always quick. 

- Please file an issue explaining, this site should be helpful for reference.
- [Edit/extend this page](https://github.com/no-google-in-china/no-google-in-china.github.io/edit/master/README.md)



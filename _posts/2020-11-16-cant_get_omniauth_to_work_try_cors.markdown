---
layout: post
title:      "Can't Get Omniauth to Work? Try CORS"
date:       2020-11-17 00:37:40 +0000
permalink:  cant_get_omniauth_to_work_try_cors
---

I struggled for hours trying to get omniauth to work. First I followed the instructions in the course. Then I foudn and followed the instructions on half a dozen blogs strewn around the internet, using both github and facebook as authenticators, and it did not work. Just when I was about to give up, I asked my roommates, both of whom are web developers, what I should do. They immediately asked me if I had the CORS browser extension.

I had never heard of the CORS extension before, and it had never come up during my research. My roommates insisted that I download the extension and give it a shot. After I had downloaded and extension and enabled it, the problem went away. So whats happening? To be honest, after about an hour of reading about CORS, I can not say for sure. It seems it disables some security features that are built in to your browser. Since it disables security features, make sure to only turn it on when testing omniauth, and then immediately disable it again for security reasons.



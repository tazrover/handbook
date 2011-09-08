# Frequently Asked Questions
<a name='faq'></a>

## "How are programs kept alive? Do I need to use Forever?"

Nodejitsu's cloud services watch your programs for you! You shouldn't have to do anything special to keep your apps running, much less use Forever.

## "How can I make my app use a port other than port 80?"

Connecting to other servers using arbitrary ports requires no special considerations. However, *listening* for outside connections is currently limited to port 80 on the Nodejitsu platform because we require http host headers for domain name resolution of subdomains.

The ability to host tcp applications on nodejitsu and listen on non-80 ports is on our roadmap but has no associated timeline.


## "Why won't this C++ addon module/dependency install?"

Some C++ addons require libraries that are not included in Nodejitsu's infrastructure by default. For example, [node-canvas](https://github.com/learnboost/node-canvas) requires [cairo](http://cairographics.org/), which is not available on nodejitsu's platform.

There is currently no process for getting a library such as cairo installed on our infrastructure.
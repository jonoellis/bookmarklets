# Bookmarklets

## Copy and Alert the components of a URL 
```javascript
javascript:
u=(window.location.protocol);
v=(window.location.href);
w=(window.location.hostname);
x=(window.location.pathname);
y=(window.location.search);
z=(window.location.hash);
a=("Protocol: "+u+"\nHref: "+v+"\nHostname: "+w+"\nPathname: "+x+"\nSearch: "+y+"\nHash: "+z);
navigator.clipboard.writeText(a);
alert(a);
```

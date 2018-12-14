# Bookmarklets

## Kill Sticky
```javascript
javascript:\(function\(\)%7B\(function%20\(\)%20%7Bvar%20i%2C%20elements%20%3D%20document.querySelectorAll\('body%20*'\)%3Bfor%20\(i%20%3D%200%3B%20i%20%3C%20elements.length%3B%20i%2B%2B\)%20%7Bif%20\(getComputedStyle\(elements%5Bi%5D\).position%20%3D%3D%3D%20'fixed'\)%20%7Belements%5Bi%5D.parentNode.removeChild\(elements%5Bi%5D\)%3B%7D%7D%7D\)\(\)%7D\)\(\)
```

## Wikipedia lookup
```javascript
javascript:\(function\(\)%20%7B%20function%20se\(d\)%20%7B%20return%20d.selection%20?%20d.selection.createRange\(\).text%20:%20d.getSelection\(\)%20%7D%20s%20=%20se\(document\);%20for%20\(i=0;%20i%3Cframes.length%20&&%20!s;%20i++\)%20s%20=%20se\(frames%5Bi%5D.document\);%20if%20\(!s%20%7C%7C%20s==''\)%20s%20=%20prompt\('Enter%20search%20terms%20for%20Wikipedia',''\);%20open\('http://en.wikipedia.org'%20+%20\(s%20?%20'/w/index.php?title=Special:Search&search='%20+%20encodeURIComponent\(s\)%20:%20''\)\).focus\(\);%20%7D\)\(\);
```

## Delete Google Sheet
```javascript
javascript:\(function\(\)%20%7B%20%20%20%20var%20eltMove%20=%20document.querySelector\('#\\\\:b2%3Ediv%3Espan'\);%20%20%20%20fireMouseEvent\(document.querySelector\('#docs-file-menu'\),%20'mousedown'\);%20%20%20%20fireMouseEvent\(eltMove,%20'mousedown'\);%20%20%20%20fireMouseEvent\(eltMove,%20'mouseup'\);%20%20%20%20fireMouseEvent\(eltMove,%20'mouseup'\);%20%20%20%20function%20fireMouseEvent\(eltTarget,%20myEvent\)%20%7B%20%20%20%20%20%20%20%20var%20screenX,%20screenY,%20clientX,%20clientY;%20%20%20%20%20%20%20%20var%20event%20=%20document.createEvent\('MouseEvents'\);%20%20%20%20%20%20%20%20event.initMouseEvent\(myEvent,%20true,%20true,%20window,%201,%20screenX,%20screenY,%20clientX,%20clientY,%20false,%20false,%20false,%20false,%200,%20null\);%20%20%20%20%20%20%20%20eltTarget.dispatchEvent\(event\);%20%20%20%20%7D%7D\)\(\);
```



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

## Edit in Rubric
```javascript
javascript:\(function\(\)%7B%20var%20lp%20=%20'https://publishing.mygov.scot/#/contents/',%20b%20=%20document.getElementsByTagName\('body'\),%20id,%20lnk,%20error%20=%20'Sorry,%20the%20ID%20of%20this%20content%20item%20could%20not%20be%20found.';%20if%20\(b.length\)%20%7B%20id%20=%20b%5B0%5D.getAttribute\('data-uuid'\);%20if%20\(id\)%20%7B%20lnk%20=%20lp%20+%20id;%20window.location%20=%20lnk;%20return%20true;%20%7D%20%7D%20alert\(error\);%20%7D\)\(\);
```

## www=stage
```javascript
javascript:\(function\(\)%7Bvar%20loc=location.href;
if\(loc.indexOf\(%22www%22\)%3E=0\)%7Bloc=loc.replace\('www','stage'\);
%7Delse%7Bloc=loc.replace\('stage','www'\);
%7Dlocation.replace\(loc\)%7D\)\(\)
```

## View JSON
```javascript
javascript:window.location.href=window.location.href+'index.json';
```

## Edit gov.scot in Rubric
``` javascript
javascript:\(function\(\)%7B%20var%20lp%20=%20'https://beta.publishing.gov.scot/#/contents/',%20b%20=%20document.getElementsByTagName\('body'\),%20id,%20lnk,%20error%20=%20'Sorry,%20the%20ID%20of%20this%20content%20item%20could%20not%20be%20found.';%20if%20\(b.length\)%20%7B%20id%20=%20b%5B0%5D.getAttribute\('data-uuid'\);%20if%20\(id\)%20%7B%20lnk%20=%20lp%20+%20id;%20window.location%20=%20lnk;%20return%20true;%20%7D%20%7D%20alert\(error\);%20%7D\)\(\);
```

## View Data Layer - ALERT
```javascript
javascript:\(function\(\)%7B%20alert\(JSON.stringify\(dataLayer,%20function\(key,value\)%20%7Bif\(key%20==%20'gtm.element'\)%7B%20return%20'format';
%7D%20return%20value;
%7D,%204\)\)%20%7D\)\(\);
```

## View Data Layer - DIV
```javascript
javascript:\(function\(a\)%7Ba=document.createElement\('div'\);a.style.position=%20'fixed';
a.style.left='80%';
a.style.right='0%';
a.style.top='0%';
a.style.zIndex='100000';
a.style.background='white';
a.innerHTML=%20JSON.stringify\(dataLayer,%20function\(key,value\)%20%7Bif\(key%20==%20'gtm.element'\)%7Breturn%20'some%20element%20here';
%7D%20return%20value;
%7D,%204\);
document.body.appendChild\(a\);
%7D\)\(\);
```

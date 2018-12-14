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

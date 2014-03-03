SHB-js
======

Social HTML Buttons
Example of SHB.js. See more at [How to Social Buttons in HTML only using Twitter Bootstrap 3 and Font Awesome Icons (No Javascript)](http://ostr.io/code/html-social-like-share-buttons-no-javascript.html)

======

###Usage
```
SHB.build('elementID');
```

```
SHB.build({options});
```

#####Options:
 
 - **elementID**: string | ID of parent element
 - **buttons**: object | Object with loadable / custom buttons
 - **pref**: object | Object with preferences:
    - btnSizeClass: string | Button sice class: '' (default) | btn-sm | btn-lg | btn-xs
    - btnTag: string | a (default) | button
    - btnLinkAttr: string | href (default)
    - btnClass: string | 'btn btn-default'
    - url: string | URL to share or like, default: window.location.href
    - iconClass: string | default: fa
    - iconSize: string | default: fa-lg
    - title: string | Shareable title | default: document.title
    - desc: string | Shareable description | default: document.head.meta(name=description)
    - img: string | Shareable image | default: document.head.meta(name=image)
 

```
/*Load some buttons and Create Custom Button and small size of buttons*/
SHB.build({
  elementID: 'shb_custom',
  pref: {
  	btnSizeClass: 'btn-sm',
	},
	buttons: {
		fbLike: true,
  	tweet: true,
    plusOne: true,
    surf: true,
  
    customButton: {
  		 iconClass: 'fa-github',
  		 iconURL: 'https://github.com/dr-dimitru',
  		 iconParams: {} 
  	},
  }
});
```


###Example
```
<head>
  <link rel="stylesheet" href="//netdna.bootstrapcdn.com/bootstrap/3.0.0/css/bootstrap.min.css">
	<link rel="stylesheet" href="//netdna.bootstrapcdn.com/font-awesome/4.0.3/css/font-awesome.css">
	<link href="/styles/shb.css" rel="stylesheet">
  <script src="/scripts/shb.min.js" type="text/javascript"></script>
<head>
<body>
  <center>
		<p>Build All Default Buttons</p>
		<div class="btn-group" id="shb"></div>
  </center>
  <script>
    SHB.build('shb');
  </script>
</body>
```

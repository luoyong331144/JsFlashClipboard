<h1 style="color:#333">This example must be run in container. For example, Tomcat, Jetty, etc...</h1>


<!DOCTYPE html>
<html>
<head>
<title>cope text to clipboard</title>
<style type="text/css">
textarea {
	width : 300px;
	height: 300px;
}
</style>
<script type="text/javascript" src="ZeroClipboard.js"></script>
<script type="text/javascript"> 
function initClipboard() {
	ZeroClipboard.setMoviePath("ZeroClipboard.swf");
	var clip = new ZeroClipboard.Client();
	clip.setHandCursor(true);
	clip.addEventListener('mouseOver', function() {
		var value = document.getElementById("copied").value;
		clip.setText(value);
	});
	clip.glue("copy");
}
</script>
</head>
<body onLoad="initClipboard()">
	<h1>This example must be run in container. For example, Tomcat, Jetty, etc...<h1>
	<textarea id="copied">Text in this textarea will be copied.</textarea>
	<button id="copy">Copy to clipboard</button>
	<textarea></textarea>
</body>
</html>

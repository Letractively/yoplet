# What it does #

Provides local FS manipulation, such as

  * files scrutation
  * files read / write / upload / delete
  * upload comes with cookie support
  * synchronous / asynchronous callback support (see demo page)
  * debug panel

with callback functionality (liveconnect through JSObject api)

# How it works #

Signed applet embedding httpclient does the job

# Where to start from #

  * Download installer
  * Run installer to sign and deploy applet jar in hosted folder
  * integrate within html

```
	<applet id="yoplet"
			name="yoplet"
			code="org.yoplet.Yoplet.class"
			archive="/public/libs/yoplet.jar"
			width="320px"
			height="240px"
			codebase="yoplet"
			mayscript="true">
		  <param name="action" value="write" />
		  <param name="debug" value="true" />
		  <param name="filePath"  value="/path/to/file/handled" />
		  <param name="flagPath"  value="/path/to/flag/file" />
		  <param name="lineSeparator"  value="---" />
		  <param name="url" value="http://y0pl3t.appspot.com/test/upload"/>
		  <param name="content" value="content to be written"/>
		Java is required for this page
	</applet>
```
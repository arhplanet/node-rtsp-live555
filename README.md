# rtsp-live555
## introduction

This is a wrapper which allows you to get RTSP stream from IPC and export in FLV stream.

## Installation

### NPM

`npm install rtsp-live555` - install lastest stable version

`npm install godka/node-rtsp-live555` -install lastest version from github

### Clone the last version from Github
`git clone https://github.com/godka/node-rtsp-live555`

### Sample
The sample creates a web server at port 80 and scans RTSP address from IPC with onvif.A stream will be shown on the video element via flv.js when pressing 'play' button.

```javascript
var stream = new rtsp.Live555Client({ input: 'rtsp://xx:xx@xxx.xxx.xxx.xxx/udp/av0_0' });
stream.on('start', () => {
	console.log(_url + ' started');
});

stream.on('stop', () => {
	console.log(_url + ' stopped');
});
		
stream.on('data', (data) => {
    //you can write your method here
    //data is flv stream
});
```
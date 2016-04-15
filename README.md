rc
==

A stupidly simple RESTful client.

This "client" is just a shell script that uses [curl] (http://curl.haxx.se) 
to send requests to a RESTful web service and receive responses.

### Prerequisites

In order to use `rc` you need the following:

* Relatively recent version of curl (tested with curl 7.47)
* Bash shell (tested with bash 4.3.42(1))

### Installation

1. Copy the file named `rc` to some directory that is on your path.
2. Make sure the permissions on the file allow you to execute it.

### Usage

Run the script with no arguments to see the options.

When making a request that sends a body (i.e. POST, PUT, PATCH) the body 
content will be read from stdin.

The response body content will be written to stdout.

Environment variables provide the base URL for the web service, and the 
values for the `Accept` and `Content-Type` headers.

* `BASE_URL` -- base URL for the web service; default: `http://localhost:8080`
* `CONTENT_TYPE` -- value for the `Content-Type` header; default is 
  `application/json`
* `ACCEPT` -- accept header; default prefers the type specified by
  `CONTENT_TYPE`, then text of any kind, then application data of any kind

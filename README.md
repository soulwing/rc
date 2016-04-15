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

When making a request that sends a body (POST, PUT, PATCH) the body content
will be read from stdin.

When making a request that returns a response (any) the body content will
be written to stdout.

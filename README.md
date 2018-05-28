# openshift-hello

### Description
This is a simple and small image that just gives a response ("Hello from OpenShift") on port 8080. It can be useful in some test cases.

### Usage

Start the build process:
```
$ oc new-app https://github.com/khelmric/openshift-hello.git
...
```

Expose the route:
```
$ oc expose svc/openshift-hello --hostname=openshift-hello.example.com
```

Check the results:
```
$ curl http://openshift-hello.example.com
<xmp>
Hello from OpenShift
</xmp>
```

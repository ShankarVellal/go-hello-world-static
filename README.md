# Hello, World! in Go using a static binary

Build a Go static binary:
- ``cd $DIR/go/src/main``
- ``CGO_ENABLED=0 GOOS=linux go build -a -installsuffix cgo .``

Run the static binary in a Docker container:
- ``cd $DIR``
- ``docker build -t go-hello-world-static-test .``
- ``docker run --name go-hello-world-static -d -p 80:8080 -t go-hello-world-static-test``
FROM https://stackoverflow.com/a/61738823

Build with the following command:
```
docker build --target ubuntu-with-sshd -t ubuntu-with-sshd .
```

Then run with:
```
docker run -p 2222:22 ubuntu-with-sshd
```

To connect to container via local port, run: `ssh -v localhost -p 2222`.

To check for container IP address, use `docker ps` and `docker inspect`.

To run via docker-compose:
```
docker-compose up --build
```

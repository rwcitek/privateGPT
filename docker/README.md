Build a docker image

```bash
docker build --tag privategpt .
```

Create interactive container
```bash
docker run --rm -it -v ${PWD}/..:/tmp/gpt --name gpt privategpt sleep inf &
```

Exec into interactive container
```bash
docker container exec -it gpt /bin/bash
```

Remove interactive container
```bash
docker container stop gpt
```




## Start using a pre-built image

### Create a background container

```bash
docker run -d --name gpt rwcitek/privategpt sleep inf
```

### Exec into background container and run interactive privateGPT

```bash
docker container exec -it gpt /bin/bash
python3 privateGPT.py
exit   # when finished
```

### Stop and remove background container

```bash
docker container stop gpt ; docker container rm gpt
```

## To build your own image from the Dockerfile

### Set up code needed in image

From the `./docker` folder, i.e. the one with the Dockerfile, run this ...

```bash
rsync -vaR .././[a-z]* --exclude=docker src/
```

### Build a docker image

```bash
docker build --tag rwcitek/privategpt .
```




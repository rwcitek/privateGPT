
### Set up code needed in image
```bash
rsync -vaR .././[a-z]* --exclude=docker src/
```

### Build a docker image

```bash
docker build --tag rwcitek/privategpt .
```

### Create a background container

```bash
docker run -d --name gpt rwcitek/privategpt sleep inf
```

### Exec into interactive container and run privateGPT

```bash
docker container exec -it gpt /bin/bash
python3 privateGPT.py
exit   # when finished
```

### Remove interactive container

```bash
docker container stop gpt
docker container rm gpt
```

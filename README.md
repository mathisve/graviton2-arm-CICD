![publish](https://github.com/mathisve/graviton2-arm-CICD/actions/workflows/docker.yaml/badge.svg)
# graviton2-arm-CICD
Building docker containers on x86/amd64 for arm64.
```yaml
-  
  name: Setup QEMU
  uses: docker/setup-qemu-action@v1
-
  name: Set up docker Buildx
  uses: docker/setup-buildx-action@v1
-
  name: Build and push
  run: |
    docker buildx build \
    --platform linux/amd64,linux/arm64 \
    -t ${{ github.repository_owner }}/graviton2-arm-cicd:latest \
    --push \
    .
``` 

Find the accompanying video here:
[![image](https://github.com/mathisve/graviton2-arm-CICD/blob/master/img/graviton2.png)](https://youtu.be/ObfxS7x0UdY)
(click the Image!)

# Build és futtatási útmutató

## Automatikus build és feltöltés GitHub Actions segítségével

1.  Frissítsd a GitHub repository **Actions** beállításait a Docker Hub
    hitelesítő adataiddal, mint **secrets**:
    -   `DOCKER_USERNAME`
    -   `DOCKER_PASSWORD`
2.  A **main** branch-re történő push esetén a GitHub Actions:
    -   Felépíti (build) a Docker image-et
    -   Feltölti a Docker Hub-ra

## A futó konténer elérése

1.  Futtasd a következő parancsot:

    docker run -p 8080:80 -d ajdent/homework:latest

2.  Nyisd meg a böngészőt, és navigálj ide:

        http://localhost:8080

# Fájlok leírása
- .github/workflows/docker-build-push.yml
    A Github Actions leíró állomány
- Dockerfile
    A docker image építési lépéseit leíró állomány
- index.html
    Az elkészült image-et elindítva a konténer egy Nginx szervert futtat, amelynek ez lesz a kezdőoldala

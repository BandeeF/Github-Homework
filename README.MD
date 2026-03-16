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

    ``` bash
    docker run -p 8080:80 -d `DOCKER_USERNAME`/homework
    ```

2.  Nyisd meg a böngészőt, és navigálj ide:

        http://localhost:8080

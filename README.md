# Html-With-Docker
repositori ini berisikan aplikasi website html yang dijalankan dengan docker

untuk dapat menjalankan aplikasi HTML dengan docker, langkahnya adalah sebagai berkut :
1. buat Dockerfile yang isinya dilampirkan di repo ini.

2. build image :
    hamid-X455LAB SARWAN_HAMID # docker build -t webserver-sarwanhamid:v1 .
      Sending build context to Docker daemon  6.501MB
      Step 1/2 : FROM nginx:alpine
      alpine: Pulling from library/nginx
      b1f00a6a160c: Pull complete 
      893ab8d8734b: Pull complete 
      5bd0e3e256d9: Pull complete 
      79c4e9920d30: Pull complete 
      Digest: sha256:f1ca87d9adb678b180c31bf21eb9798b043c22571f419ed844bca1d103f2a2f7
      Status: Downloaded newer image for nginx:alpine
       ---> bf85f2b6bf52
      Step 2/2 : COPY . /usr/share/nginx/html
       ---> cbe6ea0843b7
      Removing intermediate container 78de58865ae1
      Successfully built cbe6ea0843b7
      Successfully tagged webserver-sarwanhamid:v1

3. memeriksa docker image
    hamid-X455LAB SARWAN_HAMID # docker images
      REPOSITORY              TAG                 IMAGE ID            CREATED             SIZE
      webserver-sarwanhamid   v1                  cbe6ea0843b7        3 minutes ago       22MB

4. menjalankan image
    hamid-X455LAB SARWAN_HAMID # docker run -d -p 8000:80 webserver-sarwanhamid:v1 
      698b34a46b043259b7e391d11e066d4d3f6acd9cd5f182416ad209f9f1137f34

5. ubah file index.html pada direktory /var/www/html dengan file index.html yang diinginkan (personal website)

6. buka/jalankan website dengan mengetikkan ip address di web browser

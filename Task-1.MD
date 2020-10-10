**Create a Docker Image and Store the Dockerfile**

<h4>Steps to complete the task: </h3> <br>
<h5>Login through your credentials, open Google Cloud Shell and execute these commands </h5> <br>

<pre><code>1. gsutil cat gs://cloud-training/gsp318/marking/setup_marking.sh | bash <br>
2. gcloud source repos clone valkyrie-app <br>  
3. cd valkyrie-app <br>
4. cat > Dockerfile <br>
5. FROM golang:1.10 M <br>
WORKDIR /go/src/app <br>
COPY source . <br>
RUN go install -v <br>
ENTRYPOINT ["app","-single=true","-port=8080"] <br>
EOF  <br>
6. docker build -t valkyrie-app:v0.0.1 . <br>
7. cd .. <br>
8. cd marking <br>
9. ./step1.sh </code> </pre>


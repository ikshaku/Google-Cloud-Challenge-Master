<h5>Continuation from Task 5</h5>

<h2>Create a pipeline in Jenkins to deploy your app</h2>

Execute the following commands in the Google Cloud Shell:
<pre><code>1. docker ps
2. docker kill container_id
3. export POD_NAME=$(kubectl get pods --namespace default -l "app.kubernetes.io/component=jenkins-master" -l "app.kubernetes.io/instance=cd" -o jsonpath="{.items[0].metadata.name}")
4. kubectl port-forward $POD_NAME 8080:8080 >> /dev/null &
5. printf $(kubectl get secret cd-jenkins -o jsonpath="{.data.jenkins-admin-password}" | base64 --decode);echo
6. sed -i "s/green/orange/g" source/html.go</code></pre> <br>
## Update project in Jenkinsfile
<pre><code>7. sed -i "s/YOUR_PROJECT/$GOOGLE_CLOUD_PROJECT/g" Jenkinsfile
8. git config --global user.email "you@example.com"
9. git config --global user.name "student"
10. git add . <pre><code>

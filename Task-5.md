<h5>Continuation from Task 4</h5>

<h4>Update the deployment with a new version of valkyrie-app</h4>

**Execute these commands in the Google Cloud Shell**

<pre><code>1. docker build -t gcr.io/$GOOGLE_CLOUD_PROJECT/valkyrie-app:v0.0.2 .
2. docker push gcr.io/$GOOGLE_CLOUD_PROJECT/valkyrie-app:v0.0.2
3. kubectl edit deployment valkyrie-dev</code></pre>

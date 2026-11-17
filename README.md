# Equipment classification on Kubernetes

To predict when an industrial machine needs maintenance, a random forest learns from synthetic temperature, pressure, vibration, noise and operating hours. Streamlit loads the saved model. Build the image in a running Minikube cluster and expose it with the supplied manifests.

## Run locally

```sh
minikube image build -t ai-streamlit-app:v1 .
kubectl apply -f k8s/
minikube service ai-streamlit-service
```

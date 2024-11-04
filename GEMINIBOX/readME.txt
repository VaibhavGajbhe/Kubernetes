1. CREATING NAMESPACE
   kubectl get namespace 
   kubectl create -f ./namespace.yml

  metadata :
  name : gemini-pro

  gemini-pro is a namespace its fallows all yml api-resources

2. CREARTING POD
   kubectl create -f ./pod.yml
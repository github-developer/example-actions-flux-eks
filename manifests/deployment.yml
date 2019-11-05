---
apiVersion: apps/v1beta1
kind: Deployment
metadata:
  name: aws-example-octodex
  annotations:
    fluxcd.io/automated: "true"
spec:
  replicas: 1
  strategy:
    rollingUpdate:
      maxSurge: 1
      maxUnavailable: 1
  minReadySeconds: 5
  template:
    metadata:
      labels:
        app: aws-example-octodex
    spec:
      containers:
      - name: aws-example-octodex
        # image: 00000000000000.dkr.ecr.my-region.amazonaws.com/example-eks:tag
        image: REGISTRY/IMAGE:TAG
        ports:
        - containerPort: 5000
        resources:
          requests:
            cpu: 250m
          limits:
            cpu: 500m

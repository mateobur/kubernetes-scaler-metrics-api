# Kubernetes Scaler Metrics API - Sysdig Monitor

Kubernetes `custom-metrics-apiserver` interface implentation, using Sydig Monitor as metrics backend.

## TODO

- Currently, the metric value is just set to `0` if the backend doesn't respond. Other options:
  - Cache metrics and return last known value
  - Fallback to CPU usage
  - Return an explanatory error message and terminate the pod

- Backend only implements some interface functions (the ones required by the HPA).
  - Create a complete metrics provider implementation, including error handling and defensive code

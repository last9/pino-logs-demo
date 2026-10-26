# How to send data to Last9

- Obtain OTLP Authroization header from Last9 dashboard.
- Run following command:

```sh
OTEL_EXPORTER_OTLP_LOGS_PROTOCOL='grpc' OTEL_EXPORTER_OTLP_LOGS_ENDPOINT=otlp.last9.io:443 OTEL_EXPORTER_OTLP_HEADERS="Authorization=<HEADER>"  OTEL_RESOURCE_ATTRIBUTES="service.name=<SERVICE_NAME>,service.version=<SERVICE_VERSION>" node index.js
```

> Replace the service name and service version with appropriate values.

## Components
- oathkeeper: Identity & Access Proxy (IAP)
- kratos-selfservice-ui-node: UI for Kratos self-service features
- kratos: Identity Infrastructure
- krakend: API Gateway
- rabbitmq: Message Broker
- jaeger: e2e Distributed Tracing
- prometheus: Monitoring & Alerting
- grafana: Data Visualization
- mailslurper: dev SMTP mailserver


Requests hit Oathkeeper which checks JWT with Kratos to determine access. Simple node app that implements browser login flow sits behind Oathkeeper. Krakend API gateway sits behind Oathkeeper. Internal messages sent to RabbitMQ via Krakend.

TODO:
- [x] Enable prometheus for oathkeeper
- [ ] Add consul to enable jaeger
- [ ] Add intranets to further secure/organize communication within network

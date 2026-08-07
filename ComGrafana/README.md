(preciso ajustar uma configuração, ainda não 100% completo)
# COMO USAR?

### Se nenhum dado do arquivo foi modificada, pode acessar cada serviço com:
Jaeger UI: http://localhost:16686 (prefiro ele :D)
Grafana: http://localhost:3000 (admin/password)

### No código que deseja apontar para eles, coloque esse collector:
"OTEL_EXPORTER_OTLP_ENDPOINT": "http://localhost:4317"

### Agora, na pasta que contém os arquivos, abra o terminal e rode:
docker compose up -d

### Para parar, rode no mesmo terminal:
docker compose down



(opcional, caso queiras analisar pelo grafana)
### NO GRAFANA, ADICIONAR O DATA SOURCE DO JAEGER
-> ir na barra lateral, em "Connectionns -> Add new connection"
-> apertar em "Add new connection" e pesquisar por "jaeger", selecione ele e escolha "add new data source"
-> no campo de url, coloque "http://jaeger:16686"
-> ignora todas essas configurações e aperte em "save & test"
```
Data source is working
Next, you can start to visualize data by building a dashboard from scratch or by querying data in the Explore view.
```
-> tudo certo! agora, na barra lateral vá em "explore" e Tcharammm!!

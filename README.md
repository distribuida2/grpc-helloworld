# Ejemplo GRPC: helloworld

## Entorno

Primero, tenemos que instalar las dependencias relacionadas con gRPC que trae el `requirements.txt`. Se recomienda usar un virtualenv.

```bash
pip install -r requirements.txt
```

## Como hacerlo funcionar

Una vez que tenemos el entorno preparado, generamos los stubs a partir del archivo helloworld.proto.

```bash
python -m grpc_tools.protoc -I protos --python_out=. --grpc_python_out=. ./protos/helloworld.proto
```

Una vez que están generados, en dos terminales diferentes, primero corremos el servidor y luego el cliente (en el caso de usar un virtualenv, tener en cuenta que esté instanciado en cada terminal).

```bash
python greeter_server.py
```

Y luego en otra terminal:

```bash
python greeter_client.py
```

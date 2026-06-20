# Tienda Perritos - Frontend

Interfaz web estática desarrollada con HTML, CSS y JavaScript para la gestión de productos de una tienda de mascotas. Desplegada en AWS EKS con pipeline CI/CD automatizado.

## Tecnologías
- HTML5 + CSS3 + JavaScript
- Nginx (servidor web)
- Docker
- Kubernetes (AWS EKS)
- GitHub Actions (CI/CD)

## Arquitectura
- **ECR:** Almacenamiento de imagen Docker
- **EKS:** Orquestación de contenedores
- **LoadBalancer:** Acceso público via AWS ELB
- **ClusterIP:** Comunicación interna con backend

## URL Pública
El frontend es accesible mediante el LoadBalancer de AWS:
http://aacb8eab884d549cabf67046579f80f1-1775439347.us-east-1.elb.amazonaws.com

## CI/CD
El pipeline se activa automáticamente al hacer push a la rama `deploy`:
1. Build de imagen Docker (Nginx)
2. Push a Amazon ECR
3. Rollout en EKS

## Cómo usar
1. Configurar secrets AWS en GitHub
2. Hacer push a rama `deploy`
3. El pipeline despliega automáticamente en EKS
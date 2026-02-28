# nexus-repositories
nexus-repositories

````
docker run -d \
  --name nexus \
  -p 8081:8081 \
  -p 5000:5000 \
  -v nexus-data:/nexus-data \
  --restart unless-stopped \
  -m 4g \
  --ulimit nofile=65536:65536 \
  sonatype/nexus3:latest
  
  ````
  ### If you are not using https

````
  vim daemon.json
````
````
{
  "insecure-registries": ["your-nexus-ip:5000"]
}
````
#### docker login
<img width="824" height="139" alt="image" src="https://github.com/user-attachments/assets/1a5341a2-fd80-4764-912d-e5463c346b4a" />


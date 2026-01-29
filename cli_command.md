🐳 Docker CLI Full Cheat Sheet 

---
docker --version → Check Docker version; verify environment for dev/CI pipelines.

docker info → Show Docker engine, containers, images, networks; debug host setup.

docker system prune → Clean stopped containers, dangling images, unused networks; free disk space.

docker image ls → List all images on your system; check available blueprints.

docker pull <image> → Download image from Docker Hub; use as base for dev or production.

docker rmi <image> → Remove unwanted images; keep disk clean and avoid conflicts.

docker run -it <image> sh → Start container interactively; debug or explore container shell.

docker run -d -p <host>:<container> --name <name> <image> → Start container detached with port mapping; run app in background.

docker ps → Show running containers; monitor services.

docker ps -a → Show all containers, including stopped; check lifecycle status.

docker logs <container> → View container logs; debug startup or runtime issues.

docker exec -it <container> sh → Enter running container shell; inspect or debug live apps.

docker stop <container> → Stop a running container; safely halt services.

docker rm <container> → Remove container; cleanup temporary instances.

docker build -t <name>:<tag> . → Build an image from Dockerfile; create reusable blueprint.

docker tag <image> <new-name>:<new-tag> → Rename or version image; prepare for registry push.

docker push <image> → Upload image to Docker Hub or private registry; deploy to production.

docker network ls → List Docker networks; inspect container communication.

docker network inspect <network> → View network details; debug container connectivity.

docker volume ls → List Docker volumes; inspect persistent storage.

docker volume inspect <volume> → View volume details; check mounted data paths.

docker container prune → Remove stopped containers; free system resources.

docker image prune → Remove dangling images; clean unused layers.

docker volume prune → Remove unused volumes; reclaim storage.

docker exec -it <container> node src/index.js → Run app manually inside container; debug runtime issues.

docker exec -it <container> env → View environment variables; verify config or secrets.

docker exec -it <container> ls -l → List files in container; confirm copied files or builds.

docker exec -it <container> cat <file> → Read container file content; inspect configs or logs.

docker exec -it <container> ps aux → List processes; monitor running services inside container.

docker exec -it <container> top → Live monitor CPU/memory; debug resource usage.

docker exec -it <container> pwd → Show current path inside container; verify WORKDIR.

docker exec -it <container> cd <path> → Change directory inside container; navigate project files.

docker exec -it <container> vi <file> → Edit file temporarily inside container; hotfix/testing.

docker exec -it <container> exit → Exit container shell; return to host safely.

---

🧠  Dev Notes

Images = blueprints; containers = running instances.

Always map ports (-p host:container) for host access.

Use -d for detached containers; -it for debugging or interactive sessions.

Prune regularly to save disk space (system prune, container prune, image prune).

Tag images explicitly (name:version) → production best practice.

Use docker exec mainly for debugging; permanent changes should go in Dockerfile.

Logs first (docker logs), exec second (docker exec) → debug hierarchy.

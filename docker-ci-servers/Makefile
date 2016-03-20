
gitlab-data:
	docker create \
	--name gitlab-data \
    --volume /Users/sandeepshinde/srv/gitlab/config:/etc/gitlab \
    --volume /Users/sandeepshinde/srv/gitlab/logs:/var/log/gitlab \
    --volume /Users/sandeepshinde/srv/gitlab/data:/var/opt/gitlab \
    gitlab/gitlab-ce:latest
    
gitlab:
	docker run --detach \
    --hostname gitlab.example.com \
    --publish 443:443 --publish 8082:80 --publish 2222:22 \
    --name gitlab \
    --restart always \
    --volumes-from gitlab-data \
    gitlab/gitlab-ce:latest
    
nexus:
	docker run -d -p 8081:8081 --name nexus sonatype/nexus:oss    
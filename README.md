# docker-gitlabrunner
gitlabrunner

>
https://hub.docker.com/r/gitlab/gitlab-runner/~/dockerfile/
https://docs.gitlab.com/runner/install/docker.html



## register 进入容器操作

- Run the following command: 

    
    sudo gitlab-runner register

- Enter your GitLab instance URL:  


    Please enter the gitlab-ci coordinator URL (e.g. https://gitlab.com )
    https://gitlab.test.com:10080

- Enter the token you obtained to register the Runner:
    
    
    Please enter the gitlab-ci token for this runner
    xxx

- Enter a description for the Runner, you can change this later in GitLab's UI:

    
    Please enter the gitlab-ci description for this runner
    [hostame] my-runner

- Enter the tags associated with the Runner, you can change this later in GitLab's UI:
    
    
    Please enter the gitlab-ci tags for this runner (comma separated):
    my-tag,another-tag
    
- Choose whether the Runner should pick up jobs that do not have tags, you can change this later in GitLab's UI (defaults to false):

...



## runner内使用docker

>
https://docs.gitlab.com/ce/ci/docker/using_docker_build.html

暂时定用下面这种

```
sudo gitlab-ci-multi-runner register -n \
  --url https://gitlab.com/ \
  --registration-token REGISTRATION_TOKEN \
  --executor docker \
  --description "My Docker Runner" \
  --docker-image "docker:latest" \
  --docker-volumes /var/run/docker.sock:/var/run/docker.sock
```

## 使用私有仓库镜像 配置个变量

>
http://gitlab.internal:10080/help/ci/docker/using_docker_images.md


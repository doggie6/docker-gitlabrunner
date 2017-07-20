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

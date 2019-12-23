#example pipeline using github and dockerhub


fly -t test login -c http://cicd:8080 -u admin -p 'admin123!@#'
fly -t test sync
fly -t test set-pipeline -c pipeline1.yaml --load-vars-from variables2.yaml -p ex1
fly -t test unpause-pipeline -p ex1

To delete:
fly -t test destroy-pipeline -p ex1


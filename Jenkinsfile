
pipeline{
    environment{
       dockerhub_registry=https://hub.docker.com/chytra
       dockerhub_credentials=chytra
              }
              
    //This is related to docker build
    
    Stages{
      Stage('Building the docker image'){
            Steps{
                app = docker.build("getintodevops/hellonode")
        
             }
          }
          
        Stage('Push the image'){
            Steps{
                docker.withRegistry("$dockerhub_registry", "$dockerhub_credentials") {
                app.push("${env.BUILD_NUMBER}")
                app.push("latest")
               }
        
             }
          }
    }
  
}

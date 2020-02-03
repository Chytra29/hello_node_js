
pipeline{
    environment{
       dockerhub_registry="https://hub.docker.com/chytra"
       dockerhub='chytra'
              }
              
    //This is related to docker build
    
    stages{
      stage('Building the docker image'){
            steps{
                app = docker.build("getintodevops/hellonode")
        
             }
          }
          
        stage('Push the image'){
            steps{
                docker.withRegistry("$dockerhub_registry", "$dockerhub") {
                app.push("${env.BUILD_NUMBER}")
                app.push("latest")
               }
        
             }
          }
    }
  
}

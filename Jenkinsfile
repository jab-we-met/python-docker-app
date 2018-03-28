node{
   stage("App Build started"){
      echo 'App build started..'
      git 'https://github.com/jab-we-met/python-docker-app.git'
      }
      
    stage("Docker Build"){
     def app = docker.build "mtanweer/cenovus1234"
     }
    
    stage("Tag & Push image"){
       withDockerRegistry([credentialsId: 'DockerID', url: 'https://hub.docker.com']) {
          sh 'docker tag jenkins-docker mtanweer/my_image:1.0'
          
         
      }
    }
    
    stage("App deployed"){
     echo 'App deployed to Hub..'
    }


}

node{

    stage('SCM Checkout')
    {
        git credentialsId: '4cc785e9-441d-4818-a248-2bfb2148004d', url: 'https://github.com/VardhanNS/phpmysql-app.git'
    }
    
    stage('Run Docker Compose File')
    {
        sh 'sudo docker-compose build'
        sh 'sudo docker-compose up -d'
    }
  stage('PUSH image to Docker Hub')
    {
      /* withCredentials([string(credentialsId: 'DockerHubPassword', variable: 'DHPWD')]) 
        {
            sh "docker login -u kolleyvenkatesh -p ${DHPWD}"
        }
        sh 'docker push kolleyvenkatesh/phpmysql_app'
        */
        //docker.withRegistry( 'https://registry.hub.docker.com', 'DockerHubPassword' ) {
             
             sh 'sudo docker login -u "kolleyvenkatesh" -p "Venkey@123" docker.io'
             //sh 'sudo docker push kolleyvenkatesh/mysql'
             //sh 'sudo docker push upasanatestdocker/job1_web1.0'
             sh 'sudo docker push kolleyvenkatesh/job1_web2.0'
            // sh 'docker push kolleyvenkatesh/mysql'
          
    }
}

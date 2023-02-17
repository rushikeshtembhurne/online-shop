node{

    stage('SCM Checkout')
    {
        git credentialsId: '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', url: 'https://github.com/rushikeshtembhurne/online-shop.git'
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
            sh "docker login -u upasanatestdocker -p ${DHPWD}"
        }
        sh 'docker push vardhanns/phpmysql_app'
        */
        //docker.withRegistry( 'https://registry.hub.docker.com', 'DockerHubPassword' ) {
             
             sh 'sudo docker login -u "rishi0921" -p "Rishi@123" docker.io'
             //sh 'sudo docker push upasanatestdocker/mysql'
             //sh 'sudo docker push upasanatestdocker/job1_web1.0'
             sh 'sudo docker push rishi0921/job1_web2.0'
            // sh 'docker push upasanatestdocker/mysql'
          
    }
}

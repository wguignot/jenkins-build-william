
node {

  
   def IMAGE="srv-web-william"
	
    stage('Clone') {
          checkout scm
    }

    stage('Build') {
          docker.build("$IMAGE",  '.')
    }

    stage('Run image') {
        docker.image('srv-web-william').withRun('--name srv_web-william' ) { c ->

        sh 'docker ps | grep srv_web-william'
	}

    }
}

node {
   //env.DOCKER_HOST="127.0.0.1"
   env.DOCKERD="/usr/local/bin/dockerd"
   env.DOCKER_OPTS="--dns 8.8.8.8 --dns 8.8.4.4"
   
   stage('Preparation') { // for display purposes
      git 'https://github.com/Vladilit/docker_course_votingapp.git'
   }
   stage('Build') {
      // Run the maven build
      sh 'cd Exercises/02.VotingSystem/ && export http_proxy="http://127.0.0.1:3128/" && docker-compose up'
   }
   stage('Results') {
      sh 'docker log 02votingsystem_voting.processor_1'
   }
}

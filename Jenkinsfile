node {
   stage('Preparation') { // for display purposes
      git 'https://github.com/Vladilit/docker_course_votingapp.git'
   }
   stage('Build') {
      // Run the maven build
      sh 'docker-compose up'
   }
   stage('Results') {
      sh 'docker log 02votingsystem_voting.processor_1'
   }
}
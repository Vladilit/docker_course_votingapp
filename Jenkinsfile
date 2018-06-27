node {
   stage('Preparation') { // for display purposes
      git 'https://github.com/Vladilit/docker_course_votingapp.git'
   }
   stage('Build') {
      // Run the maven build
      sh 'cd Exercises/02.VotingSystem/ && docker-compose up'
   }
   stage('Results') {
      sh 'docker log 02votingsystem_voting.processor_1'
   }
}

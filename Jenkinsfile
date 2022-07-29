node {
    
  stage 'Checkout'

  git 'https://github.com/Abhishek679/pythonnDockerJenkins.git'
        
  stage 'Package Docker image'

  def img = docker.build('abhishekd679/python-docker-jenkins:latest', '.')

  stage 'Publish'
  docker.withRegistry('https://localhost:5000') {
     img.push('latest')
  }

}

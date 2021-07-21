node {
  stage 'Checkout'
  git 'ssh://git@github.com:navepand/final_upgrad_project.git'
 
  stage 'Docker build'
  docker.build('test-node-app')
 
  stage 'Docker push'
  docker.withRegistry('https://126533046923.dkr.ecr.us-east-1.amazonaws.com/', 'ecr:us-east-1:nodeapp-ecr-credentials') {
    docker.image('test-node-app').push('latest')
  }
}
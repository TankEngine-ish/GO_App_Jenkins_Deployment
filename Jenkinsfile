pipeline {
    agent {
        node {
            label 'WSL_agent'
        }
    }
      tools {
        go '1.18.1'
      }

      environment {
        GO111MODULE = 'on'  // In this mode, the go command looks for the go.mod file in the project directory
                            // to determine the required dependencies and their versions.
      }

      stages {
        stage ('Test'){
            steps {
                git branch: 'main', url: 'https://github.com/TankEngine-ish/GO_App_Jenkins_Deployment'
                sh 'go test ./...'
            }
        }
        stage ('Build'){
            steps {
              
                  git branch: 'main', url: 'https://github.com/TankEngine-ish/GO_App_Jenkins_Deployment'
                    // app = docker.build("gojenkinsdeployment")
                    sh 'go build .'
                }
            }
        stage ('Run'){
            steps {
                    sh 'cd /var/lib/jenkins/workspace/go_full_pipeline && GO_App_Jenkins_Deployment &'
                }
            }
        }
    }


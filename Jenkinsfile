pipeline{
    agent any
    stages{
        stage('compile'){
            // when { branch 'main'} //rest will run
            steps {
                echo 'compile '
            }
        }
        stage('Test cases'){
            when{
                expression{ env.BRANCH_NAME != 'main'}
            }
             steps {
                echo 'test cases '
            }
        }
        stage('Docker build'){// run on tag
            when{
                not {
                    branch '**'
                }
                tag ''
            }
            steps {
                echo 'docker build '
            }
        }
        stage('Docker push'){
             when{
                not {
                    branch '**'
                }
                tag ''
            }
            steps {
                echo 'Docker push'
            }
        }
         stage('deploy to dev'){
             when{
                not {
                    branch '**'
                }
                tag ''
            }
            steps {
                echo 'deploy to dev'
            }
        }
       
    }
}
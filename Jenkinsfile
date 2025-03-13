pipeline{
    agent any
    stages{
        stage('compile'){
            when { branch 'main'}
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
        stage('Docker build'){
            when{
                expression{ env.BRANCH_NAME != 'main'}
            }
            steps {
                echo 'docker build '
            }
        }
        stage('Docker push'){
            when{
                expression{ env.BRANCH_NAME != 'main'}
            }
            steps {
                echo 'Docker push'
            }
        }
         stage('deploy to dev'){
            when{
                expression{ env.BRANCH_NAME != 'main'}
            }
            steps {
                echo 'deploy to dev'
            }
        }
       
    }
}
node(){ 

    if(env.TAG_NAME){
        stage('Docker build'){
            print 'Docker build'
        }
        stage('Docker Push'){
            print 'Docker push'
        }
        stage('Deploy to dev'){
            print 'Deploy to dev'
        }
    }else{
        stage('Compile'){
            print 'compile'
        }  
        stage('Test Case'){
            print 'Test case'
        }
    }
    
    
}
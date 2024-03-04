pipeline{
    agent any
    
    stages{
        
        stage("compile"){
           
           steps{ 
            sh 'echo "g++ -o program program.cpp"'
           }
        }
        stage("run"){
            steps{ 
            sh 'echo ".\\program.exe"'
           }
        }
    
    }
}
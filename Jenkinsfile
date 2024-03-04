// pipeline{
//     agent any
    
//     stages{
        
//         stage("compile"){
           
//            steps{ 
//             sh 'echo "g++ -o program program.cpp"'
//            }
//         }
//         stage("run"){
//             steps{ 
//             sh 'echo ".\\program.exe"'
//            }
//         }
    
//     }
// }
pipeline {
    agent any
    
    stages {
        stage('Checkout SCM') {
            steps {
                checkout scm
            }
        }
        stage('Compile') {
            steps {
                bat 'g++ -o program program.cpp' // for Windows
                // sh 'g++ -o program program.cpp' // for Unix-like systems
            }
        }
        stage('Run') {
            steps {
                bat '.\\program.exe' // for Windows
                // sh './program.exe > output.txt' // for Unix-like systems
                echo 'Output of program.exe:'
                bat 'type output.txt' // for Windows
                // sh 'cat output.txt' // for Unix-like systems
            }
        }
    }
}

pipeline {
    agent none 
    stages {
        stage('Build') { 
            agent {
                echo "This is a first application"
                }
            }
            steps {
                sh 'python -m py_compile sources/add2vals.py sources/calc.py' 
                stash(name: 'compiled-results', includes: 'sources/*.py*') 
            }
        }
    }
}

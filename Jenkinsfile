
pipeline {
    agent none

    stages {
        stage('Build Assets') {
            agent any

            steps {
                echo 'Building Assets...'
		sh 'python -m py_compile sources/add2vals.py sources/calc.py'
            }
        }
        stage('Post Build') {
            agent any

            steps {
                echo 'Transferring Assets...'
		sh 'cp -r ~/.jenkins/workspace/simple-python-pyinstaller-app/sources/ build'
            }
        }
        stage('Test') {
            agent any

            steps {
                echo 'Testing stuff...'
            }
        }
    }
}

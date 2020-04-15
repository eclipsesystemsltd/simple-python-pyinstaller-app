
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
		sh 'cp -r ~/.jenkins/workspace/simple-python-pyinstaller-app/sources/ ~/git/simple-python-pyinstaller-app/build'
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

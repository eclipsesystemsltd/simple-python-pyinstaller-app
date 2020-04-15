
pipeline {
    agent none

    stages {
        stage('Build Assets') {
            agent master

            steps {
                echo 'Building Assets...'
		sh 'python -m py_compile sources/add2vals.py sources/calc.py'
            }
        }
        stage('Post Build') {
            agent master

            steps {
                echo 'Transferring Assets...'
		sh 'cp -r ~/.jenkins/workspace/simple-python-pyinstaller-app/sources/ build'
            }
        }
        stage('Test') {
            agent master

            steps {
                echo 'Testing stuff...'
            }
        }
    }
}

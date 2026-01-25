@Library('jenkins-shared-library') _

pipeline {
    agent any

    stages {
        stage('Sync github repo') {
            when { branch 'master' }
            steps {
                syncRemoteBranch('git@github.com:nbr23/ansible-role-jacadi.git', 'master')
            }
        }
    }
}

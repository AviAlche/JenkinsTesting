def remote = [:]
remote.name = 'test'
remote.host = '10.10.168.2'
remote.user = 'root'
remote.password = 'sysdreamworks'
remote.allowAnyHosts = true

pipeline {
    agent any

    stages {
        stage('Push repo to automation vm') {
          steps {
            sh 'ls src'
            sh 'pwd'
            script {
                sshPut remote: remote, from: 'src/**', into: '/root/.'
            }
          }
        }
    }
}

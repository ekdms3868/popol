pipeline {
  agent any
  stages {
    stage('git scm update') {
      steps {
        git url: 'https://github.com/ekdms3868/popol.git', branch: 'main'
      }
    }

    stage('Setup Ansible') {
        steps {
            sh 'sudo apt update && sudo apt install -y ansible'
            }
        }

    stage('Run Ansible Playbook') {
        steps {
                // Ansible Playbook을 실행합니다.
                // 예: master 노드에 playbook.yml을 실행
            sh 'ansible-playbook -i /root/lab1 playbook.yml'
            }
        }
    }
  }
}
pipeline{
     agent any
     
     stages{
         
         stage("cretae clone of ansible deployment job")
         {
             steps{
             git branch: 'main', url: 'https://github.com/neerajcornhill/myansible.git'
             }
         }
         
         stage("excute the job")
         {
             steps{
                 ansiblePlaybook credentialsId: 'ansiuser1', disableHostKeyChecking: true, installation: 'myansible', inventory: 'dev.inv', playbook: 'playbook1.yml'
             }
         }
     }
}

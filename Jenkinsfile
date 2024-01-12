node {

 stage('clone git repo'){

 git 'https://github.com/YauheniyaH/PTE_Jmeter_task'

 }

 

 stage("configure") {

        sh "mkdir $WORKSPACE/$BUILD_NUMBER/"

    }

 

 stage('run test'){

 sh "mkdir /tmp/reports"

 sh "cd /Users/Yauheniya_Hladkaya/Trainings/apache-jmeter-5.6.2/bin"

      sh "jmeter -Jjmeter.save.saveservice.output_format=xml
          -n -t app//Users/Yauheniya_Hladkaya/Trainings/apache-jmeter-5.6.2/bin/test plans/JMeter.jmx
            -l /tmp/reports/JMeter.jtl -e -o /tmp/reports/HtmlReport"

 }

 

 stage('publish results'){

 sh "mv /tmp/reports/* $WORKSPACE/$BUILD_NUMBER/"

 archiveArtifacts artifacts: '$WORKSPACE/$BUILD_NUMBER/JMeter.jtl, $WORKSPACE/$BUILD_NUMBER/HtmlReport/index.html'

    } 

  }

}

node {

// stage('clone git repo'){

// git 'https://github.com/YauheniyaH/PTE_Jmeter_task.git'

// }

 

 stage('configure') {

        sh "mkdir $WORKSPACE/$BUILD_NUMBER/"

    }

 

 stage('run test'){
  
 sh "rm /tmp/newReports"
 sh "mkdir /tmp/newReports"

 sh "cd /Users/Yauheniya_Hladkaya/Trainings/apache-jmeter-5.6.2/bin"

      sh """/Users/Yauheniya_Hladkaya/Trainings/apache-jmeter-5.6.2/bin/jmeter -Jjmeter.save.saveservice.output_format=xml
          -n -t "/Users/Yauheniya_Hladkaya/Trainings/apache-jmeter-5.6.2/bin/test_plans/Jmeter task 01/Jmeter task 01 copy 03.jmx"
            -l /tmp/reports/JMeter.jtl -e -o /tmp/reports/HtmlReport"""

 }

 

 stage('publish results'){

 sh "mv /tmp/reports/* $WORKSPACE/$BUILD_NUMBER/"

 archiveArtifacts artifacts: '$WORKSPACE/$BUILD_NUMBER/JMeter.jtl, $WORKSPACE/$BUILD_NUMBER/HtmlReport/index.html'

    } 


}

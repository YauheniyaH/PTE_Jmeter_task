node {

// stage('clone git repo'){

// git 'https://github.com/YauheniyaH/PTE_Jmeter_task.git'

// }

 

 stage('configure') {

        sh 'mkdir $WORKSPACE/$BUILD_NUMBER/'

    }

 

 stage('run test'){
  
 //sh "rmdir /temp/reports"
 sh "mkdir /temp/reports"

 sh "cd /Users/Yauheniya_Hladkaya/Trainings/apache-jmeter-5.6.2/bin"

      sh """/Users/Yauheniya_Hladkaya/Trainings/apache-jmeter-5.6.2/bin/jmeter -n -t "/Users/Yauheniya_Hladkaya/Trainings/apache-jmeter-5.6.2/bin/test_plans/Jmeter task 01/Jmeter task 01 copy 03.jmx" -l /temp/reports/JMeter.jtl -e -o /temp/reports/HtmlReport"""

 }

 

// stage('publish results'){

// sh "mv /temp/reports/* $WORKSPACE/$BUILD_NUMBER/"

// archiveArtifacts artifacts: '$WORKSPACE/$BUILD_NUMBER/JMeter.jtl, $WORKSPACE/$BUILD_NUMBER/HtmlReport/index.html'

//    } 


}

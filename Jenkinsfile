// comment
pipeline {
 agent any
 stages {
    stage('Checkout-Proyecto'){     
    	 steps{
            echo 'Revisando repositorio del Proyecto'
			git branch: 'master', poll: true, url: 'https://github.com/edeleon2408/enrolamiento-api.git'
         }        	
    }
    stage('Clean-Install-Packages'){     
    	 steps{
            echo 'Limpiando e Instalando paquetes del Proyecto'
	   }        	
    }
    stage('Build-Proyecto'){     
    	 steps{
            echo 'Check Codigo en SCA'
			
	   }        	
    }
    stage('Check-SCA-Proyecto'){     
    	 steps{
            echo 'Check Codigo en SCA del Proyecto'
					
	   }        	
    }
    stage('Testing Proyecto'){     
    	 steps{
            echo 'Realizando Testin del Proyecto'	
            
	   }        	
    }//fin stage
    
  }//fin stages
  
  post {
        success {
            echo 'I will success!'
            //mail bcc: '', 
            //body: "<b>Notificación CI</b><br><br>Estimado Usuario, El proceso CI se ha ejecutado de manera satisfactoria.<br><br>Project: ${env.JOB_NAME} <br>Build Number: ${env.BUILD_NUMBER} <br> URL de build: ${env.BUILD_URL}",
            //cc: '', 
            //charset: 'UTF-8', 
            //from: '', 
            //mimeType: 'text/html', 
            //replyTo: '', 
            //subject: "SUCCESS CI: Project name -> ${env.JOB_NAME}", 
            //to: "edeleon2408@gmail.com";  
                     
        }
        failure {
        	echo 'I will failure!'
            //mail bcc: '', 
            //body: "<b>Notificación CI</b><br><br>Estimado Usuario, El proceso CI ha fallado, por favor notificar al area administrativa del proceso.<br><br>Project: ${env.JOB_NAME} <br>Build Number: ${env.BUILD_NUMBER} <br> URL de build: ${env.BUILD_URL}",
            //cc: '', 
            //charset: 'UTF-8', 
            //from: '', 
            //mimeType: 'text/html', 
            //replyTo: '', 
            //subject: "FAILURED CI: Project name -> ${env.JOB_NAME}", 
            //to: "edeleon2408@gmail.com";
        }
    }//fin post
}

pipeline {
      agent {
             node { label "built-in"
				        customWorkspace "/mnt/22q3"
					 }
        }
		stages {
		
			stage ("22Q1"){
			
				steps {
		     
		    sh " rm -rf * "
                    sh "git clone https://github.com/Rohit0698/master-dev-qa-22q1-22q2-22q3.git"
	            sh " docker run -itdp 81-85:80 --name testqa httpd "
	            sh " chmod -R 777 /mnt/22q3 "
		    sh " docker cp /mnt/22q3/master-dev-qa-22q1-22q2-22q3/index.html testqa:/usr/local/apache2/htdocs "
                    
                    
				}
			}
		}
}

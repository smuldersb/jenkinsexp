stage 'checkout'
	

	node {
	    checkout scm
	}
	

	stage 'build'
	

	node {
	    echo 'building'
	}
	

	stage 'test'
	

	parallel ( 
	    test1: {
	        node {
	            echo 'performing test 1'
emailext body: 'test 1 successful', recipientProviders: [[$class: 'RequesterRecipientProvider'], [$class: 'UpstreamComitterRecipientProvider']], subject: 'test result', to: 'recv@mailhog'
	        }
	    }, test2: {
	        node {
	            echo 'performing test 2'
emailext body: 'test 2 successful', recipientProviders: [[$class: 'RequesterRecipientProvider'], [$class: 'UpstreamComitterRecipientProvider']], subject: 'test result', to: 'recv@mailhog'
	        }
	    }, test3: {
	        node {
	            echo 'performing test 3'
emailext body: 'test 3 successful', recipientProviders: [[$class: 'RequesterRecipientProvider'], [$class: 'UpstreamComitterRecipientProvider']], subject: 'test result', to: 'recv@mailhog'
	        }
	    }
	)
	

	stage 'deploy'
	node {
	    echo 'here is your app'
	}
	


stage 'checkout'

node {
    checkout scm
}

stage 'build'

node {
    echo 'building'
}

stage 'test'

node {
    echo 'testing'

}

emailext body: 'this is done', recipientProviders: [[$class: 'RequesterRecipientProvider'], [$class: 'UpstreamComitterRecipientProvider']], subject: 'build done', to: 'recv@mailhog'

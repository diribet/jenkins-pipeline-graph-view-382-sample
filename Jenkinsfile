import groovy.transform.Field

@Field def utils = null
@Field def utilsInStage = null

node() {
    stage("Prepare") {
        checkout scm
    }

    utils = load("utils.groovy")

    stage("Load libs") {
        utilsInStage = load("utilsInStage.groovy")
    }

    stage("Test") {
        utils.printInfo("Running tests")
        utilsInStage.printInfo("Running tests")
    }
}

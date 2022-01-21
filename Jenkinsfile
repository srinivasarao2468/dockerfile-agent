pipeline {
  agent {
      // Equivalent to "docker build -f Dockerfile.build --build-arg version=1.0.2 ./build/
      dockerfile {
          filename 'Dockerfile.build'
          dir 'build'
          additionalBuildArgs  '--build-arg version=1.0.2'
          args '-v /tmp:/tmp'
      }
  }
  stages{
      stage("abc"){
          steps {
                sh 'node --version'
                sh 'git --version'
          }
      }
  }
}

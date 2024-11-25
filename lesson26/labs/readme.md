# Lab Title

### Lab 1 Hello Bash

```bash
echo "Hello, World!"
```

### Lab 2 Hello Stage

```bash
node {
    stage('Hello') {

        echo 'Hello World'

    }
}
```

## Lab 3 Stage

```bash
pipeline {
agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
    }
}
```

## Lab 4 Steps

```bash
pipeline {
agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }

}
```

## Lab 5 Build

```bash
pipeline {
agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building a new laptop ...'
                sh 'mkdir -p build'
                sh 'touch build/computer.txt'
                sh 'echo "Main Board" >> build/computer.txt'
                sh 'cat build/computer.txt'
                sh 'echo "Display" >> build/computer.txt'
                sh 'cat build/computer.txt'
                sh 'echo "Keyboard" >> build/computer.txt'
                sh 'cat build/computer.txt'
            }
        }
    }
}
```

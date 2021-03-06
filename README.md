Installing Jenkins
To update Ubuntu with Jenkins source lists, type in the following commands:
```bash
sudo wget -q -O - http://pkg.jenkins-ci.org/debian/jenkins-ci.org.key | sudo apt-key add -

sudo sh -c 'echo deb http://pkg.jenkins-ci.org/debian binary/ > /etc/apt/sources.list.d/jenkins.list'

sudo apt-get update

sudo apt-get install jenkins
```

On Mac, simply run:
```
brew install jenkins
```

Then, visit your server using port 8080, e.g. http://jenkins.lookahead.io:8080, and you should see the Jenkins startup screen:
You installed Jenkins on a Debian-based or a Fedora-based distribution, you can use the following commands:

```bash
sudo service jenkins restart

sudo service jenkins stop

sudo service jenkins start
```

To Unlock

```bash
sudo vi /var/lib/jenkins/config.xml
```

Turn security off and remove the \<authorizationStrategy> node

\<useSecurity>false\</useSecurity>

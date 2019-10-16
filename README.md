## make a sonar qube environment with docker
* download [docker-compose.yml](https://github.com/kazumaz/sonar-qube/blob/master/docker-compose.yml) and put it to your own directory

2.execute command `docker-compose up`

3.access [your local sonar qube](http://localhost:9000/) 

## scan your code
1.add build.gradle.kts following code

```
plugins {
	id("org.springframework.boot") version "2.1.8.RELEASE"
	id("io.spring.dependency-management") version "1.0.8.RELEASE"
	kotlin("jvm") version "1.2.71"
	kotlin("plugin.spring") version "1.2.71"
	id("org.sonarqube").version("2.8")  ★★★ add this!!!
}
```
see [latest version](https://plugins.gradle.org/plugin/org.sonarqube)

2.add gradle-wrapper.properties  folowing code
```
systemProp.sonar.host.url=http://localhost:9000
```
3.execute command `./gradlew clean sonarqube`

4.access [your local sonar qube](http://localhost:9000/) and check the result
 
<img width="1389" alt="スクリーンショット 2019-10-14 13 18 41" src="https://user-images.githubusercontent.com/17084684/66729274-4bb93200-ee85-11e9-8b61-85b9db46aec9.png">

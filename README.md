# make a sonar qube environment with docker
1)download docker-compose.yml file
2)docker-compose up
3)access [http://localhost:9000/] if you don't change port number

# Scan your code
1)add build.gradle.kts following code
```
plugins {
	id("org.springframework.boot") version "2.1.8.RELEASE"
	id("io.spring.dependency-management") version "1.0.8.RELEASE"
	kotlin("jvm") version "1.2.71"
	kotlin("plugin.spring") version "1.2.71"
	id("org.sonarqube").version("2.8")  ★★★ add this!!!
}
```
2)add gradle-wrapper.properties  folowing code
```
systemProp.sonar.host.url=http://localhost:9000
```
3)

<img width="1389" alt="スクリーンショット 2019-10-14 13 18 41" src="https://user-images.githubusercontent.com/17084684/66729274-4bb93200-ee85-11e9-8b61-85b9db46aec9.png">

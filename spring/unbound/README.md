# Unbound

## To Run on Eclipse
1. go to Run-> Run configuration -> Maven Build -> New configuration
2. set base directory of you project ie.${project_loc:unbound}
3. set goal spring-boot:run
4. Run project from Run-> New_Configuration 

## Failed to configure a DataSource: 'url' attribute is not specified and no embedded datasource could be configured.
1. @SpringBootApplication(exclude = {DataSourceAutoConfiguration.class })

## build executable jar with another typical jar
<plugin>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-maven-plugin</artifactId>
	<executions>
		<execution>
			<goals>
				<goal>repackage</goal>
			</goals>
			<configuration>
				<classifier>exec</classifier>
			</configuration>
		</execution>
	</executions>
</plugin>
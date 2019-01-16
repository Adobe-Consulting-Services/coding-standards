# Adobe Consulting Services Coding Standards

This git repository houses various coding standard configuration files used by Adobe Consulting Services.

## Usage

Add [this repo](http://repo.adobe.com/) and then...

### PMD

	<plugin>
	    <groupId>org.apache.maven.plugins</groupId>
	    <artifactId>maven-pmd-plugin</artifactId>
	    <version>3.0.1</version>
	    <configuration>
	        <rulesets>
	            <ruleset>acs/pmd/rules.xml</ruleset>
	        </rulesets>
	    </configuration>
	    <dependencies>
	        <dependency>
	            <groupId>com.adobe.acs</groupId>
	            <artifactId>coding-standards</artifactId>
	            <version>0.0.1</version>
	        </dependency>
	    </dependencies>
	</plugin>

### Checkstyle

	<plugin>
	    <groupId>org.apache.maven.plugins</groupId>
	    <artifactId>maven-checkstyle-plugin</artifactId>
	    <version>2.10</version>
	    <configuration>
	        <configLocation>acs/checkstyle/checks.xml</configLocation>
	    </configuration>
        <dependencies>
            <dependency>
                <groupId>com.adobe.acs</groupId>
                <artifactId>coding-standards</artifactId>
                <version>0.0.1</version>
            </dependency>
            <dependency>
                <groupId>com.adobe.acs</groupId>
                <artifactId>checkstyle-osgi-checks</artifactId>
                <version>0.0.3</version>
            </dependency>
        </dependencies>
	</plugin>

#### Eclipse Users

The URL above won't import into Eclipse Checkstyle plugin due to the use of custom modules. Use [https://raw.github.com/Adobe-Consulting-Services/coding-standards/master/checkstyle/checks-eclipse.xml](https://raw.github.com/Adobe-Consulting-Services/coding-standards/master/checkstyle/checks-eclipse.xml) instead

# Adobe Consulting Services Coding Standards

This git repository houses various coding standard configuration files used by Adobe Consulting Services.

## Usage

### PMD

	<plugin>
	    <groupId>org.apache.maven.plugins</groupId>
	    <artifactId>maven-pmd-plugin</artifactId>
	    <version>3.0.1</version>
	    <configuration>
	        <rulesets>
	            <ruleset>https://raw.github.com/Adobe-Consulting-Services/coding-standards/master/pmd/rules.xml</ruleset>
	        </rulesets>
	    </configuration>
	</plugin>

### Checkstyle

Add [this repo](https://github.com/Adobe-Consulting-Services/maven-repo) and then...

	<plugin>
	    <groupId>org.apache.maven.plugins</groupId>
	    <artifactId>maven-checkstyle-plugin</artifactId>
	    <version>2.10</version>
	    <configuration>
	        <configLocation>https://raw.github.com/Adobe-Consulting-Services/coding-standards/master/checkstyle/checks.xml</configLocation>
	    </configuration>
        <dependencies>
            <dependency>
                <groupId>com.adobe.acs</groupId>
                <artifactId>checkstyle-osgi-checks</artifactId>
                <version>0.0.2</version>
            </dependency>
        </dependencies>
	</plugin>

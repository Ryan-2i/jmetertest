To run your newly generated testing framework use: 
mvn clean verify -Denvironment=default 
Environment config is setup in serenity.conf, the sample tests use the default env config.

To run specific tests using a cucumber tags use cucumber filtering, for example:
mvn clean verify -Dcucumber.filter.tags="@UITest" -Denvironment=default

*Jmeter performance testing*
- Create a .jmx file using the Jmeter GUI for testing
- Drop the file into the src/test/java/jmeter/jmx directory
- Specify your volumetrics & .jmx file name in the JmeterPerformanceTest.feature file
- Run: mvn clean verify -Dcucumber.filter.tags="@Jmeter" -Denvironment=default
- The output of your performance test will be stored in the src/test/resources/jmeter/outputs directory (this will be date/time stamped to differentiate runs)
- Open the index.html file from this folder in your browser to analyse the performance testing run results

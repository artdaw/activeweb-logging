# ActiveWeb Logging package #

### Installation ###

1. add dependency to your `pom.xml`:

		<dependency>
			<groupId>org.javalite</groupId>
			<artifactId>activeweb-logging</artifactId>
			<version>1.0-SNAPSHOT</version>
		</dependency>

2. add repository where activeweb-logging is placed:

		<repository>
			<id>artdaw-snapshots</id>
			<url>https://github.com/artdaw/m2/raw/master/snapshots</url>
		</repository>

3. in your Guice module bind `LoggerTypeListener`:

		bindListener(Matchers.any(), new LoggerTypeListener());

4. Profit! Use @InjectLogger as follows:

		@InjectLogger
		private static Logger logger;
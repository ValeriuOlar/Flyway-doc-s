## Oracle Flyway Configuration 

- The most up to date Flyway Comunity Version is 5.1.4

[Flyway Comunity Version](https://repo1.maven.org/maven2/org/flywaydb/flyway-commandline/5.1.4/)



### 👷‍ Installation

In order to conect to Flyway CLI you need to add in flyway.config your database candentials.




```
flyway.url=jdbc:oracle:thin:@ech-10-157-150-221.mastercard.int:1527:devcloud
flyway.user= devadmin
flyway.password= Zse45tgb

```




### 🤖 To run Flyway:


Usage
=====

flyway [options] command

By default, the configuration will be read from conf/flyway.conf.
Options passed from the command-line override the configuration.

### 💻 Commands
--------
migrate  : Migrates the database
clean    : Drops all objects in the configured schemas
info     : Prints the information about applied, current and pending migrations
validate : Validates the applied migrations against the ones on the classpath
undo     : [pro] Undoes the most recently applied versioned migration
baseline : Baselines an existing database at the baselineVersion
repair   : Repairs the schema history table

### ⚫️ Options (Format: -key=value)
-------
driver                       : Fully qualified classname of the JDBC driver
url                          : Jdbc url to use to connect to the database
user                         : User to use to connect to the database
password                     : Password to use to connect to the database
schemas                      : Comma-separated list of the schemas managed by Flyway
table                        : Name of Flyway's schema history table
locations                    : Classpath locations to scan recursively for migrations
resolvers                    : Comma-separated list of custom MigrationResolvers
skipDefaultResolvers         : Skips default resolvers (jdbc, sql and Spring-jdbc)
sqlMigrationPrefix           : File name prefix for versioned SQL migrations
undoSqlMigrationPrefix       : [pro] File name prefix for undo SQL migrations
repeatableSqlMigrationPrefix : File name prefix for repeatable SQL migrations
sqlMigrationSeparator        : File name separator for SQL migrations
sqlMigrationSuffixes         : Comma-separated list of file name suffixes for SQL migrations
stream                       : [pro] Stream SQL migrations when executing them
batch                        : [pro] Batch SQL statements when executing them
mixed                        : Allow mixing transactional and non-transactional statements
encoding                     : Encoding of SQL migrations
placeholderReplacement       : Whether placeholders should be replaced
placeholders                 : Placeholders to replace in sql migrations
placeholderPrefix            : Prefix of every placeholder
placeholderSuffix            : Suffix of every placeholder
installedBy                  : Username that will be recorded in the schema history table
target                       : Target version up to which Flyway should use migrations
outOfOrder                   : Allows migrations to be run "out of order"
callbacks                    : Comma-separated list of FlywayCallback classes
skipDefaultCallbacks         : Skips default callbacks (sql)
validateOnMigrate            : Validate when running migrate
ignoreMissingMigrations      : Allow missing migrations when validating
ignoreIgnoredMigrations      : Allow ignored migrations when validating
ignoreFutureMigrations       : Allow future migrations when validating
cleanOnValidationError       : Automatically clean on a validation error
cleanDisabled                : Whether to disable clean
baselineVersion              : Version to tag schema with when executing baseline
baselineDescription          : Description to tag schema with when executing baseline
baselineOnMigrate            : Baseline on migrate against uninitialized non-empty schema
configFiles                  : Comma-separated list of config files to use
configFileEncoding           : Encoding to use when loading the config files
jarDirs                      : Comma-separated list of dirs for Jdbc drivers & Java migrations
dryRunOutput                 : [pro] File where to output the SQL statements of a migration dry run
errorHandlers                : [pro] Comma-separated list of handlers for errors and warnings
oracle.sqlplus               : [pro] Oracle SQL*Plus command support

Flags
-----
-X : Print debug output
-q : Suppress all output, except for errors and warnings
-n : Suppress prompting for a user and password
-v : Print the Flyway version and exit
-? : Print this usage info and exit

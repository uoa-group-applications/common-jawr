common-jawr
===========

The purpose of common-jawr is to provide a classpath scanner for configuration files for JAWR. The scanner will look for files that match the pattern


    jawr-*.properties

When the file is in a jar or war, the file must be non-zero in size. When in a directory, it cane be zero size as the only time this happens is in dev mode.
When in dev mode (indicated by the environment variable that is set by common-scanner), every time JAWR asks if files have changed it will check date stamps
on files and reload all the properties if one of them has changed. It will not attempt to do this for files taken from WAR or JAR files.

It provides a web fragment, so simply including it will expose /css/* and /js/* to JAWR.
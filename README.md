JavaServiceProviderInterfaceDemo
================================

Simple Demos for Java's SPI(Service Provider Interface) and java.util.ServiceLoader usage.

### Introduction

This demo app include 6 tiny jar projects.

1. CloudService
  * Demonstrates pseudo "Cloud Service" providers.
  * Defines `spidemo.cloud.spi.Cloud` interface for service provider.
  * Provides `spidemo.cloud.CloudService` utility class to wrap `java.util.ServiceLoader<Cloud>` operations.
2. SearchService
  * Demonstrates pseudo "Keyword Search Service" providers.
  * Defines `spidemo.search.spi.Search` interface for service provider.
  * Provides `spidemo.search.SearchService` utility class to wrap `java.util.ServiceLoader<Search>` operations.
3. FooProvider
  * Implementations for CloudService and SearchService.
4. BarProvider
  * Includes two implementations for SearchService.
5. BazProvider
  * Implementation for CloudService.
6. DemoApp
  * client app for CloudService and SearchService.

### Requirements
* JDK 1.6 or over
* Ant 1.8.x or over

### Build and Run

Run default Ant target.

```
$ ant
run:
     [java] Provider Name: Foo Cloud Provider
     [java] Foo VPC
     [java] Foo VPN
     [java] Foo Shared Server
     [java] Foo Dedicated Server
     [java] Provider Name: Baz Cloud Provider
     [java] Baz Xen Computing
     [java] Baz Security Gateway
     [java] Baz Shared Storage
     [java] Provider Name: Foo Search Provider
     [java] Foo Search 1
     [java] Foo Search 2
     [java] Foo Search 3
     [java] Provider Name: Bar Search Provider
     [java] Bar Search 1
     [java] Bar Search 2
     [java] Bar Search 3
     [java] Provider Name: Bar Search2 Provider
     [java] Bar2 Search 1
     [java] Bar2 Search 2
     [java] Bar2 Search 3

BUILD SUCCESSFUL
Total time: 12 seconds
```

### References

* Introduction to the Service Provider Interfaces (The Java™ Tutorials > Sound)
  * https://docs.oracle.com/javase/tutorial/sound/SPI-intro.html
* Creating Extensible Applications (The Java™ Tutorials > The Extension Mechanism > Creating and Using Extensions)
  * https://docs.oracle.com/javase/tutorial/ext/basics/spi.html
* ServiceLoader (Java Platform SE 7 )
  * https://docs.oracle.com/javase/7/docs/api/java/util/ServiceLoader.html

(Japanese Language)

* ServiceLoader (Java Platform SE 7 )
  * https://docs.oracle.com/javase/jp/7/api/java/util/ServiceLoader.html
* Jarファイルメモ(Hishidama's java-archive Memo)
  * http://www.ne.jp/asahi/hishidama/home/tech/java/jar.html#h_Service_Provider



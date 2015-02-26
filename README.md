# Jenkins JCache plugin
This plugin provides basis for plugins implemnting [JSR 107](https://jcp.org/en/jsr/detail?id=107) (Java Temporary Caching API).


Currently plugin defines abtract method `getCacheManager()`, which provides access to `javax.cache.CacheManager`. 
Plugins extending JCache plugin has to implement this method and return actual instance of `CacheManager` provided by some 
implementation of JSR 107 like [Infinispan](http://infinispan.org/). 


To extends this plugin or depend on it in any other way, add following dependency to your plugin:
```
<dependency>
	<groupId>org.jenkins-ci.plugins</groupId>
	<artifactId>jcache</artifactId>
	<version>${version.org.jenkins-ci.plugins.jcache}</version>
</dependency>
```
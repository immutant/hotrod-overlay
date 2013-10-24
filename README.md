
JBoss modules/config required to use an Immutant cluster as a Datomic data store

Requirements:

- An incremental release newer than Immutant 1.0.2
- lein-immutant 1.1.0 or higher

To install:

    $ lein immutant overlay hotrod

*WARNING*: Immutant 1.0.x includes Infinispan 5.3.0, which has a bug
preventing the durability of any data cached via Hotrod. The fix
requires an upgrade to Infinispan 6.0.0, the modules of which are
completely incompatible with any version of Immutant containing
Infinispan 5.3.0. Incremental releases of Immutant since 1.0.2 have
been upgraded to Infinispan 6.0.0.

For best results:

    $ lein immutant install LATEST
    $ lein immutant overlay hotrod

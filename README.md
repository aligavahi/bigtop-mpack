# bigtop-mpack
This was forked from @guyuqi who created all of this.  It was forked so I could make changes to start making forward progress.

Please put 'bgtp-ambari-mpack' in the path: $Ambari_Source/contrib/management-packs

To build:

```git clone https://github.com/mattAndruff/bigtop-mpack.git
cd bigtop-mpack/bgtp-ambari-mpack/
mvn clean package -DskipTests # mpack will now be located in the ./target/```

To Install into ambari:  (on the Ambari server run)

```sudo ambari-server stop
sudo ambari-server install-mpack --mpack=./target/bgtp-ambari-mpack-1.0.0.0-SNAPSHOT-bgtp-ambari-mpack.tar.gz
sudo ambari-server start```

Troubleshooting:

Read the ambari server logs located: `/var/log/ambari-server/ambari-server.log`

```#usefule commands:

sudo ambari-server install-mpack --mpack=./target/bgtp-ambari-mpack-1.0.0.0-SNAPSHOT-bgtp-ambari-mpack.tar.gz --purge # will delete previously installed mpacks only use it if you want to delete prevoiusly installed mpacks

sudo ambari-server reset # --> will reset ambari back to "new install"  only use if you mean it. It will delete *ALL* config.
```



<!-- THIS FILE IS GENERATED VIA '.template-helpers/generate-tag-details.pl' -->

# Tags of `kibana`

-	[`kibana:4.0.3`](#kibana403)
-	[`kibana:4.0`](#kibana40)
-	[`kibana:4.1.8`](#kibana418)
-	[`kibana:4.1`](#kibana41)
-	[`kibana:4.2.2`](#kibana422)
-	[`kibana:4.2`](#kibana42)
-	[`kibana:4.3.3`](#kibana433)
-	[`kibana:4.3`](#kibana43)
-	[`kibana:4.4.2`](#kibana442)
-	[`kibana:4.4`](#kibana44)
-	[`kibana:4.5.1`](#kibana451)
-	[`kibana:4.5`](#kibana45)
-	[`kibana:4`](#kibana4)
-	[`kibana:latest`](#kibanalatest)
-	[`kibana:5.0.0-alpha3`](#kibana500-alpha3)
-	[`kibana:5.0.0`](#kibana500)
-	[`kibana:5.0`](#kibana50)
-	[`kibana:5`](#kibana5)

## `kibana:4.0.3`

```console
$ docker pull library/kibana@sha256:cec1aaa0e3fc3d21d397805e44dcb06413387c52b7a7f0b8b2fd4c9d17b73076
```

-	Total v2 Content-Length: 83.2 MB (83235622 bytes)

### Layers (16)

#### `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`

```dockerfile
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
```

-	Created: Mon, 23 May 2016 22:57:20 GMT
-	v2 Blob: `sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`
-	v2 Content-Length: 51.4 MB (51356334 bytes)
-	v2 Last-Modified: Mon, 23 May 2016 23:09:48 GMT

#### `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Mon, 23 May 2016 22:57:23 GMT
-	Parent Layer: `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`

```dockerfile
RUN groupadd -r kibana && useradd -r -m -g kibana kibana
```

-	Created: Tue, 24 May 2016 02:15:27 GMT
-	Parent Layer: `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`
-	v2 Blob: `sha256:ef236d3c18b4ce0744c2ae4b8ae7f442605c745fd7b10c65b441ed51682b2c5f`
-	v2 Content-Length: 4.3 KB (4342 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:56 GMT

#### `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`

```dockerfile
RUN apt-get update && apt-get install -y 		ca-certificates 		wget 	--no-install-recommends && rm -rf /var/lib/apt/lists/*
```

-	Created: Tue, 24 May 2016 02:16:12 GMT
-	Parent Layer: `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`
-	v2 Blob: `sha256:7b4763c5420742eed897623fc3fc72c5a54f1245ee6d50734ca70a012f60a753`
-	v2 Content-Length: 16.6 MB (16615966 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:53 GMT

#### `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`

```dockerfile
ENV GOSU_VERSION=1.7
```

-	Created: Tue, 24 May 2016 02:16:15 GMT
-	Parent Layer: `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
```

-	Created: Tue, 24 May 2016 02:16:21 GMT
-	Parent Layer: `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`
-	v2 Blob: `sha256:8d4b6aaf60cb73053140071b6910c2697c581367449734e64959c86f2619d14f`
-	v2 Content-Length: 807.9 KB (807931 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:43 GMT

#### `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`

```dockerfile
ENV TINI_VERSION=v0.9.0
```

-	Created: Tue, 24 May 2016 02:16:23 GMT
-	Parent Layer: `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
```

-	Created: Tue, 24 May 2016 02:16:29 GMT
-	Parent Layer: `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`
-	v2 Blob: `sha256:a69ada16019ca97e3e09836f89b4fa99cf84902554f4df7857bd852a372a7417`
-	v2 Content-Length: 7.1 KB (7121 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:38 GMT

#### `c60aadc6a8b1c3db9fd09647b98af430f086d744d36cb786625ad77d1cada73a`

```dockerfile
ENV KIBANA_VERSION=4.0.3
```

-	Created: Tue, 24 May 2016 02:16:30 GMT
-	Parent Layer: `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `5f78175f5346d0a69ac63a833747df3cc7443c04a9c282145c0eebf4193ffa0a`

```dockerfile
ENV KIBANA_SHA1=75312e930466430167a7e01be3ae41aeaf01a26c
```

-	Created: Tue, 24 May 2016 02:16:31 GMT
-	Parent Layer: `c60aadc6a8b1c3db9fd09647b98af430f086d744d36cb786625ad77d1cada73a`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `a944edf45be17199542a6bacb8e9ba12a30940fda18712453270d72cd09cc4d9`

```dockerfile
RUN set -x 	&& wget -O kibana.tar.gz "https://download.elastic.co/kibana/kibana/kibana-${KIBANA_VERSION}-linux-x64.tar.gz" 	&& echo "${KIBANA_SHA1} *kibana.tar.gz" | sha1sum -c - 	&& mkdir -p /opt/kibana 	&& tar -xz --strip-components=1 -C /opt/kibana -f kibana.tar.gz 	&& chown -R kibana:kibana /opt/kibana 	&& rm kibana.tar.gz 		&& sed -ri "s!^(\#\s*)?(elasticsearch_url:).*!\2 'http://elasticsearch:9200'!" /opt/kibana/config/kibana.yml 	&& grep -q 'elasticsearch:9200' /opt/kibana/config/kibana.yml
```

-	Created: Tue, 24 May 2016 02:16:36 GMT
-	Parent Layer: `5f78175f5346d0a69ac63a833747df3cc7443c04a9c282145c0eebf4193ffa0a`
-	v2 Blob: `sha256:bf2516f9db2cc1b3138d553147b868a123e02683cb2f4e4e75e9869a3f2ae25d`
-	v2 Content-Length: 14.4 MB (14443298 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:28 GMT

#### `37cc14da24cbfee494124daa4d51533f6b64b2756a772b8324363bfbf37f6315`

```dockerfile
ENV PATH=/opt/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Created: Tue, 24 May 2016 02:16:46 GMT
-	Parent Layer: `a944edf45be17199542a6bacb8e9ba12a30940fda18712453270d72cd09cc4d9`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `473c4d74355c0e42bf336d2c4a12c39bb1f8288b148b6bb56c059abbf8d4829d`

```dockerfile
COPY file:bcaeac8c6bbd37e21bd6b91328c8390bf48cb8f8b62b7397258d943664deeba1 in /
```

-	Created: Tue, 24 May 2016 02:16:47 GMT
-	Parent Layer: `37cc14da24cbfee494124daa4d51533f6b64b2756a772b8324363bfbf37f6315`
-	v2 Blob: `sha256:7a2dc2187be63c58e3d9c3e2cec03f1b79ca5af72b1bf9602a71a9c43e4122ed`
-	v2 Content-Length: 342.0 B
-	v2 Last-Modified: Thu, 12 May 2016 19:36:15 GMT

#### `068639fe615edea1eb89fb7771a7ee01105bcb5b836e79cd79350eab30749f30`

```dockerfile
EXPOSE 5601/tcp
```

-	Created: Tue, 24 May 2016 02:16:48 GMT
-	Parent Layer: `473c4d74355c0e42bf336d2c4a12c39bb1f8288b148b6bb56c059abbf8d4829d`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `24d6d5ae2f1f9b2b8fe0ab5966e8080b1c1f05bb6ea47f39e1073343d87e27a4`

```dockerfile
ENTRYPOINT &{["/docker-entrypoint.sh"]}
```

-	Created: Tue, 24 May 2016 02:16:49 GMT
-	Parent Layer: `068639fe615edea1eb89fb7771a7ee01105bcb5b836e79cd79350eab30749f30`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `a63e24a31b0ad9c32d45115c12175ddcfcad6cbc2cda30bc2b194dba8c1a05f6`

```dockerfile
CMD ["kibana"]
```

-	Created: Tue, 24 May 2016 02:16:50 GMT
-	Parent Layer: `24d6d5ae2f1f9b2b8fe0ab5966e8080b1c1f05bb6ea47f39e1073343d87e27a4`
-	Docker Version: 1.9.1
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `kibana:4.0`

```console
$ docker pull library/kibana@sha256:3cc1a858504aba9c47023854b69ad9425697e6ef5621987771b040d3e8c345d2
```

-	Total v2 Content-Length: 83.2 MB (83235622 bytes)

### Layers (16)

#### `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`

```dockerfile
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
```

-	Created: Mon, 23 May 2016 22:57:20 GMT
-	v2 Blob: `sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`
-	v2 Content-Length: 51.4 MB (51356334 bytes)
-	v2 Last-Modified: Mon, 23 May 2016 23:09:48 GMT

#### `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Mon, 23 May 2016 22:57:23 GMT
-	Parent Layer: `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`

```dockerfile
RUN groupadd -r kibana && useradd -r -m -g kibana kibana
```

-	Created: Tue, 24 May 2016 02:15:27 GMT
-	Parent Layer: `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`
-	v2 Blob: `sha256:ef236d3c18b4ce0744c2ae4b8ae7f442605c745fd7b10c65b441ed51682b2c5f`
-	v2 Content-Length: 4.3 KB (4342 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:56 GMT

#### `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`

```dockerfile
RUN apt-get update && apt-get install -y 		ca-certificates 		wget 	--no-install-recommends && rm -rf /var/lib/apt/lists/*
```

-	Created: Tue, 24 May 2016 02:16:12 GMT
-	Parent Layer: `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`
-	v2 Blob: `sha256:7b4763c5420742eed897623fc3fc72c5a54f1245ee6d50734ca70a012f60a753`
-	v2 Content-Length: 16.6 MB (16615966 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:53 GMT

#### `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`

```dockerfile
ENV GOSU_VERSION=1.7
```

-	Created: Tue, 24 May 2016 02:16:15 GMT
-	Parent Layer: `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
```

-	Created: Tue, 24 May 2016 02:16:21 GMT
-	Parent Layer: `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`
-	v2 Blob: `sha256:8d4b6aaf60cb73053140071b6910c2697c581367449734e64959c86f2619d14f`
-	v2 Content-Length: 807.9 KB (807931 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:43 GMT

#### `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`

```dockerfile
ENV TINI_VERSION=v0.9.0
```

-	Created: Tue, 24 May 2016 02:16:23 GMT
-	Parent Layer: `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
```

-	Created: Tue, 24 May 2016 02:16:29 GMT
-	Parent Layer: `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`
-	v2 Blob: `sha256:a69ada16019ca97e3e09836f89b4fa99cf84902554f4df7857bd852a372a7417`
-	v2 Content-Length: 7.1 KB (7121 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:38 GMT

#### `c60aadc6a8b1c3db9fd09647b98af430f086d744d36cb786625ad77d1cada73a`

```dockerfile
ENV KIBANA_VERSION=4.0.3
```

-	Created: Tue, 24 May 2016 02:16:30 GMT
-	Parent Layer: `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `5f78175f5346d0a69ac63a833747df3cc7443c04a9c282145c0eebf4193ffa0a`

```dockerfile
ENV KIBANA_SHA1=75312e930466430167a7e01be3ae41aeaf01a26c
```

-	Created: Tue, 24 May 2016 02:16:31 GMT
-	Parent Layer: `c60aadc6a8b1c3db9fd09647b98af430f086d744d36cb786625ad77d1cada73a`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `a944edf45be17199542a6bacb8e9ba12a30940fda18712453270d72cd09cc4d9`

```dockerfile
RUN set -x 	&& wget -O kibana.tar.gz "https://download.elastic.co/kibana/kibana/kibana-${KIBANA_VERSION}-linux-x64.tar.gz" 	&& echo "${KIBANA_SHA1} *kibana.tar.gz" | sha1sum -c - 	&& mkdir -p /opt/kibana 	&& tar -xz --strip-components=1 -C /opt/kibana -f kibana.tar.gz 	&& chown -R kibana:kibana /opt/kibana 	&& rm kibana.tar.gz 		&& sed -ri "s!^(\#\s*)?(elasticsearch_url:).*!\2 'http://elasticsearch:9200'!" /opt/kibana/config/kibana.yml 	&& grep -q 'elasticsearch:9200' /opt/kibana/config/kibana.yml
```

-	Created: Tue, 24 May 2016 02:16:36 GMT
-	Parent Layer: `5f78175f5346d0a69ac63a833747df3cc7443c04a9c282145c0eebf4193ffa0a`
-	v2 Blob: `sha256:bf2516f9db2cc1b3138d553147b868a123e02683cb2f4e4e75e9869a3f2ae25d`
-	v2 Content-Length: 14.4 MB (14443298 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:28 GMT

#### `37cc14da24cbfee494124daa4d51533f6b64b2756a772b8324363bfbf37f6315`

```dockerfile
ENV PATH=/opt/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Created: Tue, 24 May 2016 02:16:46 GMT
-	Parent Layer: `a944edf45be17199542a6bacb8e9ba12a30940fda18712453270d72cd09cc4d9`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `473c4d74355c0e42bf336d2c4a12c39bb1f8288b148b6bb56c059abbf8d4829d`

```dockerfile
COPY file:bcaeac8c6bbd37e21bd6b91328c8390bf48cb8f8b62b7397258d943664deeba1 in /
```

-	Created: Tue, 24 May 2016 02:16:47 GMT
-	Parent Layer: `37cc14da24cbfee494124daa4d51533f6b64b2756a772b8324363bfbf37f6315`
-	v2 Blob: `sha256:7a2dc2187be63c58e3d9c3e2cec03f1b79ca5af72b1bf9602a71a9c43e4122ed`
-	v2 Content-Length: 342.0 B
-	v2 Last-Modified: Thu, 12 May 2016 19:36:15 GMT

#### `068639fe615edea1eb89fb7771a7ee01105bcb5b836e79cd79350eab30749f30`

```dockerfile
EXPOSE 5601/tcp
```

-	Created: Tue, 24 May 2016 02:16:48 GMT
-	Parent Layer: `473c4d74355c0e42bf336d2c4a12c39bb1f8288b148b6bb56c059abbf8d4829d`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `24d6d5ae2f1f9b2b8fe0ab5966e8080b1c1f05bb6ea47f39e1073343d87e27a4`

```dockerfile
ENTRYPOINT &{["/docker-entrypoint.sh"]}
```

-	Created: Tue, 24 May 2016 02:16:49 GMT
-	Parent Layer: `068639fe615edea1eb89fb7771a7ee01105bcb5b836e79cd79350eab30749f30`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `a63e24a31b0ad9c32d45115c12175ddcfcad6cbc2cda30bc2b194dba8c1a05f6`

```dockerfile
CMD ["kibana"]
```

-	Created: Tue, 24 May 2016 02:16:50 GMT
-	Parent Layer: `24d6d5ae2f1f9b2b8fe0ab5966e8080b1c1f05bb6ea47f39e1073343d87e27a4`
-	Docker Version: 1.9.1
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `kibana:4.1.8`

**does not exist** (yet?)

## `kibana:4.1`

```console
$ docker pull library/kibana@sha256:b03b9ad68e0660f4424e58a2b205dfede9aaa0f76404002270138e6246ba58bc
```

-	Total v2 Content-Length: 88.0 MB (88035639 bytes)

### Layers (16)

#### `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`

```dockerfile
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
```

-	Created: Mon, 23 May 2016 22:57:20 GMT
-	v2 Blob: `sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`
-	v2 Content-Length: 51.4 MB (51356334 bytes)
-	v2 Last-Modified: Mon, 23 May 2016 23:09:48 GMT

#### `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Mon, 23 May 2016 22:57:23 GMT
-	Parent Layer: `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`

```dockerfile
RUN groupadd -r kibana && useradd -r -m -g kibana kibana
```

-	Created: Tue, 24 May 2016 02:15:27 GMT
-	Parent Layer: `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`
-	v2 Blob: `sha256:ef236d3c18b4ce0744c2ae4b8ae7f442605c745fd7b10c65b441ed51682b2c5f`
-	v2 Content-Length: 4.3 KB (4342 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:56 GMT

#### `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`

```dockerfile
RUN apt-get update && apt-get install -y 		ca-certificates 		wget 	--no-install-recommends && rm -rf /var/lib/apt/lists/*
```

-	Created: Tue, 24 May 2016 02:16:12 GMT
-	Parent Layer: `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`
-	v2 Blob: `sha256:7b4763c5420742eed897623fc3fc72c5a54f1245ee6d50734ca70a012f60a753`
-	v2 Content-Length: 16.6 MB (16615966 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:53 GMT

#### `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`

```dockerfile
ENV GOSU_VERSION=1.7
```

-	Created: Tue, 24 May 2016 02:16:15 GMT
-	Parent Layer: `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
```

-	Created: Tue, 24 May 2016 02:16:21 GMT
-	Parent Layer: `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`
-	v2 Blob: `sha256:8d4b6aaf60cb73053140071b6910c2697c581367449734e64959c86f2619d14f`
-	v2 Content-Length: 807.9 KB (807931 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:43 GMT

#### `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`

```dockerfile
ENV TINI_VERSION=v0.9.0
```

-	Created: Tue, 24 May 2016 02:16:23 GMT
-	Parent Layer: `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
```

-	Created: Tue, 24 May 2016 02:16:29 GMT
-	Parent Layer: `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`
-	v2 Blob: `sha256:a69ada16019ca97e3e09836f89b4fa99cf84902554f4df7857bd852a372a7417`
-	v2 Content-Length: 7.1 KB (7121 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:38 GMT

#### `c60aadc6a8b1c3db9fd09647b98af430f086d744d36cb786625ad77d1cada73a`

```dockerfile
ENV KIBANA_VERSION=4.0.3
```

-	Created: Tue, 24 May 2016 02:16:30 GMT
-	Parent Layer: `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `5f78175f5346d0a69ac63a833747df3cc7443c04a9c282145c0eebf4193ffa0a`

```dockerfile
ENV KIBANA_SHA1=75312e930466430167a7e01be3ae41aeaf01a26c
```

-	Created: Tue, 24 May 2016 02:16:31 GMT
-	Parent Layer: `c60aadc6a8b1c3db9fd09647b98af430f086d744d36cb786625ad77d1cada73a`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `aa8cde98cbd2351f2afe08aed320bb6a63e1224f57b994b2e59cd29d34ab4c7b`

```dockerfile
RUN set -x 	&& wget -O kibana.tar.gz "https://download.elastic.co/kibana/kibana/kibana-${KIBANA_VERSION}-linux-x64.tar.gz" 	&& echo "${KIBANA_SHA1} *kibana.tar.gz" | sha1sum -c - 	&& mkdir -p /opt/kibana 	&& tar -xz --strip-components=1 -C /opt/kibana -f kibana.tar.gz 	&& chown -R kibana:kibana /opt/kibana 	&& rm kibana.tar.gz 		&& sed -ri "s!^(\#\s*)?(elasticsearch_url:).*!\2 'http://elasticsearch:9200'!" /opt/kibana/config/kibana.yml 	&& grep -q 'elasticsearch:9200' /opt/kibana/config/kibana.yml
```

-	Created: Tue, 24 May 2016 02:19:10 GMT
-	Parent Layer: `5f78175f5346d0a69ac63a833747df3cc7443c04a9c282145c0eebf4193ffa0a`
-	v2 Blob: `sha256:58d962a476145a7dab868b302fcad6ac7afaf0ac61dde3af4a619a5861b184cb`
-	v2 Content-Length: 19.2 MB (19243315 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:01:49 GMT

#### `21d5a8ad5d52cfb6573ae1295a7f6cf16c51032d45c69bcd8c8042c09fcfb718`

```dockerfile
ENV PATH=/opt/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Created: Tue, 24 May 2016 02:19:33 GMT
-	Parent Layer: `aa8cde98cbd2351f2afe08aed320bb6a63e1224f57b994b2e59cd29d34ab4c7b`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `8cdd2f8eddb0fccbb328dda743c55a4440ee913e302a6bb2c2193f954f282ca9`

```dockerfile
COPY file:bcaeac8c6bbd37e21bd6b91328c8390bf48cb8f8b62b7397258d943664deeba1 in /
```

-	Created: Tue, 24 May 2016 02:19:34 GMT
-	Parent Layer: `21d5a8ad5d52cfb6573ae1295a7f6cf16c51032d45c69bcd8c8042c09fcfb718`
-	v2 Blob: `sha256:7a2dc2187be63c58e3d9c3e2cec03f1b79ca5af72b1bf9602a71a9c43e4122ed`
-	v2 Content-Length: 342.0 B
-	v2 Last-Modified: Thu, 12 May 2016 19:36:15 GMT

#### `df6e9acb96534953916e22765e522d5bcb183c3dc620867f881519386aece4c9`

```dockerfile
EXPOSE 5601/tcp
```

-	Created: Tue, 24 May 2016 02:19:35 GMT
-	Parent Layer: `8cdd2f8eddb0fccbb328dda743c55a4440ee913e302a6bb2c2193f954f282ca9`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `dc74d85d64a266e96ddccacb8466764e1672d45655f098af5261a77898e2ed06`

```dockerfile
ENTRYPOINT &{["/docker-entrypoint.sh"]}
```

-	Created: Tue, 24 May 2016 02:19:36 GMT
-	Parent Layer: `df6e9acb96534953916e22765e522d5bcb183c3dc620867f881519386aece4c9`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `555aa3c83d8b6a2a716cd837e62f9c7d2b9ebdc10db0617eaadc7292e07201a8`

```dockerfile
CMD ["kibana"]
```

-	Created: Tue, 24 May 2016 02:19:37 GMT
-	Parent Layer: `dc74d85d64a266e96ddccacb8466764e1672d45655f098af5261a77898e2ed06`
-	Docker Version: 1.9.1
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `kibana:4.2.2`

```console
$ docker pull library/kibana@sha256:bf1b8ed5ab53f3cd82bc1aa11fc998ba6aafd46071be73f67b33d049e7586f5d
```

-	Total v2 Content-Length: 99.3 MB (99292985 bytes)

### Layers (16)

#### `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`

```dockerfile
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
```

-	Created: Mon, 23 May 2016 22:57:20 GMT
-	v2 Blob: `sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`
-	v2 Content-Length: 51.4 MB (51356334 bytes)
-	v2 Last-Modified: Mon, 23 May 2016 23:09:48 GMT

#### `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Mon, 23 May 2016 22:57:23 GMT
-	Parent Layer: `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`

```dockerfile
RUN groupadd -r kibana && useradd -r -m -g kibana kibana
```

-	Created: Tue, 24 May 2016 02:15:27 GMT
-	Parent Layer: `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`
-	v2 Blob: `sha256:ef236d3c18b4ce0744c2ae4b8ae7f442605c745fd7b10c65b441ed51682b2c5f`
-	v2 Content-Length: 4.3 KB (4342 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:56 GMT

#### `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`

```dockerfile
RUN apt-get update && apt-get install -y 		ca-certificates 		wget 	--no-install-recommends && rm -rf /var/lib/apt/lists/*
```

-	Created: Tue, 24 May 2016 02:16:12 GMT
-	Parent Layer: `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`
-	v2 Blob: `sha256:7b4763c5420742eed897623fc3fc72c5a54f1245ee6d50734ca70a012f60a753`
-	v2 Content-Length: 16.6 MB (16615966 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:53 GMT

#### `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`

```dockerfile
ENV GOSU_VERSION=1.7
```

-	Created: Tue, 24 May 2016 02:16:15 GMT
-	Parent Layer: `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
```

-	Created: Tue, 24 May 2016 02:16:21 GMT
-	Parent Layer: `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`
-	v2 Blob: `sha256:8d4b6aaf60cb73053140071b6910c2697c581367449734e64959c86f2619d14f`
-	v2 Content-Length: 807.9 KB (807931 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:43 GMT

#### `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`

```dockerfile
ENV TINI_VERSION=v0.9.0
```

-	Created: Tue, 24 May 2016 02:16:23 GMT
-	Parent Layer: `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
```

-	Created: Tue, 24 May 2016 02:16:29 GMT
-	Parent Layer: `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`
-	v2 Blob: `sha256:a69ada16019ca97e3e09836f89b4fa99cf84902554f4df7857bd852a372a7417`
-	v2 Content-Length: 7.1 KB (7121 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:38 GMT

#### `c60aadc6a8b1c3db9fd09647b98af430f086d744d36cb786625ad77d1cada73a`

```dockerfile
ENV KIBANA_VERSION=4.0.3
```

-	Created: Tue, 24 May 2016 02:16:30 GMT
-	Parent Layer: `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `5f78175f5346d0a69ac63a833747df3cc7443c04a9c282145c0eebf4193ffa0a`

```dockerfile
ENV KIBANA_SHA1=75312e930466430167a7e01be3ae41aeaf01a26c
```

-	Created: Tue, 24 May 2016 02:16:31 GMT
-	Parent Layer: `c60aadc6a8b1c3db9fd09647b98af430f086d744d36cb786625ad77d1cada73a`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `c50a99fca7a6eed1fa951dbddfd4bdf7b5cb7df5f4252803876d65cfe54ad713`

```dockerfile
RUN set -x 	&& wget -O kibana.tar.gz "https://download.elastic.co/kibana/kibana/kibana-${KIBANA_VERSION}-linux-x64.tar.gz" 	&& echo "${KIBANA_SHA1} *kibana.tar.gz" | sha1sum -c - 	&& mkdir -p /opt/kibana 	&& tar -xz --strip-components=1 -C /opt/kibana -f kibana.tar.gz 	&& chown -R kibana:kibana /opt/kibana 	&& rm kibana.tar.gz 		&& sed -ri "s!^(\#\s*)?(elasticsearch\.url:).*!\2 'http://elasticsearch:9200'!" /opt/kibana/config/kibana.yml 	&& grep -q 'elasticsearch:9200' /opt/kibana/config/kibana.yml
```

-	Created: Tue, 24 May 2016 02:22:00 GMT
-	Parent Layer: `5f78175f5346d0a69ac63a833747df3cc7443c04a9c282145c0eebf4193ffa0a`
-	v2 Blob: `sha256:9d9193a997dea9cb0905465d774618fbf5c3f4bb997cf99c1534e717b3d37311`
-	v2 Content-Length: 30.5 MB (30500658 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:02:42 GMT

#### `b83b15c6ea271cf7628f5bcf10af497c4fd0d7423b7d2d511762df2d261b5b24`

```dockerfile
ENV PATH=/opt/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Created: Tue, 24 May 2016 02:22:06 GMT
-	Parent Layer: `c50a99fca7a6eed1fa951dbddfd4bdf7b5cb7df5f4252803876d65cfe54ad713`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `e3d136a6e64f37a7b36d70bdf66d788058bf6108d05adf9c6363e71cb543c488`

```dockerfile
COPY file:19c1e8bb9b9b1bfd96fabd1909bec9f7fc0a0134c2a2712ac20b5d4dfeeccb80 in /
```

-	Created: Tue, 24 May 2016 02:22:07 GMT
-	Parent Layer: `b83b15c6ea271cf7628f5bcf10af497c4fd0d7423b7d2d511762df2d261b5b24`
-	v2 Blob: `sha256:b40842db255aa7a6d423e4caec50388d2b6799bdd3f686d8b5f271bdd225d52e`
-	v2 Content-Length: 345.0 B
-	v2 Last-Modified: Thu, 12 May 2016 19:38:05 GMT

#### `f4640a40f4f9bf3d7b8a6e907503e03301d7c2188dd25cad0edc21ba36e48790`

```dockerfile
EXPOSE 5601/tcp
```

-	Created: Tue, 24 May 2016 02:22:08 GMT
-	Parent Layer: `e3d136a6e64f37a7b36d70bdf66d788058bf6108d05adf9c6363e71cb543c488`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `e7a40d5d3fd3c44bcd7f23a552a038d109b779377d06ed72dcfb1459ecc7ac67`

```dockerfile
ENTRYPOINT &{["/docker-entrypoint.sh"]}
```

-	Created: Tue, 24 May 2016 02:22:09 GMT
-	Parent Layer: `f4640a40f4f9bf3d7b8a6e907503e03301d7c2188dd25cad0edc21ba36e48790`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `717dbf2d71ae098a4bfca44976945eb8b3d14c7e2f45123a1ef81cabd7414234`

```dockerfile
CMD ["kibana"]
```

-	Created: Tue, 24 May 2016 02:22:10 GMT
-	Parent Layer: `e7a40d5d3fd3c44bcd7f23a552a038d109b779377d06ed72dcfb1459ecc7ac67`
-	Docker Version: 1.9.1
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `kibana:4.2`

```console
$ docker pull library/kibana@sha256:afedc34492a22f1196f362a243da15030b99a6bb8ae95baed6df2140ecb890cd
```

-	Total v2 Content-Length: 99.3 MB (99292985 bytes)

### Layers (16)

#### `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`

```dockerfile
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
```

-	Created: Mon, 23 May 2016 22:57:20 GMT
-	v2 Blob: `sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`
-	v2 Content-Length: 51.4 MB (51356334 bytes)
-	v2 Last-Modified: Mon, 23 May 2016 23:09:48 GMT

#### `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Mon, 23 May 2016 22:57:23 GMT
-	Parent Layer: `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`

```dockerfile
RUN groupadd -r kibana && useradd -r -m -g kibana kibana
```

-	Created: Tue, 24 May 2016 02:15:27 GMT
-	Parent Layer: `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`
-	v2 Blob: `sha256:ef236d3c18b4ce0744c2ae4b8ae7f442605c745fd7b10c65b441ed51682b2c5f`
-	v2 Content-Length: 4.3 KB (4342 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:56 GMT

#### `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`

```dockerfile
RUN apt-get update && apt-get install -y 		ca-certificates 		wget 	--no-install-recommends && rm -rf /var/lib/apt/lists/*
```

-	Created: Tue, 24 May 2016 02:16:12 GMT
-	Parent Layer: `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`
-	v2 Blob: `sha256:7b4763c5420742eed897623fc3fc72c5a54f1245ee6d50734ca70a012f60a753`
-	v2 Content-Length: 16.6 MB (16615966 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:53 GMT

#### `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`

```dockerfile
ENV GOSU_VERSION=1.7
```

-	Created: Tue, 24 May 2016 02:16:15 GMT
-	Parent Layer: `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
```

-	Created: Tue, 24 May 2016 02:16:21 GMT
-	Parent Layer: `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`
-	v2 Blob: `sha256:8d4b6aaf60cb73053140071b6910c2697c581367449734e64959c86f2619d14f`
-	v2 Content-Length: 807.9 KB (807931 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:43 GMT

#### `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`

```dockerfile
ENV TINI_VERSION=v0.9.0
```

-	Created: Tue, 24 May 2016 02:16:23 GMT
-	Parent Layer: `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
```

-	Created: Tue, 24 May 2016 02:16:29 GMT
-	Parent Layer: `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`
-	v2 Blob: `sha256:a69ada16019ca97e3e09836f89b4fa99cf84902554f4df7857bd852a372a7417`
-	v2 Content-Length: 7.1 KB (7121 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:38 GMT

#### `c60aadc6a8b1c3db9fd09647b98af430f086d744d36cb786625ad77d1cada73a`

```dockerfile
ENV KIBANA_VERSION=4.0.3
```

-	Created: Tue, 24 May 2016 02:16:30 GMT
-	Parent Layer: `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `5f78175f5346d0a69ac63a833747df3cc7443c04a9c282145c0eebf4193ffa0a`

```dockerfile
ENV KIBANA_SHA1=75312e930466430167a7e01be3ae41aeaf01a26c
```

-	Created: Tue, 24 May 2016 02:16:31 GMT
-	Parent Layer: `c60aadc6a8b1c3db9fd09647b98af430f086d744d36cb786625ad77d1cada73a`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `c50a99fca7a6eed1fa951dbddfd4bdf7b5cb7df5f4252803876d65cfe54ad713`

```dockerfile
RUN set -x 	&& wget -O kibana.tar.gz "https://download.elastic.co/kibana/kibana/kibana-${KIBANA_VERSION}-linux-x64.tar.gz" 	&& echo "${KIBANA_SHA1} *kibana.tar.gz" | sha1sum -c - 	&& mkdir -p /opt/kibana 	&& tar -xz --strip-components=1 -C /opt/kibana -f kibana.tar.gz 	&& chown -R kibana:kibana /opt/kibana 	&& rm kibana.tar.gz 		&& sed -ri "s!^(\#\s*)?(elasticsearch\.url:).*!\2 'http://elasticsearch:9200'!" /opt/kibana/config/kibana.yml 	&& grep -q 'elasticsearch:9200' /opt/kibana/config/kibana.yml
```

-	Created: Tue, 24 May 2016 02:22:00 GMT
-	Parent Layer: `5f78175f5346d0a69ac63a833747df3cc7443c04a9c282145c0eebf4193ffa0a`
-	v2 Blob: `sha256:9d9193a997dea9cb0905465d774618fbf5c3f4bb997cf99c1534e717b3d37311`
-	v2 Content-Length: 30.5 MB (30500658 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:02:42 GMT

#### `b83b15c6ea271cf7628f5bcf10af497c4fd0d7423b7d2d511762df2d261b5b24`

```dockerfile
ENV PATH=/opt/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Created: Tue, 24 May 2016 02:22:06 GMT
-	Parent Layer: `c50a99fca7a6eed1fa951dbddfd4bdf7b5cb7df5f4252803876d65cfe54ad713`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `e3d136a6e64f37a7b36d70bdf66d788058bf6108d05adf9c6363e71cb543c488`

```dockerfile
COPY file:19c1e8bb9b9b1bfd96fabd1909bec9f7fc0a0134c2a2712ac20b5d4dfeeccb80 in /
```

-	Created: Tue, 24 May 2016 02:22:07 GMT
-	Parent Layer: `b83b15c6ea271cf7628f5bcf10af497c4fd0d7423b7d2d511762df2d261b5b24`
-	v2 Blob: `sha256:b40842db255aa7a6d423e4caec50388d2b6799bdd3f686d8b5f271bdd225d52e`
-	v2 Content-Length: 345.0 B
-	v2 Last-Modified: Thu, 12 May 2016 19:38:05 GMT

#### `f4640a40f4f9bf3d7b8a6e907503e03301d7c2188dd25cad0edc21ba36e48790`

```dockerfile
EXPOSE 5601/tcp
```

-	Created: Tue, 24 May 2016 02:22:08 GMT
-	Parent Layer: `e3d136a6e64f37a7b36d70bdf66d788058bf6108d05adf9c6363e71cb543c488`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `e7a40d5d3fd3c44bcd7f23a552a038d109b779377d06ed72dcfb1459ecc7ac67`

```dockerfile
ENTRYPOINT &{["/docker-entrypoint.sh"]}
```

-	Created: Tue, 24 May 2016 02:22:09 GMT
-	Parent Layer: `f4640a40f4f9bf3d7b8a6e907503e03301d7c2188dd25cad0edc21ba36e48790`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `717dbf2d71ae098a4bfca44976945eb8b3d14c7e2f45123a1ef81cabd7414234`

```dockerfile
CMD ["kibana"]
```

-	Created: Tue, 24 May 2016 02:22:10 GMT
-	Parent Layer: `e7a40d5d3fd3c44bcd7f23a552a038d109b779377d06ed72dcfb1459ecc7ac67`
-	Docker Version: 1.9.1
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `kibana:4.3.3`

```console
$ docker pull library/kibana@sha256:fc2060784e64fd0441cab815a743f17d7ea0ab9328f8b859c994f8aa05760e37
```

-	Total v2 Content-Length: 101.3 MB (101320017 bytes)

### Layers (16)

#### `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`

```dockerfile
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
```

-	Created: Mon, 23 May 2016 22:57:20 GMT
-	v2 Blob: `sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`
-	v2 Content-Length: 51.4 MB (51356334 bytes)
-	v2 Last-Modified: Mon, 23 May 2016 23:09:48 GMT

#### `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Mon, 23 May 2016 22:57:23 GMT
-	Parent Layer: `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`

```dockerfile
RUN groupadd -r kibana && useradd -r -m -g kibana kibana
```

-	Created: Tue, 24 May 2016 02:15:27 GMT
-	Parent Layer: `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`
-	v2 Blob: `sha256:ef236d3c18b4ce0744c2ae4b8ae7f442605c745fd7b10c65b441ed51682b2c5f`
-	v2 Content-Length: 4.3 KB (4342 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:56 GMT

#### `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`

```dockerfile
RUN apt-get update && apt-get install -y 		ca-certificates 		wget 	--no-install-recommends && rm -rf /var/lib/apt/lists/*
```

-	Created: Tue, 24 May 2016 02:16:12 GMT
-	Parent Layer: `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`
-	v2 Blob: `sha256:7b4763c5420742eed897623fc3fc72c5a54f1245ee6d50734ca70a012f60a753`
-	v2 Content-Length: 16.6 MB (16615966 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:53 GMT

#### `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`

```dockerfile
ENV GOSU_VERSION=1.7
```

-	Created: Tue, 24 May 2016 02:16:15 GMT
-	Parent Layer: `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
```

-	Created: Tue, 24 May 2016 02:16:21 GMT
-	Parent Layer: `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`
-	v2 Blob: `sha256:8d4b6aaf60cb73053140071b6910c2697c581367449734e64959c86f2619d14f`
-	v2 Content-Length: 807.9 KB (807931 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:43 GMT

#### `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`

```dockerfile
ENV TINI_VERSION=v0.9.0
```

-	Created: Tue, 24 May 2016 02:16:23 GMT
-	Parent Layer: `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
```

-	Created: Tue, 24 May 2016 02:16:29 GMT
-	Parent Layer: `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`
-	v2 Blob: `sha256:a69ada16019ca97e3e09836f89b4fa99cf84902554f4df7857bd852a372a7417`
-	v2 Content-Length: 7.1 KB (7121 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:38 GMT

#### `c60aadc6a8b1c3db9fd09647b98af430f086d744d36cb786625ad77d1cada73a`

```dockerfile
ENV KIBANA_VERSION=4.0.3
```

-	Created: Tue, 24 May 2016 02:16:30 GMT
-	Parent Layer: `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `5f78175f5346d0a69ac63a833747df3cc7443c04a9c282145c0eebf4193ffa0a`

```dockerfile
ENV KIBANA_SHA1=75312e930466430167a7e01be3ae41aeaf01a26c
```

-	Created: Tue, 24 May 2016 02:16:31 GMT
-	Parent Layer: `c60aadc6a8b1c3db9fd09647b98af430f086d744d36cb786625ad77d1cada73a`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `88edc4264823846a22209a1186de7adeae8777ccf06bc309753131cd78f7e6ec`

```dockerfile
RUN set -x 	&& wget -O kibana.tar.gz "https://download.elastic.co/kibana/kibana/kibana-${KIBANA_VERSION}-linux-x64.tar.gz" 	&& echo "${KIBANA_SHA1} *kibana.tar.gz" | sha1sum -c - 	&& mkdir -p /opt/kibana 	&& tar -xz --strip-components=1 -C /opt/kibana -f kibana.tar.gz 	&& chown -R kibana:kibana /opt/kibana 	&& rm kibana.tar.gz 		&& sed -ri "s!^(\#\s*)?(elasticsearch\.url:).*!\2 'http://elasticsearch:9200'!" /opt/kibana/config/kibana.yml 	&& grep -q 'elasticsearch:9200' /opt/kibana/config/kibana.yml
```

-	Created: Tue, 24 May 2016 02:24:08 GMT
-	Parent Layer: `5f78175f5346d0a69ac63a833747df3cc7443c04a9c282145c0eebf4193ffa0a`
-	v2 Blob: `sha256:6a5c66c66124209db2484659e13c21815e13efa809885d95756ee52eefcaf301`
-	v2 Content-Length: 32.5 MB (32527690 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:03:37 GMT

#### `20c0e3f2523ab2e14a508ba8d870528001bc83ee5a1dc009ef97664d3369bde6`

```dockerfile
ENV PATH=/opt/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Created: Tue, 24 May 2016 02:24:17 GMT
-	Parent Layer: `88edc4264823846a22209a1186de7adeae8777ccf06bc309753131cd78f7e6ec`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `5eb1caa82f7216cd635448b217a2791a25c66c3c53d6f37c41c5c50a31787448`

```dockerfile
COPY file:19c1e8bb9b9b1bfd96fabd1909bec9f7fc0a0134c2a2712ac20b5d4dfeeccb80 in /
```

-	Created: Tue, 24 May 2016 02:24:19 GMT
-	Parent Layer: `20c0e3f2523ab2e14a508ba8d870528001bc83ee5a1dc009ef97664d3369bde6`
-	v2 Blob: `sha256:b40842db255aa7a6d423e4caec50388d2b6799bdd3f686d8b5f271bdd225d52e`
-	v2 Content-Length: 345.0 B
-	v2 Last-Modified: Thu, 12 May 2016 19:38:05 GMT

#### `5f053de1a38bf47056ab6af90fa0019d54658bdacba5182835038ad5d29a7035`

```dockerfile
EXPOSE 5601/tcp
```

-	Created: Tue, 24 May 2016 02:24:20 GMT
-	Parent Layer: `5eb1caa82f7216cd635448b217a2791a25c66c3c53d6f37c41c5c50a31787448`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `28e84a245bffce46f96b944c79adb4ff03c4281d03b4176f52cfbf5c349a15d1`

```dockerfile
ENTRYPOINT &{["/docker-entrypoint.sh"]}
```

-	Created: Tue, 24 May 2016 02:24:21 GMT
-	Parent Layer: `5f053de1a38bf47056ab6af90fa0019d54658bdacba5182835038ad5d29a7035`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `306c958bd497b3c4259786cf3f5bbd26b6143f842d767e5192968c8fd639241a`

```dockerfile
CMD ["kibana"]
```

-	Created: Tue, 24 May 2016 02:24:22 GMT
-	Parent Layer: `28e84a245bffce46f96b944c79adb4ff03c4281d03b4176f52cfbf5c349a15d1`
-	Docker Version: 1.9.1
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `kibana:4.3`

```console
$ docker pull library/kibana@sha256:4dd2e1d8e78a83343da0a8d300d67caec956396e98b002f3f30aa8490aa4055b
```

-	Total v2 Content-Length: 101.3 MB (101320017 bytes)

### Layers (16)

#### `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`

```dockerfile
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
```

-	Created: Mon, 23 May 2016 22:57:20 GMT
-	v2 Blob: `sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`
-	v2 Content-Length: 51.4 MB (51356334 bytes)
-	v2 Last-Modified: Mon, 23 May 2016 23:09:48 GMT

#### `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Mon, 23 May 2016 22:57:23 GMT
-	Parent Layer: `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`

```dockerfile
RUN groupadd -r kibana && useradd -r -m -g kibana kibana
```

-	Created: Tue, 24 May 2016 02:15:27 GMT
-	Parent Layer: `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`
-	v2 Blob: `sha256:ef236d3c18b4ce0744c2ae4b8ae7f442605c745fd7b10c65b441ed51682b2c5f`
-	v2 Content-Length: 4.3 KB (4342 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:56 GMT

#### `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`

```dockerfile
RUN apt-get update && apt-get install -y 		ca-certificates 		wget 	--no-install-recommends && rm -rf /var/lib/apt/lists/*
```

-	Created: Tue, 24 May 2016 02:16:12 GMT
-	Parent Layer: `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`
-	v2 Blob: `sha256:7b4763c5420742eed897623fc3fc72c5a54f1245ee6d50734ca70a012f60a753`
-	v2 Content-Length: 16.6 MB (16615966 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:53 GMT

#### `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`

```dockerfile
ENV GOSU_VERSION=1.7
```

-	Created: Tue, 24 May 2016 02:16:15 GMT
-	Parent Layer: `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
```

-	Created: Tue, 24 May 2016 02:16:21 GMT
-	Parent Layer: `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`
-	v2 Blob: `sha256:8d4b6aaf60cb73053140071b6910c2697c581367449734e64959c86f2619d14f`
-	v2 Content-Length: 807.9 KB (807931 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:43 GMT

#### `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`

```dockerfile
ENV TINI_VERSION=v0.9.0
```

-	Created: Tue, 24 May 2016 02:16:23 GMT
-	Parent Layer: `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
```

-	Created: Tue, 24 May 2016 02:16:29 GMT
-	Parent Layer: `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`
-	v2 Blob: `sha256:a69ada16019ca97e3e09836f89b4fa99cf84902554f4df7857bd852a372a7417`
-	v2 Content-Length: 7.1 KB (7121 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:38 GMT

#### `c60aadc6a8b1c3db9fd09647b98af430f086d744d36cb786625ad77d1cada73a`

```dockerfile
ENV KIBANA_VERSION=4.0.3
```

-	Created: Tue, 24 May 2016 02:16:30 GMT
-	Parent Layer: `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `5f78175f5346d0a69ac63a833747df3cc7443c04a9c282145c0eebf4193ffa0a`

```dockerfile
ENV KIBANA_SHA1=75312e930466430167a7e01be3ae41aeaf01a26c
```

-	Created: Tue, 24 May 2016 02:16:31 GMT
-	Parent Layer: `c60aadc6a8b1c3db9fd09647b98af430f086d744d36cb786625ad77d1cada73a`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `88edc4264823846a22209a1186de7adeae8777ccf06bc309753131cd78f7e6ec`

```dockerfile
RUN set -x 	&& wget -O kibana.tar.gz "https://download.elastic.co/kibana/kibana/kibana-${KIBANA_VERSION}-linux-x64.tar.gz" 	&& echo "${KIBANA_SHA1} *kibana.tar.gz" | sha1sum -c - 	&& mkdir -p /opt/kibana 	&& tar -xz --strip-components=1 -C /opt/kibana -f kibana.tar.gz 	&& chown -R kibana:kibana /opt/kibana 	&& rm kibana.tar.gz 		&& sed -ri "s!^(\#\s*)?(elasticsearch\.url:).*!\2 'http://elasticsearch:9200'!" /opt/kibana/config/kibana.yml 	&& grep -q 'elasticsearch:9200' /opt/kibana/config/kibana.yml
```

-	Created: Tue, 24 May 2016 02:24:08 GMT
-	Parent Layer: `5f78175f5346d0a69ac63a833747df3cc7443c04a9c282145c0eebf4193ffa0a`
-	v2 Blob: `sha256:6a5c66c66124209db2484659e13c21815e13efa809885d95756ee52eefcaf301`
-	v2 Content-Length: 32.5 MB (32527690 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:03:37 GMT

#### `20c0e3f2523ab2e14a508ba8d870528001bc83ee5a1dc009ef97664d3369bde6`

```dockerfile
ENV PATH=/opt/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Created: Tue, 24 May 2016 02:24:17 GMT
-	Parent Layer: `88edc4264823846a22209a1186de7adeae8777ccf06bc309753131cd78f7e6ec`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `5eb1caa82f7216cd635448b217a2791a25c66c3c53d6f37c41c5c50a31787448`

```dockerfile
COPY file:19c1e8bb9b9b1bfd96fabd1909bec9f7fc0a0134c2a2712ac20b5d4dfeeccb80 in /
```

-	Created: Tue, 24 May 2016 02:24:19 GMT
-	Parent Layer: `20c0e3f2523ab2e14a508ba8d870528001bc83ee5a1dc009ef97664d3369bde6`
-	v2 Blob: `sha256:b40842db255aa7a6d423e4caec50388d2b6799bdd3f686d8b5f271bdd225d52e`
-	v2 Content-Length: 345.0 B
-	v2 Last-Modified: Thu, 12 May 2016 19:38:05 GMT

#### `5f053de1a38bf47056ab6af90fa0019d54658bdacba5182835038ad5d29a7035`

```dockerfile
EXPOSE 5601/tcp
```

-	Created: Tue, 24 May 2016 02:24:20 GMT
-	Parent Layer: `5eb1caa82f7216cd635448b217a2791a25c66c3c53d6f37c41c5c50a31787448`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `28e84a245bffce46f96b944c79adb4ff03c4281d03b4176f52cfbf5c349a15d1`

```dockerfile
ENTRYPOINT &{["/docker-entrypoint.sh"]}
```

-	Created: Tue, 24 May 2016 02:24:21 GMT
-	Parent Layer: `5f053de1a38bf47056ab6af90fa0019d54658bdacba5182835038ad5d29a7035`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `306c958bd497b3c4259786cf3f5bbd26b6143f842d767e5192968c8fd639241a`

```dockerfile
CMD ["kibana"]
```

-	Created: Tue, 24 May 2016 02:24:22 GMT
-	Parent Layer: `28e84a245bffce46f96b944c79adb4ff03c4281d03b4176f52cfbf5c349a15d1`
-	Docker Version: 1.9.1
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `kibana:4.4.2`

```console
$ docker pull library/kibana@sha256:f71bcb0f9b9f8b33dcb105939ad902ae17a59539d57939d8753ba1f4efd1392c
```

-	Total v2 Content-Length: 101.8 MB (101841896 bytes)

### Layers (18)

#### `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`

```dockerfile
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
```

-	Created: Mon, 23 May 2016 22:57:20 GMT
-	v2 Blob: `sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`
-	v2 Content-Length: 51.4 MB (51356334 bytes)
-	v2 Last-Modified: Mon, 23 May 2016 23:09:48 GMT

#### `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Mon, 23 May 2016 22:57:23 GMT
-	Parent Layer: `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`

```dockerfile
RUN groupadd -r kibana && useradd -r -m -g kibana kibana
```

-	Created: Tue, 24 May 2016 02:15:27 GMT
-	Parent Layer: `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`
-	v2 Blob: `sha256:ef236d3c18b4ce0744c2ae4b8ae7f442605c745fd7b10c65b441ed51682b2c5f`
-	v2 Content-Length: 4.3 KB (4342 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:56 GMT

#### `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`

```dockerfile
RUN apt-get update && apt-get install -y 		ca-certificates 		wget 	--no-install-recommends && rm -rf /var/lib/apt/lists/*
```

-	Created: Tue, 24 May 2016 02:16:12 GMT
-	Parent Layer: `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`
-	v2 Blob: `sha256:7b4763c5420742eed897623fc3fc72c5a54f1245ee6d50734ca70a012f60a753`
-	v2 Content-Length: 16.6 MB (16615966 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:53 GMT

#### `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`

```dockerfile
ENV GOSU_VERSION=1.7
```

-	Created: Tue, 24 May 2016 02:16:15 GMT
-	Parent Layer: `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
```

-	Created: Tue, 24 May 2016 02:16:21 GMT
-	Parent Layer: `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`
-	v2 Blob: `sha256:8d4b6aaf60cb73053140071b6910c2697c581367449734e64959c86f2619d14f`
-	v2 Content-Length: 807.9 KB (807931 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:43 GMT

#### `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`

```dockerfile
ENV TINI_VERSION=v0.9.0
```

-	Created: Tue, 24 May 2016 02:16:23 GMT
-	Parent Layer: `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
```

-	Created: Tue, 24 May 2016 02:16:29 GMT
-	Parent Layer: `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`
-	v2 Blob: `sha256:a69ada16019ca97e3e09836f89b4fa99cf84902554f4df7857bd852a372a7417`
-	v2 Content-Length: 7.1 KB (7121 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:38 GMT

#### `3ed696f09b1d5f406d763f15956349e40ede1914c5504b19fcd20ec96c4b2b1e`

```dockerfile
RUN apt-key adv --keyserver ha.pool.sks-keyservers.net --recv-keys 46095ACC8548582C1A2699A9D27D666CD88E42B4
```

-	Created: Tue, 24 May 2016 02:26:31 GMT
-	Parent Layer: `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`
-	v2 Blob: `sha256:bc20bd2597ed2f4e39d66072bac0322c025a28501ed7d3702ea59600425c5a5f`
-	v2 Content-Length: 1.5 KB (1451 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:05:23 GMT

#### `4fd95a9187de0a9dbf990d6fcdeb0cd04a19ffe8128cc77eb0438e38fe12e58b`

```dockerfile
ENV KIBANA_MAJOR=4.4
```

-	Created: Tue, 24 May 2016 02:26:32 GMT
-	Parent Layer: `3ed696f09b1d5f406d763f15956349e40ede1914c5504b19fcd20ec96c4b2b1e`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `7b80c210be5b805e11d46e7d05d9e6cad145928993383f06860bce7b8dc61959`

```dockerfile
ENV KIBANA_VERSION=4.4.2
```

-	Created: Tue, 24 May 2016 02:26:33 GMT
-	Parent Layer: `4fd95a9187de0a9dbf990d6fcdeb0cd04a19ffe8128cc77eb0438e38fe12e58b`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `c8eae2c7363f1980c18852b8d2eccff42162ff2b7f77c3d75e7b86facc7d892c`

```dockerfile
RUN echo "deb http://packages.elastic.co/kibana/${KIBANA_MAJOR}/debian stable main" > /etc/apt/sources.list.d/kibana.list
```

-	Created: Tue, 24 May 2016 02:26:35 GMT
-	Parent Layer: `7b80c210be5b805e11d46e7d05d9e6cad145928993383f06860bce7b8dc61959`
-	v2 Blob: `sha256:013a2329a0487c5d73571fd7d3ada221fe258cb7beb7ea2f6d854825d493e411`
-	v2 Content-Length: 220.0 B
-	v2 Last-Modified: Tue, 31 May 2016 20:05:11 GMT

#### `e346ee327acec5b88dd382b598c0c1e932f279f06995fd15461355648d2e46e8`

```dockerfile
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends kibana=$KIBANA_VERSION 	&& chown -R kibana:kibana /opt/kibana 	&& rm -rf /var/lib/apt/lists/* 		&& sed -ri "s!^(\#\s*)?(elasticsearch\.url:).*!\2 'http://elasticsearch:9200'!" /opt/kibana/config/kibana.yml 	&& grep -q 'elasticsearch:9200' /opt/kibana/config/kibana.yml
```

-	Created: Tue, 24 May 2016 02:27:25 GMT
-	Parent Layer: `c8eae2c7363f1980c18852b8d2eccff42162ff2b7f77c3d75e7b86facc7d892c`
-	v2 Blob: `sha256:dd4834512d5798e34df6169dcb4453b5059295e130c684ed9ded7f734e68e9f7`
-	v2 Content-Length: 33.0 MB (33047898 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:05:06 GMT

#### `f73b75a104cd40027992f30233cc7f250df5106776e2d1763c4e535a6071b973`

```dockerfile
ENV PATH=/opt/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Created: Tue, 24 May 2016 02:27:32 GMT
-	Parent Layer: `e346ee327acec5b88dd382b598c0c1e932f279f06995fd15461355648d2e46e8`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `a6218e02df0b1343aa1150056edbeadfe44e77b480c49521e654d8fc2139332a`

```dockerfile
COPY file:19c1e8bb9b9b1bfd96fabd1909bec9f7fc0a0134c2a2712ac20b5d4dfeeccb80 in /
```

-	Created: Tue, 24 May 2016 02:27:33 GMT
-	Parent Layer: `f73b75a104cd40027992f30233cc7f250df5106776e2d1763c4e535a6071b973`
-	v2 Blob: `sha256:b40842db255aa7a6d423e4caec50388d2b6799bdd3f686d8b5f271bdd225d52e`
-	v2 Content-Length: 345.0 B
-	v2 Last-Modified: Thu, 12 May 2016 19:38:05 GMT

#### `371d87077b7997fcfc1e1ef538c4dc70ca1e7465c7ed9a47c12d71b3a88a38eb`

```dockerfile
EXPOSE 5601/tcp
```

-	Created: Tue, 24 May 2016 02:27:34 GMT
-	Parent Layer: `a6218e02df0b1343aa1150056edbeadfe44e77b480c49521e654d8fc2139332a`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `097fbe6ac7eede6f7617bf4477731dee25873f8dc68ffc749b3eea6caccb419d`

```dockerfile
ENTRYPOINT &{["/docker-entrypoint.sh"]}
```

-	Created: Tue, 24 May 2016 02:27:34 GMT
-	Parent Layer: `371d87077b7997fcfc1e1ef538c4dc70ca1e7465c7ed9a47c12d71b3a88a38eb`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `9e421b32701fdecf6b961b5e2f7014e24822146bda5585b14993ee9468f98a23`

```dockerfile
CMD ["kibana"]
```

-	Created: Tue, 24 May 2016 02:27:35 GMT
-	Parent Layer: `097fbe6ac7eede6f7617bf4477731dee25873f8dc68ffc749b3eea6caccb419d`
-	Docker Version: 1.9.1
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `kibana:4.4`

```console
$ docker pull library/kibana@sha256:046067a49ea48ef0bce62e452d9f3b0c40ac402dced216adce3d78cade615323
```

-	Total v2 Content-Length: 101.8 MB (101841896 bytes)

### Layers (18)

#### `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`

```dockerfile
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
```

-	Created: Mon, 23 May 2016 22:57:20 GMT
-	v2 Blob: `sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`
-	v2 Content-Length: 51.4 MB (51356334 bytes)
-	v2 Last-Modified: Mon, 23 May 2016 23:09:48 GMT

#### `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Mon, 23 May 2016 22:57:23 GMT
-	Parent Layer: `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`

```dockerfile
RUN groupadd -r kibana && useradd -r -m -g kibana kibana
```

-	Created: Tue, 24 May 2016 02:15:27 GMT
-	Parent Layer: `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`
-	v2 Blob: `sha256:ef236d3c18b4ce0744c2ae4b8ae7f442605c745fd7b10c65b441ed51682b2c5f`
-	v2 Content-Length: 4.3 KB (4342 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:56 GMT

#### `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`

```dockerfile
RUN apt-get update && apt-get install -y 		ca-certificates 		wget 	--no-install-recommends && rm -rf /var/lib/apt/lists/*
```

-	Created: Tue, 24 May 2016 02:16:12 GMT
-	Parent Layer: `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`
-	v2 Blob: `sha256:7b4763c5420742eed897623fc3fc72c5a54f1245ee6d50734ca70a012f60a753`
-	v2 Content-Length: 16.6 MB (16615966 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:53 GMT

#### `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`

```dockerfile
ENV GOSU_VERSION=1.7
```

-	Created: Tue, 24 May 2016 02:16:15 GMT
-	Parent Layer: `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
```

-	Created: Tue, 24 May 2016 02:16:21 GMT
-	Parent Layer: `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`
-	v2 Blob: `sha256:8d4b6aaf60cb73053140071b6910c2697c581367449734e64959c86f2619d14f`
-	v2 Content-Length: 807.9 KB (807931 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:43 GMT

#### `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`

```dockerfile
ENV TINI_VERSION=v0.9.0
```

-	Created: Tue, 24 May 2016 02:16:23 GMT
-	Parent Layer: `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
```

-	Created: Tue, 24 May 2016 02:16:29 GMT
-	Parent Layer: `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`
-	v2 Blob: `sha256:a69ada16019ca97e3e09836f89b4fa99cf84902554f4df7857bd852a372a7417`
-	v2 Content-Length: 7.1 KB (7121 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:38 GMT

#### `3ed696f09b1d5f406d763f15956349e40ede1914c5504b19fcd20ec96c4b2b1e`

```dockerfile
RUN apt-key adv --keyserver ha.pool.sks-keyservers.net --recv-keys 46095ACC8548582C1A2699A9D27D666CD88E42B4
```

-	Created: Tue, 24 May 2016 02:26:31 GMT
-	Parent Layer: `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`
-	v2 Blob: `sha256:bc20bd2597ed2f4e39d66072bac0322c025a28501ed7d3702ea59600425c5a5f`
-	v2 Content-Length: 1.5 KB (1451 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:05:23 GMT

#### `4fd95a9187de0a9dbf990d6fcdeb0cd04a19ffe8128cc77eb0438e38fe12e58b`

```dockerfile
ENV KIBANA_MAJOR=4.4
```

-	Created: Tue, 24 May 2016 02:26:32 GMT
-	Parent Layer: `3ed696f09b1d5f406d763f15956349e40ede1914c5504b19fcd20ec96c4b2b1e`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `7b80c210be5b805e11d46e7d05d9e6cad145928993383f06860bce7b8dc61959`

```dockerfile
ENV KIBANA_VERSION=4.4.2
```

-	Created: Tue, 24 May 2016 02:26:33 GMT
-	Parent Layer: `4fd95a9187de0a9dbf990d6fcdeb0cd04a19ffe8128cc77eb0438e38fe12e58b`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `c8eae2c7363f1980c18852b8d2eccff42162ff2b7f77c3d75e7b86facc7d892c`

```dockerfile
RUN echo "deb http://packages.elastic.co/kibana/${KIBANA_MAJOR}/debian stable main" > /etc/apt/sources.list.d/kibana.list
```

-	Created: Tue, 24 May 2016 02:26:35 GMT
-	Parent Layer: `7b80c210be5b805e11d46e7d05d9e6cad145928993383f06860bce7b8dc61959`
-	v2 Blob: `sha256:013a2329a0487c5d73571fd7d3ada221fe258cb7beb7ea2f6d854825d493e411`
-	v2 Content-Length: 220.0 B
-	v2 Last-Modified: Tue, 31 May 2016 20:05:11 GMT

#### `e346ee327acec5b88dd382b598c0c1e932f279f06995fd15461355648d2e46e8`

```dockerfile
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends kibana=$KIBANA_VERSION 	&& chown -R kibana:kibana /opt/kibana 	&& rm -rf /var/lib/apt/lists/* 		&& sed -ri "s!^(\#\s*)?(elasticsearch\.url:).*!\2 'http://elasticsearch:9200'!" /opt/kibana/config/kibana.yml 	&& grep -q 'elasticsearch:9200' /opt/kibana/config/kibana.yml
```

-	Created: Tue, 24 May 2016 02:27:25 GMT
-	Parent Layer: `c8eae2c7363f1980c18852b8d2eccff42162ff2b7f77c3d75e7b86facc7d892c`
-	v2 Blob: `sha256:dd4834512d5798e34df6169dcb4453b5059295e130c684ed9ded7f734e68e9f7`
-	v2 Content-Length: 33.0 MB (33047898 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:05:06 GMT

#### `f73b75a104cd40027992f30233cc7f250df5106776e2d1763c4e535a6071b973`

```dockerfile
ENV PATH=/opt/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Created: Tue, 24 May 2016 02:27:32 GMT
-	Parent Layer: `e346ee327acec5b88dd382b598c0c1e932f279f06995fd15461355648d2e46e8`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `a6218e02df0b1343aa1150056edbeadfe44e77b480c49521e654d8fc2139332a`

```dockerfile
COPY file:19c1e8bb9b9b1bfd96fabd1909bec9f7fc0a0134c2a2712ac20b5d4dfeeccb80 in /
```

-	Created: Tue, 24 May 2016 02:27:33 GMT
-	Parent Layer: `f73b75a104cd40027992f30233cc7f250df5106776e2d1763c4e535a6071b973`
-	v2 Blob: `sha256:b40842db255aa7a6d423e4caec50388d2b6799bdd3f686d8b5f271bdd225d52e`
-	v2 Content-Length: 345.0 B
-	v2 Last-Modified: Thu, 12 May 2016 19:38:05 GMT

#### `371d87077b7997fcfc1e1ef538c4dc70ca1e7465c7ed9a47c12d71b3a88a38eb`

```dockerfile
EXPOSE 5601/tcp
```

-	Created: Tue, 24 May 2016 02:27:34 GMT
-	Parent Layer: `a6218e02df0b1343aa1150056edbeadfe44e77b480c49521e654d8fc2139332a`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `097fbe6ac7eede6f7617bf4477731dee25873f8dc68ffc749b3eea6caccb419d`

```dockerfile
ENTRYPOINT &{["/docker-entrypoint.sh"]}
```

-	Created: Tue, 24 May 2016 02:27:34 GMT
-	Parent Layer: `371d87077b7997fcfc1e1ef538c4dc70ca1e7465c7ed9a47c12d71b3a88a38eb`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `9e421b32701fdecf6b961b5e2f7014e24822146bda5585b14993ee9468f98a23`

```dockerfile
CMD ["kibana"]
```

-	Created: Tue, 24 May 2016 02:27:35 GMT
-	Parent Layer: `097fbe6ac7eede6f7617bf4477731dee25873f8dc68ffc749b3eea6caccb419d`
-	Docker Version: 1.9.1
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `kibana:4.5.1`

```console
$ docker pull library/kibana@sha256:d1e2cbf8638c181cf1eb654c56987d8581c64897e6e9365bf182cd185974f364
```

-	Total v2 Content-Length: 102.4 MB (102394233 bytes)

### Layers (18)

#### `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`

```dockerfile
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
```

-	Created: Mon, 23 May 2016 22:57:20 GMT
-	v2 Blob: `sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`
-	v2 Content-Length: 51.4 MB (51356334 bytes)
-	v2 Last-Modified: Mon, 23 May 2016 23:09:48 GMT

#### `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Mon, 23 May 2016 22:57:23 GMT
-	Parent Layer: `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`

```dockerfile
RUN groupadd -r kibana && useradd -r -m -g kibana kibana
```

-	Created: Tue, 24 May 2016 02:15:27 GMT
-	Parent Layer: `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`
-	v2 Blob: `sha256:ef236d3c18b4ce0744c2ae4b8ae7f442605c745fd7b10c65b441ed51682b2c5f`
-	v2 Content-Length: 4.3 KB (4342 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:56 GMT

#### `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`

```dockerfile
RUN apt-get update && apt-get install -y 		ca-certificates 		wget 	--no-install-recommends && rm -rf /var/lib/apt/lists/*
```

-	Created: Tue, 24 May 2016 02:16:12 GMT
-	Parent Layer: `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`
-	v2 Blob: `sha256:7b4763c5420742eed897623fc3fc72c5a54f1245ee6d50734ca70a012f60a753`
-	v2 Content-Length: 16.6 MB (16615966 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:53 GMT

#### `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`

```dockerfile
ENV GOSU_VERSION=1.7
```

-	Created: Tue, 24 May 2016 02:16:15 GMT
-	Parent Layer: `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
```

-	Created: Tue, 24 May 2016 02:16:21 GMT
-	Parent Layer: `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`
-	v2 Blob: `sha256:8d4b6aaf60cb73053140071b6910c2697c581367449734e64959c86f2619d14f`
-	v2 Content-Length: 807.9 KB (807931 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:43 GMT

#### `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`

```dockerfile
ENV TINI_VERSION=v0.9.0
```

-	Created: Tue, 24 May 2016 02:16:23 GMT
-	Parent Layer: `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
```

-	Created: Tue, 24 May 2016 02:16:29 GMT
-	Parent Layer: `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`
-	v2 Blob: `sha256:a69ada16019ca97e3e09836f89b4fa99cf84902554f4df7857bd852a372a7417`
-	v2 Content-Length: 7.1 KB (7121 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:38 GMT

#### `3ed696f09b1d5f406d763f15956349e40ede1914c5504b19fcd20ec96c4b2b1e`

```dockerfile
RUN apt-key adv --keyserver ha.pool.sks-keyservers.net --recv-keys 46095ACC8548582C1A2699A9D27D666CD88E42B4
```

-	Created: Tue, 24 May 2016 02:26:31 GMT
-	Parent Layer: `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`
-	v2 Blob: `sha256:bc20bd2597ed2f4e39d66072bac0322c025a28501ed7d3702ea59600425c5a5f`
-	v2 Content-Length: 1.5 KB (1451 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:05:23 GMT

#### `4fd95a9187de0a9dbf990d6fcdeb0cd04a19ffe8128cc77eb0438e38fe12e58b`

```dockerfile
ENV KIBANA_MAJOR=4.4
```

-	Created: Tue, 24 May 2016 02:26:32 GMT
-	Parent Layer: `3ed696f09b1d5f406d763f15956349e40ede1914c5504b19fcd20ec96c4b2b1e`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `7b80c210be5b805e11d46e7d05d9e6cad145928993383f06860bce7b8dc61959`

```dockerfile
ENV KIBANA_VERSION=4.4.2
```

-	Created: Tue, 24 May 2016 02:26:33 GMT
-	Parent Layer: `4fd95a9187de0a9dbf990d6fcdeb0cd04a19ffe8128cc77eb0438e38fe12e58b`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `f84da64f1c13d8a6c9b465632115f2a008c2b56a6c164a8acd40c5fc06c548d5`

```dockerfile
RUN echo "deb http://packages.elastic.co/kibana/${KIBANA_MAJOR}/debian stable main" > /etc/apt/sources.list.d/kibana.list
```

-	Created: Tue, 24 May 2016 02:29:21 GMT
-	Parent Layer: `7b80c210be5b805e11d46e7d05d9e6cad145928993383f06860bce7b8dc61959`
-	v2 Blob: `sha256:a3400c76b9f2a19f57facf8449db8ce58eef204d7db9f86935a773ce8ab77584`
-	v2 Content-Length: 220.0 B
-	v2 Last-Modified: Tue, 31 May 2016 20:06:53 GMT

#### `87d4d68dc94b47ece493a5e1f6118b4da37e0e74efda37a0a2ff3def779ab656`

```dockerfile
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends kibana=$KIBANA_VERSION 	&& chown -R kibana:kibana /opt/kibana 	&& rm -rf /var/lib/apt/lists/* 		&& sed -ri "s!^(\#\s*)?(elasticsearch\.url:).*!\2 'http://elasticsearch:9200'!" /opt/kibana/config/kibana.yml 	&& grep -q 'elasticsearch:9200' /opt/kibana/config/kibana.yml
```

-	Created: Tue, 24 May 2016 02:30:05 GMT
-	Parent Layer: `f84da64f1c13d8a6c9b465632115f2a008c2b56a6c164a8acd40c5fc06c548d5`
-	v2 Blob: `sha256:40e44879562d98f5ab14301b8e694592bf2ac9775e9da3834a560269f66151f0`
-	v2 Content-Length: 33.6 MB (33600235 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:06:46 GMT

#### `8ca0987ce0f1c06c6130647c08bfa1ee0ab8b5f4978f38166d7395b0ba1fd9dd`

```dockerfile
ENV PATH=/opt/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Created: Tue, 24 May 2016 02:30:32 GMT
-	Parent Layer: `87d4d68dc94b47ece493a5e1f6118b4da37e0e74efda37a0a2ff3def779ab656`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `b57c883092731f3bf0098d061f4cf1c4e4fa0470d12f9e46369e8d141e221275`

```dockerfile
COPY file:19c1e8bb9b9b1bfd96fabd1909bec9f7fc0a0134c2a2712ac20b5d4dfeeccb80 in /
```

-	Created: Tue, 24 May 2016 02:30:33 GMT
-	Parent Layer: `8ca0987ce0f1c06c6130647c08bfa1ee0ab8b5f4978f38166d7395b0ba1fd9dd`
-	v2 Blob: `sha256:b40842db255aa7a6d423e4caec50388d2b6799bdd3f686d8b5f271bdd225d52e`
-	v2 Content-Length: 345.0 B
-	v2 Last-Modified: Thu, 12 May 2016 19:38:05 GMT

#### `b15f751d01d860daa45e0981e09366f2e6bed8ea36c72f7027b597f40cffa538`

```dockerfile
EXPOSE 5601/tcp
```

-	Created: Tue, 24 May 2016 02:30:34 GMT
-	Parent Layer: `b57c883092731f3bf0098d061f4cf1c4e4fa0470d12f9e46369e8d141e221275`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `28a65d5ae46c187e6d7253dd20033cc83ac22f152b1b20312a03362a2fdc3e37`

```dockerfile
ENTRYPOINT &{["/docker-entrypoint.sh"]}
```

-	Created: Tue, 24 May 2016 02:30:35 GMT
-	Parent Layer: `b15f751d01d860daa45e0981e09366f2e6bed8ea36c72f7027b597f40cffa538`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `32c1284c3b5189b54fb11eb00b7bd104911c5207c00751e7a77d320a89e437b9`

```dockerfile
CMD ["kibana"]
```

-	Created: Tue, 24 May 2016 02:30:36 GMT
-	Parent Layer: `28a65d5ae46c187e6d7253dd20033cc83ac22f152b1b20312a03362a2fdc3e37`
-	Docker Version: 1.9.1
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `kibana:4.5`

```console
$ docker pull library/kibana@sha256:2001ca8f8576ec0ed551fcded8ac335e927cdb8ddfc282b2f095914be95b91e2
```

-	Total v2 Content-Length: 102.4 MB (102394233 bytes)

### Layers (18)

#### `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`

```dockerfile
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
```

-	Created: Mon, 23 May 2016 22:57:20 GMT
-	v2 Blob: `sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`
-	v2 Content-Length: 51.4 MB (51356334 bytes)
-	v2 Last-Modified: Mon, 23 May 2016 23:09:48 GMT

#### `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Mon, 23 May 2016 22:57:23 GMT
-	Parent Layer: `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`

```dockerfile
RUN groupadd -r kibana && useradd -r -m -g kibana kibana
```

-	Created: Tue, 24 May 2016 02:15:27 GMT
-	Parent Layer: `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`
-	v2 Blob: `sha256:ef236d3c18b4ce0744c2ae4b8ae7f442605c745fd7b10c65b441ed51682b2c5f`
-	v2 Content-Length: 4.3 KB (4342 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:56 GMT

#### `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`

```dockerfile
RUN apt-get update && apt-get install -y 		ca-certificates 		wget 	--no-install-recommends && rm -rf /var/lib/apt/lists/*
```

-	Created: Tue, 24 May 2016 02:16:12 GMT
-	Parent Layer: `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`
-	v2 Blob: `sha256:7b4763c5420742eed897623fc3fc72c5a54f1245ee6d50734ca70a012f60a753`
-	v2 Content-Length: 16.6 MB (16615966 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:53 GMT

#### `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`

```dockerfile
ENV GOSU_VERSION=1.7
```

-	Created: Tue, 24 May 2016 02:16:15 GMT
-	Parent Layer: `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
```

-	Created: Tue, 24 May 2016 02:16:21 GMT
-	Parent Layer: `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`
-	v2 Blob: `sha256:8d4b6aaf60cb73053140071b6910c2697c581367449734e64959c86f2619d14f`
-	v2 Content-Length: 807.9 KB (807931 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:43 GMT

#### `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`

```dockerfile
ENV TINI_VERSION=v0.9.0
```

-	Created: Tue, 24 May 2016 02:16:23 GMT
-	Parent Layer: `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
```

-	Created: Tue, 24 May 2016 02:16:29 GMT
-	Parent Layer: `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`
-	v2 Blob: `sha256:a69ada16019ca97e3e09836f89b4fa99cf84902554f4df7857bd852a372a7417`
-	v2 Content-Length: 7.1 KB (7121 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:38 GMT

#### `3ed696f09b1d5f406d763f15956349e40ede1914c5504b19fcd20ec96c4b2b1e`

```dockerfile
RUN apt-key adv --keyserver ha.pool.sks-keyservers.net --recv-keys 46095ACC8548582C1A2699A9D27D666CD88E42B4
```

-	Created: Tue, 24 May 2016 02:26:31 GMT
-	Parent Layer: `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`
-	v2 Blob: `sha256:bc20bd2597ed2f4e39d66072bac0322c025a28501ed7d3702ea59600425c5a5f`
-	v2 Content-Length: 1.5 KB (1451 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:05:23 GMT

#### `4fd95a9187de0a9dbf990d6fcdeb0cd04a19ffe8128cc77eb0438e38fe12e58b`

```dockerfile
ENV KIBANA_MAJOR=4.4
```

-	Created: Tue, 24 May 2016 02:26:32 GMT
-	Parent Layer: `3ed696f09b1d5f406d763f15956349e40ede1914c5504b19fcd20ec96c4b2b1e`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `7b80c210be5b805e11d46e7d05d9e6cad145928993383f06860bce7b8dc61959`

```dockerfile
ENV KIBANA_VERSION=4.4.2
```

-	Created: Tue, 24 May 2016 02:26:33 GMT
-	Parent Layer: `4fd95a9187de0a9dbf990d6fcdeb0cd04a19ffe8128cc77eb0438e38fe12e58b`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `f84da64f1c13d8a6c9b465632115f2a008c2b56a6c164a8acd40c5fc06c548d5`

```dockerfile
RUN echo "deb http://packages.elastic.co/kibana/${KIBANA_MAJOR}/debian stable main" > /etc/apt/sources.list.d/kibana.list
```

-	Created: Tue, 24 May 2016 02:29:21 GMT
-	Parent Layer: `7b80c210be5b805e11d46e7d05d9e6cad145928993383f06860bce7b8dc61959`
-	v2 Blob: `sha256:a3400c76b9f2a19f57facf8449db8ce58eef204d7db9f86935a773ce8ab77584`
-	v2 Content-Length: 220.0 B
-	v2 Last-Modified: Tue, 31 May 2016 20:06:53 GMT

#### `87d4d68dc94b47ece493a5e1f6118b4da37e0e74efda37a0a2ff3def779ab656`

```dockerfile
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends kibana=$KIBANA_VERSION 	&& chown -R kibana:kibana /opt/kibana 	&& rm -rf /var/lib/apt/lists/* 		&& sed -ri "s!^(\#\s*)?(elasticsearch\.url:).*!\2 'http://elasticsearch:9200'!" /opt/kibana/config/kibana.yml 	&& grep -q 'elasticsearch:9200' /opt/kibana/config/kibana.yml
```

-	Created: Tue, 24 May 2016 02:30:05 GMT
-	Parent Layer: `f84da64f1c13d8a6c9b465632115f2a008c2b56a6c164a8acd40c5fc06c548d5`
-	v2 Blob: `sha256:40e44879562d98f5ab14301b8e694592bf2ac9775e9da3834a560269f66151f0`
-	v2 Content-Length: 33.6 MB (33600235 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:06:46 GMT

#### `8ca0987ce0f1c06c6130647c08bfa1ee0ab8b5f4978f38166d7395b0ba1fd9dd`

```dockerfile
ENV PATH=/opt/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Created: Tue, 24 May 2016 02:30:32 GMT
-	Parent Layer: `87d4d68dc94b47ece493a5e1f6118b4da37e0e74efda37a0a2ff3def779ab656`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `b57c883092731f3bf0098d061f4cf1c4e4fa0470d12f9e46369e8d141e221275`

```dockerfile
COPY file:19c1e8bb9b9b1bfd96fabd1909bec9f7fc0a0134c2a2712ac20b5d4dfeeccb80 in /
```

-	Created: Tue, 24 May 2016 02:30:33 GMT
-	Parent Layer: `8ca0987ce0f1c06c6130647c08bfa1ee0ab8b5f4978f38166d7395b0ba1fd9dd`
-	v2 Blob: `sha256:b40842db255aa7a6d423e4caec50388d2b6799bdd3f686d8b5f271bdd225d52e`
-	v2 Content-Length: 345.0 B
-	v2 Last-Modified: Thu, 12 May 2016 19:38:05 GMT

#### `b15f751d01d860daa45e0981e09366f2e6bed8ea36c72f7027b597f40cffa538`

```dockerfile
EXPOSE 5601/tcp
```

-	Created: Tue, 24 May 2016 02:30:34 GMT
-	Parent Layer: `b57c883092731f3bf0098d061f4cf1c4e4fa0470d12f9e46369e8d141e221275`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `28a65d5ae46c187e6d7253dd20033cc83ac22f152b1b20312a03362a2fdc3e37`

```dockerfile
ENTRYPOINT &{["/docker-entrypoint.sh"]}
```

-	Created: Tue, 24 May 2016 02:30:35 GMT
-	Parent Layer: `b15f751d01d860daa45e0981e09366f2e6bed8ea36c72f7027b597f40cffa538`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `32c1284c3b5189b54fb11eb00b7bd104911c5207c00751e7a77d320a89e437b9`

```dockerfile
CMD ["kibana"]
```

-	Created: Tue, 24 May 2016 02:30:36 GMT
-	Parent Layer: `28a65d5ae46c187e6d7253dd20033cc83ac22f152b1b20312a03362a2fdc3e37`
-	Docker Version: 1.9.1
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `kibana:4`

```console
$ docker pull library/kibana@sha256:13de6966f66671a79b0dc006311606ac7f19bdcb0e5b269c458fcfcd05ff4fdc
```

-	Total v2 Content-Length: 102.4 MB (102394233 bytes)

### Layers (18)

#### `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`

```dockerfile
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
```

-	Created: Mon, 23 May 2016 22:57:20 GMT
-	v2 Blob: `sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`
-	v2 Content-Length: 51.4 MB (51356334 bytes)
-	v2 Last-Modified: Mon, 23 May 2016 23:09:48 GMT

#### `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Mon, 23 May 2016 22:57:23 GMT
-	Parent Layer: `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`

```dockerfile
RUN groupadd -r kibana && useradd -r -m -g kibana kibana
```

-	Created: Tue, 24 May 2016 02:15:27 GMT
-	Parent Layer: `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`
-	v2 Blob: `sha256:ef236d3c18b4ce0744c2ae4b8ae7f442605c745fd7b10c65b441ed51682b2c5f`
-	v2 Content-Length: 4.3 KB (4342 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:56 GMT

#### `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`

```dockerfile
RUN apt-get update && apt-get install -y 		ca-certificates 		wget 	--no-install-recommends && rm -rf /var/lib/apt/lists/*
```

-	Created: Tue, 24 May 2016 02:16:12 GMT
-	Parent Layer: `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`
-	v2 Blob: `sha256:7b4763c5420742eed897623fc3fc72c5a54f1245ee6d50734ca70a012f60a753`
-	v2 Content-Length: 16.6 MB (16615966 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:53 GMT

#### `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`

```dockerfile
ENV GOSU_VERSION=1.7
```

-	Created: Tue, 24 May 2016 02:16:15 GMT
-	Parent Layer: `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
```

-	Created: Tue, 24 May 2016 02:16:21 GMT
-	Parent Layer: `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`
-	v2 Blob: `sha256:8d4b6aaf60cb73053140071b6910c2697c581367449734e64959c86f2619d14f`
-	v2 Content-Length: 807.9 KB (807931 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:43 GMT

#### `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`

```dockerfile
ENV TINI_VERSION=v0.9.0
```

-	Created: Tue, 24 May 2016 02:16:23 GMT
-	Parent Layer: `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
```

-	Created: Tue, 24 May 2016 02:16:29 GMT
-	Parent Layer: `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`
-	v2 Blob: `sha256:a69ada16019ca97e3e09836f89b4fa99cf84902554f4df7857bd852a372a7417`
-	v2 Content-Length: 7.1 KB (7121 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:38 GMT

#### `3ed696f09b1d5f406d763f15956349e40ede1914c5504b19fcd20ec96c4b2b1e`

```dockerfile
RUN apt-key adv --keyserver ha.pool.sks-keyservers.net --recv-keys 46095ACC8548582C1A2699A9D27D666CD88E42B4
```

-	Created: Tue, 24 May 2016 02:26:31 GMT
-	Parent Layer: `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`
-	v2 Blob: `sha256:bc20bd2597ed2f4e39d66072bac0322c025a28501ed7d3702ea59600425c5a5f`
-	v2 Content-Length: 1.5 KB (1451 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:05:23 GMT

#### `4fd95a9187de0a9dbf990d6fcdeb0cd04a19ffe8128cc77eb0438e38fe12e58b`

```dockerfile
ENV KIBANA_MAJOR=4.4
```

-	Created: Tue, 24 May 2016 02:26:32 GMT
-	Parent Layer: `3ed696f09b1d5f406d763f15956349e40ede1914c5504b19fcd20ec96c4b2b1e`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `7b80c210be5b805e11d46e7d05d9e6cad145928993383f06860bce7b8dc61959`

```dockerfile
ENV KIBANA_VERSION=4.4.2
```

-	Created: Tue, 24 May 2016 02:26:33 GMT
-	Parent Layer: `4fd95a9187de0a9dbf990d6fcdeb0cd04a19ffe8128cc77eb0438e38fe12e58b`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `f84da64f1c13d8a6c9b465632115f2a008c2b56a6c164a8acd40c5fc06c548d5`

```dockerfile
RUN echo "deb http://packages.elastic.co/kibana/${KIBANA_MAJOR}/debian stable main" > /etc/apt/sources.list.d/kibana.list
```

-	Created: Tue, 24 May 2016 02:29:21 GMT
-	Parent Layer: `7b80c210be5b805e11d46e7d05d9e6cad145928993383f06860bce7b8dc61959`
-	v2 Blob: `sha256:a3400c76b9f2a19f57facf8449db8ce58eef204d7db9f86935a773ce8ab77584`
-	v2 Content-Length: 220.0 B
-	v2 Last-Modified: Tue, 31 May 2016 20:06:53 GMT

#### `87d4d68dc94b47ece493a5e1f6118b4da37e0e74efda37a0a2ff3def779ab656`

```dockerfile
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends kibana=$KIBANA_VERSION 	&& chown -R kibana:kibana /opt/kibana 	&& rm -rf /var/lib/apt/lists/* 		&& sed -ri "s!^(\#\s*)?(elasticsearch\.url:).*!\2 'http://elasticsearch:9200'!" /opt/kibana/config/kibana.yml 	&& grep -q 'elasticsearch:9200' /opt/kibana/config/kibana.yml
```

-	Created: Tue, 24 May 2016 02:30:05 GMT
-	Parent Layer: `f84da64f1c13d8a6c9b465632115f2a008c2b56a6c164a8acd40c5fc06c548d5`
-	v2 Blob: `sha256:40e44879562d98f5ab14301b8e694592bf2ac9775e9da3834a560269f66151f0`
-	v2 Content-Length: 33.6 MB (33600235 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:06:46 GMT

#### `8ca0987ce0f1c06c6130647c08bfa1ee0ab8b5f4978f38166d7395b0ba1fd9dd`

```dockerfile
ENV PATH=/opt/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Created: Tue, 24 May 2016 02:30:32 GMT
-	Parent Layer: `87d4d68dc94b47ece493a5e1f6118b4da37e0e74efda37a0a2ff3def779ab656`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `b57c883092731f3bf0098d061f4cf1c4e4fa0470d12f9e46369e8d141e221275`

```dockerfile
COPY file:19c1e8bb9b9b1bfd96fabd1909bec9f7fc0a0134c2a2712ac20b5d4dfeeccb80 in /
```

-	Created: Tue, 24 May 2016 02:30:33 GMT
-	Parent Layer: `8ca0987ce0f1c06c6130647c08bfa1ee0ab8b5f4978f38166d7395b0ba1fd9dd`
-	v2 Blob: `sha256:b40842db255aa7a6d423e4caec50388d2b6799bdd3f686d8b5f271bdd225d52e`
-	v2 Content-Length: 345.0 B
-	v2 Last-Modified: Thu, 12 May 2016 19:38:05 GMT

#### `b15f751d01d860daa45e0981e09366f2e6bed8ea36c72f7027b597f40cffa538`

```dockerfile
EXPOSE 5601/tcp
```

-	Created: Tue, 24 May 2016 02:30:34 GMT
-	Parent Layer: `b57c883092731f3bf0098d061f4cf1c4e4fa0470d12f9e46369e8d141e221275`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `28a65d5ae46c187e6d7253dd20033cc83ac22f152b1b20312a03362a2fdc3e37`

```dockerfile
ENTRYPOINT &{["/docker-entrypoint.sh"]}
```

-	Created: Tue, 24 May 2016 02:30:35 GMT
-	Parent Layer: `b15f751d01d860daa45e0981e09366f2e6bed8ea36c72f7027b597f40cffa538`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `32c1284c3b5189b54fb11eb00b7bd104911c5207c00751e7a77d320a89e437b9`

```dockerfile
CMD ["kibana"]
```

-	Created: Tue, 24 May 2016 02:30:36 GMT
-	Parent Layer: `28a65d5ae46c187e6d7253dd20033cc83ac22f152b1b20312a03362a2fdc3e37`
-	Docker Version: 1.9.1
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `kibana:latest`

```console
$ docker pull library/kibana@sha256:a47c69cd430fab3047e705843e9f0c7f2bf5a85cd5bd5fa269e4f1027b24ea18
```

-	Total v2 Content-Length: 102.4 MB (102394233 bytes)

### Layers (18)

#### `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`

```dockerfile
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
```

-	Created: Mon, 23 May 2016 22:57:20 GMT
-	v2 Blob: `sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`
-	v2 Content-Length: 51.4 MB (51356334 bytes)
-	v2 Last-Modified: Mon, 23 May 2016 23:09:48 GMT

#### `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Mon, 23 May 2016 22:57:23 GMT
-	Parent Layer: `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`

```dockerfile
RUN groupadd -r kibana && useradd -r -m -g kibana kibana
```

-	Created: Tue, 24 May 2016 02:15:27 GMT
-	Parent Layer: `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`
-	v2 Blob: `sha256:ef236d3c18b4ce0744c2ae4b8ae7f442605c745fd7b10c65b441ed51682b2c5f`
-	v2 Content-Length: 4.3 KB (4342 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:56 GMT

#### `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`

```dockerfile
RUN apt-get update && apt-get install -y 		ca-certificates 		wget 	--no-install-recommends && rm -rf /var/lib/apt/lists/*
```

-	Created: Tue, 24 May 2016 02:16:12 GMT
-	Parent Layer: `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`
-	v2 Blob: `sha256:7b4763c5420742eed897623fc3fc72c5a54f1245ee6d50734ca70a012f60a753`
-	v2 Content-Length: 16.6 MB (16615966 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:53 GMT

#### `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`

```dockerfile
ENV GOSU_VERSION=1.7
```

-	Created: Tue, 24 May 2016 02:16:15 GMT
-	Parent Layer: `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
```

-	Created: Tue, 24 May 2016 02:16:21 GMT
-	Parent Layer: `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`
-	v2 Blob: `sha256:8d4b6aaf60cb73053140071b6910c2697c581367449734e64959c86f2619d14f`
-	v2 Content-Length: 807.9 KB (807931 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:43 GMT

#### `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`

```dockerfile
ENV TINI_VERSION=v0.9.0
```

-	Created: Tue, 24 May 2016 02:16:23 GMT
-	Parent Layer: `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
```

-	Created: Tue, 24 May 2016 02:16:29 GMT
-	Parent Layer: `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`
-	v2 Blob: `sha256:a69ada16019ca97e3e09836f89b4fa99cf84902554f4df7857bd852a372a7417`
-	v2 Content-Length: 7.1 KB (7121 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:38 GMT

#### `3ed696f09b1d5f406d763f15956349e40ede1914c5504b19fcd20ec96c4b2b1e`

```dockerfile
RUN apt-key adv --keyserver ha.pool.sks-keyservers.net --recv-keys 46095ACC8548582C1A2699A9D27D666CD88E42B4
```

-	Created: Tue, 24 May 2016 02:26:31 GMT
-	Parent Layer: `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`
-	v2 Blob: `sha256:bc20bd2597ed2f4e39d66072bac0322c025a28501ed7d3702ea59600425c5a5f`
-	v2 Content-Length: 1.5 KB (1451 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:05:23 GMT

#### `4fd95a9187de0a9dbf990d6fcdeb0cd04a19ffe8128cc77eb0438e38fe12e58b`

```dockerfile
ENV KIBANA_MAJOR=4.4
```

-	Created: Tue, 24 May 2016 02:26:32 GMT
-	Parent Layer: `3ed696f09b1d5f406d763f15956349e40ede1914c5504b19fcd20ec96c4b2b1e`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `7b80c210be5b805e11d46e7d05d9e6cad145928993383f06860bce7b8dc61959`

```dockerfile
ENV KIBANA_VERSION=4.4.2
```

-	Created: Tue, 24 May 2016 02:26:33 GMT
-	Parent Layer: `4fd95a9187de0a9dbf990d6fcdeb0cd04a19ffe8128cc77eb0438e38fe12e58b`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `f84da64f1c13d8a6c9b465632115f2a008c2b56a6c164a8acd40c5fc06c548d5`

```dockerfile
RUN echo "deb http://packages.elastic.co/kibana/${KIBANA_MAJOR}/debian stable main" > /etc/apt/sources.list.d/kibana.list
```

-	Created: Tue, 24 May 2016 02:29:21 GMT
-	Parent Layer: `7b80c210be5b805e11d46e7d05d9e6cad145928993383f06860bce7b8dc61959`
-	v2 Blob: `sha256:a3400c76b9f2a19f57facf8449db8ce58eef204d7db9f86935a773ce8ab77584`
-	v2 Content-Length: 220.0 B
-	v2 Last-Modified: Tue, 31 May 2016 20:06:53 GMT

#### `87d4d68dc94b47ece493a5e1f6118b4da37e0e74efda37a0a2ff3def779ab656`

```dockerfile
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends kibana=$KIBANA_VERSION 	&& chown -R kibana:kibana /opt/kibana 	&& rm -rf /var/lib/apt/lists/* 		&& sed -ri "s!^(\#\s*)?(elasticsearch\.url:).*!\2 'http://elasticsearch:9200'!" /opt/kibana/config/kibana.yml 	&& grep -q 'elasticsearch:9200' /opt/kibana/config/kibana.yml
```

-	Created: Tue, 24 May 2016 02:30:05 GMT
-	Parent Layer: `f84da64f1c13d8a6c9b465632115f2a008c2b56a6c164a8acd40c5fc06c548d5`
-	v2 Blob: `sha256:40e44879562d98f5ab14301b8e694592bf2ac9775e9da3834a560269f66151f0`
-	v2 Content-Length: 33.6 MB (33600235 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:06:46 GMT

#### `8ca0987ce0f1c06c6130647c08bfa1ee0ab8b5f4978f38166d7395b0ba1fd9dd`

```dockerfile
ENV PATH=/opt/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Created: Tue, 24 May 2016 02:30:32 GMT
-	Parent Layer: `87d4d68dc94b47ece493a5e1f6118b4da37e0e74efda37a0a2ff3def779ab656`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `b57c883092731f3bf0098d061f4cf1c4e4fa0470d12f9e46369e8d141e221275`

```dockerfile
COPY file:19c1e8bb9b9b1bfd96fabd1909bec9f7fc0a0134c2a2712ac20b5d4dfeeccb80 in /
```

-	Created: Tue, 24 May 2016 02:30:33 GMT
-	Parent Layer: `8ca0987ce0f1c06c6130647c08bfa1ee0ab8b5f4978f38166d7395b0ba1fd9dd`
-	v2 Blob: `sha256:b40842db255aa7a6d423e4caec50388d2b6799bdd3f686d8b5f271bdd225d52e`
-	v2 Content-Length: 345.0 B
-	v2 Last-Modified: Thu, 12 May 2016 19:38:05 GMT

#### `b15f751d01d860daa45e0981e09366f2e6bed8ea36c72f7027b597f40cffa538`

```dockerfile
EXPOSE 5601/tcp
```

-	Created: Tue, 24 May 2016 02:30:34 GMT
-	Parent Layer: `b57c883092731f3bf0098d061f4cf1c4e4fa0470d12f9e46369e8d141e221275`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `28a65d5ae46c187e6d7253dd20033cc83ac22f152b1b20312a03362a2fdc3e37`

```dockerfile
ENTRYPOINT &{["/docker-entrypoint.sh"]}
```

-	Created: Tue, 24 May 2016 02:30:35 GMT
-	Parent Layer: `b15f751d01d860daa45e0981e09366f2e6bed8ea36c72f7027b597f40cffa538`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `32c1284c3b5189b54fb11eb00b7bd104911c5207c00751e7a77d320a89e437b9`

```dockerfile
CMD ["kibana"]
```

-	Created: Tue, 24 May 2016 02:30:36 GMT
-	Parent Layer: `28a65d5ae46c187e6d7253dd20033cc83ac22f152b1b20312a03362a2fdc3e37`
-	Docker Version: 1.9.1
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `kibana:5.0.0-alpha3`

**does not exist** (yet?)

## `kibana:5.0.0`

```console
$ docker pull library/kibana@sha256:131f9e14230b58048f5b4ea686c53965bea2a604941a4dbbeb1edbb2e19bebc6
```

-	Total v2 Content-Length: 104.2 MB (104155252 bytes)

### Layers (18)

#### `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`

```dockerfile
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
```

-	Created: Mon, 23 May 2016 22:57:20 GMT
-	v2 Blob: `sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`
-	v2 Content-Length: 51.4 MB (51356334 bytes)
-	v2 Last-Modified: Mon, 23 May 2016 23:09:48 GMT

#### `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Mon, 23 May 2016 22:57:23 GMT
-	Parent Layer: `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`

```dockerfile
RUN groupadd -r kibana && useradd -r -m -g kibana kibana
```

-	Created: Tue, 24 May 2016 02:15:27 GMT
-	Parent Layer: `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`
-	v2 Blob: `sha256:ef236d3c18b4ce0744c2ae4b8ae7f442605c745fd7b10c65b441ed51682b2c5f`
-	v2 Content-Length: 4.3 KB (4342 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:56 GMT

#### `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`

```dockerfile
RUN apt-get update && apt-get install -y 		ca-certificates 		wget 	--no-install-recommends && rm -rf /var/lib/apt/lists/*
```

-	Created: Tue, 24 May 2016 02:16:12 GMT
-	Parent Layer: `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`
-	v2 Blob: `sha256:7b4763c5420742eed897623fc3fc72c5a54f1245ee6d50734ca70a012f60a753`
-	v2 Content-Length: 16.6 MB (16615966 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:53 GMT

#### `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`

```dockerfile
ENV GOSU_VERSION=1.7
```

-	Created: Tue, 24 May 2016 02:16:15 GMT
-	Parent Layer: `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
```

-	Created: Tue, 24 May 2016 02:16:21 GMT
-	Parent Layer: `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`
-	v2 Blob: `sha256:8d4b6aaf60cb73053140071b6910c2697c581367449734e64959c86f2619d14f`
-	v2 Content-Length: 807.9 KB (807931 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:43 GMT

#### `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`

```dockerfile
ENV TINI_VERSION=v0.9.0
```

-	Created: Tue, 24 May 2016 02:16:23 GMT
-	Parent Layer: `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
```

-	Created: Tue, 24 May 2016 02:16:29 GMT
-	Parent Layer: `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`
-	v2 Blob: `sha256:a69ada16019ca97e3e09836f89b4fa99cf84902554f4df7857bd852a372a7417`
-	v2 Content-Length: 7.1 KB (7121 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:38 GMT

#### `3ed696f09b1d5f406d763f15956349e40ede1914c5504b19fcd20ec96c4b2b1e`

```dockerfile
RUN apt-key adv --keyserver ha.pool.sks-keyservers.net --recv-keys 46095ACC8548582C1A2699A9D27D666CD88E42B4
```

-	Created: Tue, 24 May 2016 02:26:31 GMT
-	Parent Layer: `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`
-	v2 Blob: `sha256:bc20bd2597ed2f4e39d66072bac0322c025a28501ed7d3702ea59600425c5a5f`
-	v2 Content-Length: 1.5 KB (1451 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:05:23 GMT

#### `4fd95a9187de0a9dbf990d6fcdeb0cd04a19ffe8128cc77eb0438e38fe12e58b`

```dockerfile
ENV KIBANA_MAJOR=4.4
```

-	Created: Tue, 24 May 2016 02:26:32 GMT
-	Parent Layer: `3ed696f09b1d5f406d763f15956349e40ede1914c5504b19fcd20ec96c4b2b1e`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `7b80c210be5b805e11d46e7d05d9e6cad145928993383f06860bce7b8dc61959`

```dockerfile
ENV KIBANA_VERSION=4.4.2
```

-	Created: Tue, 24 May 2016 02:26:33 GMT
-	Parent Layer: `4fd95a9187de0a9dbf990d6fcdeb0cd04a19ffe8128cc77eb0438e38fe12e58b`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `b048240e37ae8d93ab45ed18b36733ecff0292f2f43c787222298cd6f9073baa`

```dockerfile
RUN echo 'deb http://packages.elastic.co/kibana/5.0.0-alpha/debian stable main' > /etc/apt/sources.list.d/kibana.list
```

-	Created: Tue, 24 May 2016 02:35:25 GMT
-	Parent Layer: `7b80c210be5b805e11d46e7d05d9e6cad145928993383f06860bce7b8dc61959`
-	v2 Blob: `sha256:5ee4ba164769db361e6b415528ef3ab91e09760736d1bfefd7778f71a90f1913`
-	v2 Content-Length: 229.0 B
-	v2 Last-Modified: Tue, 31 May 2016 20:08:51 GMT

#### `b05b42c0205b192fa503cc4318933442c3722a8235e2e0bcbc3e43a93489ffeb`

```dockerfile
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends kibana=$KIBANA_VERSION 	&& chown -R kibana:kibana /opt/kibana 	&& rm -rf /var/lib/apt/lists/* 		&& sed -ri "s!^(\#\s*)?(elasticsearch\.url:).*!\2 'http://elasticsearch:9200'!" /opt/kibana/config/kibana.yml 	&& grep -q 'elasticsearch:9200' /opt/kibana/config/kibana.yml
```

-	Created: Tue, 24 May 2016 02:36:18 GMT
-	Parent Layer: `b048240e37ae8d93ab45ed18b36733ecff0292f2f43c787222298cd6f9073baa`
-	v2 Blob: `sha256:bf06539faf901ee0fcde44ed1437f75615f769a258516999b2a593971b0da4ee`
-	v2 Content-Length: 35.4 MB (35361245 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:08:45 GMT

#### `7cf8924c6c6a90fe39d99d6bbddff10c45aa76b001bc6e8fcfba31864d9a9413`

```dockerfile
ENV PATH=/opt/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Created: Tue, 24 May 2016 02:36:28 GMT
-	Parent Layer: `b05b42c0205b192fa503cc4318933442c3722a8235e2e0bcbc3e43a93489ffeb`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `53dc3a560e8eaf55e528919bed5d1486bd11dbfe5e4a6dd314bbdf3a46889c2b`

```dockerfile
COPY file:19c1e8bb9b9b1bfd96fabd1909bec9f7fc0a0134c2a2712ac20b5d4dfeeccb80 in /
```

-	Created: Tue, 24 May 2016 02:36:29 GMT
-	Parent Layer: `7cf8924c6c6a90fe39d99d6bbddff10c45aa76b001bc6e8fcfba31864d9a9413`
-	v2 Blob: `sha256:b40842db255aa7a6d423e4caec50388d2b6799bdd3f686d8b5f271bdd225d52e`
-	v2 Content-Length: 345.0 B
-	v2 Last-Modified: Thu, 12 May 2016 19:38:05 GMT

#### `b383d543a56cfd665d0ebb5637915c8ab63cc7d8fa5424f987165d32585389e3`

```dockerfile
EXPOSE 5601/tcp
```

-	Created: Tue, 24 May 2016 02:36:31 GMT
-	Parent Layer: `53dc3a560e8eaf55e528919bed5d1486bd11dbfe5e4a6dd314bbdf3a46889c2b`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `0361c0e5040798684e5225d46ad83ab4e8c9bfb41ad89d8477dd2def89aa6b15`

```dockerfile
ENTRYPOINT &{["/docker-entrypoint.sh"]}
```

-	Created: Tue, 24 May 2016 02:36:32 GMT
-	Parent Layer: `b383d543a56cfd665d0ebb5637915c8ab63cc7d8fa5424f987165d32585389e3`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `1167af45bbbf161590e1dd8332816047ef18c05c1e1f0c8f5ada01f94eee18f3`

```dockerfile
CMD ["kibana"]
```

-	Created: Tue, 24 May 2016 02:36:33 GMT
-	Parent Layer: `0361c0e5040798684e5225d46ad83ab4e8c9bfb41ad89d8477dd2def89aa6b15`
-	Docker Version: 1.9.1
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `kibana:5.0`

```console
$ docker pull library/kibana@sha256:0b3f9e051b8d0c4dd67c69d29fd2f4a11650be3c830bcaa6aa9f4db5b344af1d
```

-	Total v2 Content-Length: 104.2 MB (104155252 bytes)

### Layers (18)

#### `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`

```dockerfile
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
```

-	Created: Mon, 23 May 2016 22:57:20 GMT
-	v2 Blob: `sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`
-	v2 Content-Length: 51.4 MB (51356334 bytes)
-	v2 Last-Modified: Mon, 23 May 2016 23:09:48 GMT

#### `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Mon, 23 May 2016 22:57:23 GMT
-	Parent Layer: `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`

```dockerfile
RUN groupadd -r kibana && useradd -r -m -g kibana kibana
```

-	Created: Tue, 24 May 2016 02:15:27 GMT
-	Parent Layer: `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`
-	v2 Blob: `sha256:ef236d3c18b4ce0744c2ae4b8ae7f442605c745fd7b10c65b441ed51682b2c5f`
-	v2 Content-Length: 4.3 KB (4342 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:56 GMT

#### `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`

```dockerfile
RUN apt-get update && apt-get install -y 		ca-certificates 		wget 	--no-install-recommends && rm -rf /var/lib/apt/lists/*
```

-	Created: Tue, 24 May 2016 02:16:12 GMT
-	Parent Layer: `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`
-	v2 Blob: `sha256:7b4763c5420742eed897623fc3fc72c5a54f1245ee6d50734ca70a012f60a753`
-	v2 Content-Length: 16.6 MB (16615966 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:53 GMT

#### `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`

```dockerfile
ENV GOSU_VERSION=1.7
```

-	Created: Tue, 24 May 2016 02:16:15 GMT
-	Parent Layer: `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
```

-	Created: Tue, 24 May 2016 02:16:21 GMT
-	Parent Layer: `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`
-	v2 Blob: `sha256:8d4b6aaf60cb73053140071b6910c2697c581367449734e64959c86f2619d14f`
-	v2 Content-Length: 807.9 KB (807931 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:43 GMT

#### `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`

```dockerfile
ENV TINI_VERSION=v0.9.0
```

-	Created: Tue, 24 May 2016 02:16:23 GMT
-	Parent Layer: `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
```

-	Created: Tue, 24 May 2016 02:16:29 GMT
-	Parent Layer: `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`
-	v2 Blob: `sha256:a69ada16019ca97e3e09836f89b4fa99cf84902554f4df7857bd852a372a7417`
-	v2 Content-Length: 7.1 KB (7121 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:38 GMT

#### `3ed696f09b1d5f406d763f15956349e40ede1914c5504b19fcd20ec96c4b2b1e`

```dockerfile
RUN apt-key adv --keyserver ha.pool.sks-keyservers.net --recv-keys 46095ACC8548582C1A2699A9D27D666CD88E42B4
```

-	Created: Tue, 24 May 2016 02:26:31 GMT
-	Parent Layer: `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`
-	v2 Blob: `sha256:bc20bd2597ed2f4e39d66072bac0322c025a28501ed7d3702ea59600425c5a5f`
-	v2 Content-Length: 1.5 KB (1451 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:05:23 GMT

#### `4fd95a9187de0a9dbf990d6fcdeb0cd04a19ffe8128cc77eb0438e38fe12e58b`

```dockerfile
ENV KIBANA_MAJOR=4.4
```

-	Created: Tue, 24 May 2016 02:26:32 GMT
-	Parent Layer: `3ed696f09b1d5f406d763f15956349e40ede1914c5504b19fcd20ec96c4b2b1e`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `7b80c210be5b805e11d46e7d05d9e6cad145928993383f06860bce7b8dc61959`

```dockerfile
ENV KIBANA_VERSION=4.4.2
```

-	Created: Tue, 24 May 2016 02:26:33 GMT
-	Parent Layer: `4fd95a9187de0a9dbf990d6fcdeb0cd04a19ffe8128cc77eb0438e38fe12e58b`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `b048240e37ae8d93ab45ed18b36733ecff0292f2f43c787222298cd6f9073baa`

```dockerfile
RUN echo 'deb http://packages.elastic.co/kibana/5.0.0-alpha/debian stable main' > /etc/apt/sources.list.d/kibana.list
```

-	Created: Tue, 24 May 2016 02:35:25 GMT
-	Parent Layer: `7b80c210be5b805e11d46e7d05d9e6cad145928993383f06860bce7b8dc61959`
-	v2 Blob: `sha256:5ee4ba164769db361e6b415528ef3ab91e09760736d1bfefd7778f71a90f1913`
-	v2 Content-Length: 229.0 B
-	v2 Last-Modified: Tue, 31 May 2016 20:08:51 GMT

#### `b05b42c0205b192fa503cc4318933442c3722a8235e2e0bcbc3e43a93489ffeb`

```dockerfile
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends kibana=$KIBANA_VERSION 	&& chown -R kibana:kibana /opt/kibana 	&& rm -rf /var/lib/apt/lists/* 		&& sed -ri "s!^(\#\s*)?(elasticsearch\.url:).*!\2 'http://elasticsearch:9200'!" /opt/kibana/config/kibana.yml 	&& grep -q 'elasticsearch:9200' /opt/kibana/config/kibana.yml
```

-	Created: Tue, 24 May 2016 02:36:18 GMT
-	Parent Layer: `b048240e37ae8d93ab45ed18b36733ecff0292f2f43c787222298cd6f9073baa`
-	v2 Blob: `sha256:bf06539faf901ee0fcde44ed1437f75615f769a258516999b2a593971b0da4ee`
-	v2 Content-Length: 35.4 MB (35361245 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:08:45 GMT

#### `7cf8924c6c6a90fe39d99d6bbddff10c45aa76b001bc6e8fcfba31864d9a9413`

```dockerfile
ENV PATH=/opt/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Created: Tue, 24 May 2016 02:36:28 GMT
-	Parent Layer: `b05b42c0205b192fa503cc4318933442c3722a8235e2e0bcbc3e43a93489ffeb`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `53dc3a560e8eaf55e528919bed5d1486bd11dbfe5e4a6dd314bbdf3a46889c2b`

```dockerfile
COPY file:19c1e8bb9b9b1bfd96fabd1909bec9f7fc0a0134c2a2712ac20b5d4dfeeccb80 in /
```

-	Created: Tue, 24 May 2016 02:36:29 GMT
-	Parent Layer: `7cf8924c6c6a90fe39d99d6bbddff10c45aa76b001bc6e8fcfba31864d9a9413`
-	v2 Blob: `sha256:b40842db255aa7a6d423e4caec50388d2b6799bdd3f686d8b5f271bdd225d52e`
-	v2 Content-Length: 345.0 B
-	v2 Last-Modified: Thu, 12 May 2016 19:38:05 GMT

#### `b383d543a56cfd665d0ebb5637915c8ab63cc7d8fa5424f987165d32585389e3`

```dockerfile
EXPOSE 5601/tcp
```

-	Created: Tue, 24 May 2016 02:36:31 GMT
-	Parent Layer: `53dc3a560e8eaf55e528919bed5d1486bd11dbfe5e4a6dd314bbdf3a46889c2b`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `0361c0e5040798684e5225d46ad83ab4e8c9bfb41ad89d8477dd2def89aa6b15`

```dockerfile
ENTRYPOINT &{["/docker-entrypoint.sh"]}
```

-	Created: Tue, 24 May 2016 02:36:32 GMT
-	Parent Layer: `b383d543a56cfd665d0ebb5637915c8ab63cc7d8fa5424f987165d32585389e3`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `1167af45bbbf161590e1dd8332816047ef18c05c1e1f0c8f5ada01f94eee18f3`

```dockerfile
CMD ["kibana"]
```

-	Created: Tue, 24 May 2016 02:36:33 GMT
-	Parent Layer: `0361c0e5040798684e5225d46ad83ab4e8c9bfb41ad89d8477dd2def89aa6b15`
-	Docker Version: 1.9.1
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

## `kibana:5`

```console
$ docker pull library/kibana@sha256:e7ed9ff535f883a5095213989a2a41ca5c64c290c735edda079c3c98383c377b
```

-	Total v2 Content-Length: 104.2 MB (104155252 bytes)

### Layers (18)

#### `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`

```dockerfile
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
```

-	Created: Mon, 23 May 2016 22:57:20 GMT
-	v2 Blob: `sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`
-	v2 Content-Length: 51.4 MB (51356334 bytes)
-	v2 Last-Modified: Mon, 23 May 2016 23:09:48 GMT

#### `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`

```dockerfile
CMD ["/bin/bash"]
```

-	Created: Mon, 23 May 2016 22:57:23 GMT
-	Parent Layer: `a2295636c7aa7aeaaf8aba834ed7a9863a2a8f3e87464c8ab9bd659d4d668687`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`

```dockerfile
RUN groupadd -r kibana && useradd -r -m -g kibana kibana
```

-	Created: Tue, 24 May 2016 02:15:27 GMT
-	Parent Layer: `3035387b9e834c466cd957662b14b5548c7b2bed1fc8057a2e80793bddd04d92`
-	v2 Blob: `sha256:ef236d3c18b4ce0744c2ae4b8ae7f442605c745fd7b10c65b441ed51682b2c5f`
-	v2 Content-Length: 4.3 KB (4342 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:56 GMT

#### `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`

```dockerfile
RUN apt-get update && apt-get install -y 		ca-certificates 		wget 	--no-install-recommends && rm -rf /var/lib/apt/lists/*
```

-	Created: Tue, 24 May 2016 02:16:12 GMT
-	Parent Layer: `47bdb96797fad2536d29298e4166f9d35a778ffbddd53db60c7e48fdcda2662f`
-	v2 Blob: `sha256:7b4763c5420742eed897623fc3fc72c5a54f1245ee6d50734ca70a012f60a753`
-	v2 Content-Length: 16.6 MB (16615966 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:53 GMT

#### `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`

```dockerfile
ENV GOSU_VERSION=1.7
```

-	Created: Tue, 24 May 2016 02:16:15 GMT
-	Parent Layer: `71abc8a00350a12c6f22f5bec3f06c67d37712d1e0ee3b1ea89d156bdbf44035`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
```

-	Created: Tue, 24 May 2016 02:16:21 GMT
-	Parent Layer: `d1f59305d1c3b167bffbe34e61a0aa2dadf74eb58f95d378f28c116aacc62c09`
-	v2 Blob: `sha256:8d4b6aaf60cb73053140071b6910c2697c581367449734e64959c86f2619d14f`
-	v2 Content-Length: 807.9 KB (807931 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:43 GMT

#### `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`

```dockerfile
ENV TINI_VERSION=v0.9.0
```

-	Created: Tue, 24 May 2016 02:16:23 GMT
-	Parent Layer: `a4f1d60170962bc0fffced86ca84ba5ba8498044ac0c55ee6c61c36713178b42`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`

```dockerfile
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
```

-	Created: Tue, 24 May 2016 02:16:29 GMT
-	Parent Layer: `c4d72aa1dcfb3b461ee19f52120505acc069ff521d183e428ad094bf0e7e597a`
-	v2 Blob: `sha256:a69ada16019ca97e3e09836f89b4fa99cf84902554f4df7857bd852a372a7417`
-	v2 Content-Length: 7.1 KB (7121 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:00:38 GMT

#### `3ed696f09b1d5f406d763f15956349e40ede1914c5504b19fcd20ec96c4b2b1e`

```dockerfile
RUN apt-key adv --keyserver ha.pool.sks-keyservers.net --recv-keys 46095ACC8548582C1A2699A9D27D666CD88E42B4
```

-	Created: Tue, 24 May 2016 02:26:31 GMT
-	Parent Layer: `786e73e201edd581f64315e301c3efbc2cf7f9d38978bb0bc37ba5449189a6f7`
-	v2 Blob: `sha256:bc20bd2597ed2f4e39d66072bac0322c025a28501ed7d3702ea59600425c5a5f`
-	v2 Content-Length: 1.5 KB (1451 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:05:23 GMT

#### `4fd95a9187de0a9dbf990d6fcdeb0cd04a19ffe8128cc77eb0438e38fe12e58b`

```dockerfile
ENV KIBANA_MAJOR=4.4
```

-	Created: Tue, 24 May 2016 02:26:32 GMT
-	Parent Layer: `3ed696f09b1d5f406d763f15956349e40ede1914c5504b19fcd20ec96c4b2b1e`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `7b80c210be5b805e11d46e7d05d9e6cad145928993383f06860bce7b8dc61959`

```dockerfile
ENV KIBANA_VERSION=4.4.2
```

-	Created: Tue, 24 May 2016 02:26:33 GMT
-	Parent Layer: `4fd95a9187de0a9dbf990d6fcdeb0cd04a19ffe8128cc77eb0438e38fe12e58b`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `b048240e37ae8d93ab45ed18b36733ecff0292f2f43c787222298cd6f9073baa`

```dockerfile
RUN echo 'deb http://packages.elastic.co/kibana/5.0.0-alpha/debian stable main' > /etc/apt/sources.list.d/kibana.list
```

-	Created: Tue, 24 May 2016 02:35:25 GMT
-	Parent Layer: `7b80c210be5b805e11d46e7d05d9e6cad145928993383f06860bce7b8dc61959`
-	v2 Blob: `sha256:5ee4ba164769db361e6b415528ef3ab91e09760736d1bfefd7778f71a90f1913`
-	v2 Content-Length: 229.0 B
-	v2 Last-Modified: Tue, 31 May 2016 20:08:51 GMT

#### `b05b42c0205b192fa503cc4318933442c3722a8235e2e0bcbc3e43a93489ffeb`

```dockerfile
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends kibana=$KIBANA_VERSION 	&& chown -R kibana:kibana /opt/kibana 	&& rm -rf /var/lib/apt/lists/* 		&& sed -ri "s!^(\#\s*)?(elasticsearch\.url:).*!\2 'http://elasticsearch:9200'!" /opt/kibana/config/kibana.yml 	&& grep -q 'elasticsearch:9200' /opt/kibana/config/kibana.yml
```

-	Created: Tue, 24 May 2016 02:36:18 GMT
-	Parent Layer: `b048240e37ae8d93ab45ed18b36733ecff0292f2f43c787222298cd6f9073baa`
-	v2 Blob: `sha256:bf06539faf901ee0fcde44ed1437f75615f769a258516999b2a593971b0da4ee`
-	v2 Content-Length: 35.4 MB (35361245 bytes)
-	v2 Last-Modified: Tue, 31 May 2016 20:08:45 GMT

#### `7cf8924c6c6a90fe39d99d6bbddff10c45aa76b001bc6e8fcfba31864d9a9413`

```dockerfile
ENV PATH=/opt/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Created: Tue, 24 May 2016 02:36:28 GMT
-	Parent Layer: `b05b42c0205b192fa503cc4318933442c3722a8235e2e0bcbc3e43a93489ffeb`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `53dc3a560e8eaf55e528919bed5d1486bd11dbfe5e4a6dd314bbdf3a46889c2b`

```dockerfile
COPY file:19c1e8bb9b9b1bfd96fabd1909bec9f7fc0a0134c2a2712ac20b5d4dfeeccb80 in /
```

-	Created: Tue, 24 May 2016 02:36:29 GMT
-	Parent Layer: `7cf8924c6c6a90fe39d99d6bbddff10c45aa76b001bc6e8fcfba31864d9a9413`
-	v2 Blob: `sha256:b40842db255aa7a6d423e4caec50388d2b6799bdd3f686d8b5f271bdd225d52e`
-	v2 Content-Length: 345.0 B
-	v2 Last-Modified: Thu, 12 May 2016 19:38:05 GMT

#### `b383d543a56cfd665d0ebb5637915c8ab63cc7d8fa5424f987165d32585389e3`

```dockerfile
EXPOSE 5601/tcp
```

-	Created: Tue, 24 May 2016 02:36:31 GMT
-	Parent Layer: `53dc3a560e8eaf55e528919bed5d1486bd11dbfe5e4a6dd314bbdf3a46889c2b`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `0361c0e5040798684e5225d46ad83ab4e8c9bfb41ad89d8477dd2def89aa6b15`

```dockerfile
ENTRYPOINT &{["/docker-entrypoint.sh"]}
```

-	Created: Tue, 24 May 2016 02:36:32 GMT
-	Parent Layer: `b383d543a56cfd665d0ebb5637915c8ab63cc7d8fa5424f987165d32585389e3`
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

#### `1167af45bbbf161590e1dd8332816047ef18c05c1e1f0c8f5ada01f94eee18f3`

```dockerfile
CMD ["kibana"]
```

-	Created: Tue, 24 May 2016 02:36:33 GMT
-	Parent Layer: `0361c0e5040798684e5225d46ad83ab4e8c9bfb41ad89d8477dd2def89aa6b15`
-	Docker Version: 1.9.1
-	v2 Blob: `sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`
-	v2 Content-Length: 32.0 B
-	v2 Last-Modified: Sat, 14 Nov 2015 09:09:44 GMT

# B08H51JHS1-5.6-image

# 実行結果（書籍の内容を一部修正）

```bash
$ circleci local execute 
Docker image digest: sha256:2c2fd6a4655b259ac40f3c168b82200d4a7cebdc8287c4eb866a348b0191403d
====>> Spin Up Environment
Build-agent version  ()
Docker Engine Version: 20.10.1
Kernel Version: Linux 07cc56cb526b 5.4.0-1035-aws #37-Ubuntu SMP Wed Jan 6 21:01:57 UTC 2021 x86_64 Linux
Starting container cimg/node:lts
  image is cached as cimg/node:lts, but refreshing...
lts: Pulling from cimg/node
Digest: sha256:f6ab0eb78b007434b722a3a5b9345010d5a4a0ec5a7aa4acf802aa2d88fb0090
Status: Image is up to date for cimg/node:lts
  using image cimg/node@sha256:f6ab0eb78b007434b722a3a5b9345010d5a4a0ec5a7aa4acf802aa2d88fb0090
Starting container circleci/postgres:9.6
  image is cached as circleci/postgres:9.6, but refreshing...
9.6: Pulling from circleci/postgres
Digest: sha256:d2ae0212326a264bdd1896831b64b01db3faa4a8bf019272500dca3871a27f62
Status: Image is up to date for circleci/postgres:9.6
  using image circleci/postgres@sha256:d2ae0212326a264bdd1896831b64b01db3faa4a8bf019272500dca3871a27f62
====>> Container circleci/postgres:9.6
====>> Preparing Environment Variables
Using build environment variables:
  BASH_ENV=/tmp/.bash_env-localbuild-1611994173
  CI=true
  CIRCLECI=true
  CIRCLE_BRANCH=main
  CIRCLE_BUILD_NUM=
  CIRCLE_JOB=build
  CIRCLE_NODE_INDEX=0
  CIRCLE_NODE_TOTAL=1
  CIRCLE_REPOSITORY_URL=git@github.com:ys-office/B08H51JHS1-5.6-image.git
  CIRCLE_SHA1=a687ead359061a4af1749287788df79346a057bb
  CIRCLE_SHELL_ENV=/tmp/.bash_env-localbuild-1611994173
  CIRCLE_WORKING_DIRECTORY=~/project


The redacted variables listed above will be masked in run step output.====>> プライマリイメージで定義された環境変数を利用する
  #!/bin/bash -eo pipefail
echo "NODE_ENV is '${NODE_ENV}'"
NODE_ENV is 'production'
====>> ステップで同名の環境変数を定義すると上書きされる
  #!/bin/bash -eo pipefail
echo "NODE_ENV is '${NODE_ENV}'"
NODE_ENV is 'test'
====>> サービスイメージの環境変数はステップでは利用できない
  #!/bin/bash -eo pipefail
echo "POSTGRES_USER is '${POSTGRES_USER}'"
POSTGRES_USER is ''
Success!
Step canceled
```

# エラー発生

```bash
$ circleci local execute 
Docker image digest: sha256:2c2fd6a4655b259ac40f3c168b82200d4a7cebdc8287c4eb866a348b0191403d
====>> Spin Up Environment
Build-agent version  ()
Docker Engine Version: 20.10.1
Kernel Version: Linux a289ba9b5fa4 5.4.0-1035-aws #37-Ubuntu SMP Wed Jan 6 21:01:57 UTC 2021 x86_64 Linux
Starting container cimg/node:lts
  image is cached as cimg/node:lts, but refreshing...
lts: Pulling from cimg/node
Digest: sha256:f6ab0eb78b007434b722a3a5b9345010d5a4a0ec5a7aa4acf802aa2d88fb0090
Status: Image is up to date for cimg/node:lts
  using image cimg/node@sha256:f6ab0eb78b007434b722a3a5b9345010d5a4a0ec5a7aa4acf802aa2d88fb0090
Starting container circleci/postgres:9.6
  image cache not found on this host, downloading circleci/postgres:9.6
9.6: Pulling from circleci/postgres
8aff230071c9: Pulling fs layer
4b7067af43b3: Pulling fs layer
a684c6c57155: Pulling fs layer
0e8492701cf8: Pulling fs layer
72314d9ef34e: Pulling fs layer
90cb19bedf37: Pulling fs layer
ccd3c8b3474d: Pulling fs layer
a13817e9decd: Pulling fs layer
714e7575e26d: Pulling fs layer
17d4aaea5ce1: Pulling fs layer
60a212a2a820: Pulling fs layer
007e5a8598c9: Pulling fs layer
b98754cc6a3d: Pulling fs layer
4185f5074760: Pulling fs layer
98d0a2d40ad1: Pulling fs layer
714e7575e26d: Waiting
17d4aaea5ce1: Waiting
60a212a2a820: Waiting
007e5a8598c9: Waiting
b98754cc6a3d: Waiting
4185f5074760: Waiting
98d0a2d40ad1: Waiting
72314d9ef34e: Waiting
0e8492701cf8: Waiting
90cb19bedf37: Waiting
ccd3c8b3474d: Waiting
a13817e9decd: Waiting
a684c6c57155: Verifying Checksum
a684c6c57155: Download complete
4b7067af43b3: Verifying Checksum
4b7067af43b3: Download complete
8aff230071c9: Verifying Checksum
8aff230071c9: Download complete
0e8492701cf8: Verifying Checksum
0e8492701cf8: Download complete
72314d9ef34e: Verifying Checksum
72314d9ef34e: Download complete
90cb19bedf37: Verifying Checksum
90cb19bedf37: Download complete
8aff230071c9: Pull complete
ccd3c8b3474d: Verifying Checksum
ccd3c8b3474d: Download complete
4b7067af43b3: Pull complete
a13817e9decd: Verifying Checksum
a13817e9decd: Download complete
a684c6c57155: Pull complete
0e8492701cf8: Pull complete
714e7575e26d: Verifying Checksum
714e7575e26d: Download complete
17d4aaea5ce1: Verifying Checksum
17d4aaea5ce1: Download complete
72314d9ef34e: Pull complete
60a212a2a820: Verifying Checksum
60a212a2a820: Download complete
90cb19bedf37: Pull complete
ccd3c8b3474d: Pull complete
a13817e9decd: Pull complete
b98754cc6a3d: Verifying Checksum
b98754cc6a3d: Download complete
007e5a8598c9: Verifying Checksum
007e5a8598c9: Download complete
4185f5074760: Verifying Checksum
4185f5074760: Download complete
98d0a2d40ad1: Verifying Checksum
98d0a2d40ad1: Download complete
714e7575e26d: Pull complete
17d4aaea5ce1: Pull complete
60a212a2a820: Pull complete
007e5a8598c9: Pull complete
b98754cc6a3d: Pull complete
4185f5074760: Pull complete
98d0a2d40ad1: Pull complete
Digest: sha256:d2ae0212326a264bdd1896831b64b01db3faa4a8bf019272500dca3871a27f62
Status: Downloaded newer image for circleci/postgres:9.6
  using image circleci/postgres@sha256:d2ae0212326a264bdd1896831b64b01db3faa4a8bf019272500dca3871a27f62
====>> Container circleci/postgres:9.6
Error: Database is uninitialized and superuser password is not specified.
       You must specify POSTGRES_PASSWORD to a non-empty value for the
       superuser. For example, "-e POSTGRES_PASSWORD=password" on "docker run".

       You may also use "POSTGRES_HOST_AUTH_METHOD=trust" to allow all
       connections without a password. This is *not* recommended.

       See PostgreSQL documentation about "trust":
       https://www.postgresql.org/docs/current/auth-trust.html
Error: 
Exited with code 1

Step failed
```

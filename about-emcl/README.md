# about emcl
emclとは上田隆一先生が作成した自己位置推定に用いられるROSパッケージである．ソースコードを読むためにはC++を一通り理解していることが求められる．このREADMEはそのディレクトリの構成とemclのソースコードについて説明することを目的とする．
## treeによるディレクトリ構成の表示
ワーキングディレクトリには8個のファイルやディレクトリがある．8個一つ一つについて説明する．
* CMakeList.txtは，パッケージを作成するときに自動で作成されるファイルである．
* COPYINGは，準拠しているライセンスを示している．
* README.mdは，githubにおいて最初に読むべきものとされているファイルである．
* includeは，
* launchは，ROSにおいて複数のノードを一斉に起動するファイルがあるディレクトリである．
* package.xmlは，パッケージを作成するときに自動で作成されるファイルである．依存パッケージが記述されている．
* srcは，C++を用いたROSパッケージにおいては主なソースコードがあるディレクトリである．
* testは，様々なテストをするためのディレクトリである．

## 以上8つの事項を踏まえて自己位置推定用のパッケージとして見たときに読むべきディレクトリはsrcとlaunchとincludeの3つである．

以下はtreeコマンドによりemclをワーキングディレクトリとしたときの標準出力である．また，7個のディレクトリと32のファイルがある．
% t                                                                             [~/GIT/emcl][master]
.
├── ./CMakeLists.txt
├── ./COPYING
├── ./README.md
├── ./include
│   └── ./include/emcl
│       ├── ./include/emcl/ExpResetMcl.h
│       ├── ./include/emcl/LikelihoodFieldMap.h
│       ├── ./include/emcl/Mcl.h
│       ├── ./include/emcl/OdomModel.h
│       ├── ./include/emcl/Particle.h
│       ├── ./include/emcl/Pose.h
│       ├── ./include/emcl/Scan.h
│       ├── ./include/emcl/emcl_node.h
│       └── ./include/emcl/mcl_node.h
├── ./launch
│   ├── ./launch/emcl.launch
│   ├── ./launch/emclnav.launch
│   ├── ./launch/mcl.launch
│   └── ./launch/mclnav.launch
├── ./package.xml
├── ./src
│   ├── ./src/ExpResetMcl.cpp
│   ├── ./src/LikelihoodFieldMap.cpp
│   ├── ./src/Mcl.cpp
│   ├── ./src/OdomModel.cpp
│   ├── ./src/Particle.cpp
│   ├── ./src/Pose.cpp
│   ├── ./src/Scan.cpp
│   ├── ./src/emcl_node.cpp
│   └── ./src/mcl_node.cpp
└── ./test
    ├── ./test/docker
    │   └── ./test/docker/Dockerfile
    ├── ./test/docker_env
    │   └── ./test/docker_env/Dockerfile
    ├── ./test/test.bash
    ├── ./test/test.launch
    ├── ./test/test_gui.bash
    └── ./test/test_gui.launch

7 directories, 32 files


[](上のやつ写真にすべき)

# References
* https://github.com/ryuichiueda/emcl
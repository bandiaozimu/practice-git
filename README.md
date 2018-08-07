![Image of Yaktocat](https://i.imgur.com/TtYjVo8.jpg)
![Image of Yaktocat](https://i.imgur.com/P2YcA5Z.jpg)

同人音声资料库系统
-----------------------
之前我承诺会发一个同人音声脚本的帖，现在来填坑。会写这个程式是因为爬虫脚本每天都爬下1~10GB不等的作品，跟本没法都听完，想去芜存菁。
简单介绍这程式的作用，就是网站爬虫，下载，统一命名，选妃，转档，加封面，加Tag，汇入iTunes，建立播放清单都全自动化的一条龙服务。

在看这帖之前，先声明：如果你的系统不是OSX，完全不会shell script，甚至没用过command line，请坐车离开。
31b7ed5ef3e50ddc0c365a45534b4c3c9b9a1322

如果没被吓走，就来GitHub
https://github.com/bandiaozimu/dj_voice_organize

为避免过多的爬虫对网站造成攻击，我没把爬虫脚本放在里面，若能发Pull requests作出任何有用的小修小改，我私下给。
另外，我开了三个issues，如果能解任一个，我送1.77TB的资料。

功能
-----------------------
1. 整理作品统一档名，目录规则，重复的作品不删档并于档名后加“-1”“-2”以此类推。
2. 建立资料库，纪录作品的发行社团，属性标签，声优。各作品下载数，每新增200次更新一次属性标签。
3. 解压缩，转档，封面，id3 tag，汇入iTunes，一键完成。
4. 配合Wunderlist建立推荐清单，可定制推荐机制。
5. 可与JDownloader，FlexGet 对接，爬虫-下载-整理-筛选-汇入itunes全自动化。
6. 配合Wunderlist的推播功能，可在下载完成推送通知，还可筛选推送的作品。
7. 本程式支持主机／客户端的配置方式，即主机运行 FlexGet，JDownloader，及保存作品资料；
   客户端运行解压缩，转档，封面，id3 tag，汇入iTunes。
8. 本程式会将属性标签(调教/中出し/ナース...等) 嵌入id3 tag的“注解”中，方便iTues建立智慧播放清单。

![Image of Yaktocat](https://i.imgur.com/K5dpv8L.jpg)
![Image of Yaktocat](https://i.imgur.com/NutkgUX.png)
![Image of Yaktocat](https://i.imgur.com/WP6r4n0.png)

环境
-----------------------
1. 本程式目前只对OSX做过调适。

2. 本程式需要以下perl 模组，都可在cpan上找到：

    - Web::Query;
    - JSON;
    - Encode;
    - DBI;
    - Data::Dumper;
    - File::Copy;
    - File::Basename;
    - File::Find ();
    - File::chdir;
    - Getopt::Std;
    - List::Util qw( min max );
    - DateTime;


3. 本程式需要以下程式协同运行：

    - atomicparsley
    - eyeD3
    - ffmpeg + fdk-aac
    - sqlite
    - gnu-sed
    - realpath
    - perl
    - curl


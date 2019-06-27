<template>
  <div id="app">
        <el-container style="background-color: #f5f7f9">
            <el-aside width="700px" style="position: fixed">
                <el-row class="tac" type="flex" justify="end">
                    <el-col :span="8">
                        <el-card style="border-width: 0px;border-radius: 0px" body-style="background-color:black;color:#fff;font-size:22px;padding:30px;">
                            木秀于林的博客
                        </el-card>
                        <el-menu
                                default-active="2"
                                class="el-menu-vertical-demo"
                                align="left"
                                style="border-radius: 1px">
                            <el-menu-item index="1">
                                <i class="el-icon-s-home" style="color: #222"></i>
                                <span>首页</span>
                            </el-menu-item>
                            <el-menu-item index="2">
                                <i class="el-icon-user-solid" style="color: #222"></i>
                                <span slot="title">关于</span>
                            </el-menu-item>
                            <el-menu-item index="3">
                                <i class="el-icon-s-grid" style="color: #222"></i>
                                <span slot="title">分类</span>
                            </el-menu-item>
                            <el-menu-item index="4">
                                <i class="el-icon-s-claim" style="color: #222"></i>
                                <span slot="title">归档</span>
                            </el-menu-item>
                        </el-menu>
                        <el-card body-style="padding:20px" align="center" style="margin-top: 10px">

                            <h1 style="margin: 5px">木秀于林</h1>
                            <span style="margin: 0px;font-size: 14px;color: #999">从现在开始改变</span>
                            <br>
                            <el-row justify="center">
                                <el-col :span="12"  style="margin-top:10px;font-size: 15px;color: #555;" >
                                    <img src="https://img.icons8.com/material-outlined/20/000000/github.png" style="vertical-align: middle" alt="github-logo">
                                    <el-link style="vertical-align: middle" href="https://github.com/wangwenwwx" > GitHub</el-link>
                                </el-col>
                                <el-col :span="12"  style="margin-top:10px;font-size: 15px;color: #555;" >
                                    <i class="el-icon-s-comment" style="color: #222;vertical-align: middle"></i>
                                    <el-link style="vertical-align: middle" href="https://www.zhihu.com/people/muxiuyulin"> 知乎</el-link>
                                </el-col>
                            </el-row>
                        </el-card>
                    </el-col>
                </el-row>
            </el-aside>
            <el-main style="padding-top: 0px;margin-left: 700px">
                <el-row>
                    <el-col :span="16">
                        <el-card body-style="text-align:left;padding:40px">
                            <p>title: 运行官方demo flutter_gallery
                                date: 2018-03-31 22:33:01
                                tags: flutter
                                -</p>
                            <h1 id="centerflutter-运行官方demo-fluttergallerycenter"><center>flutter 运行官方demo “flutter——gallery”</center></h1>
                            <p>&emsp;&emsp;最近开始学习flutter,在导入官方demo“flutter——gallery”时，先是package&ensp;get一直失败</p>
                            <pre><code class="language-[flutter_gallery]">Running &quot;flutter packages get&quot; in flutter_gallery...
Git error. Command: git fetch
fatal: Not a git repository (or any of the parent directories): .git
pub get failed (69) -- attempting retry 1 in 1 second...
Git error. Command: git fetch
fatal: Not a git repository (or any of the parent directories): .git
pub get failed (69) -- attempting retry 2 in 2 seconds...</code></pre>
                            <p>将pubspec.ymal中</p>
                            <pre><code>flutter_gallery_assets:
    git:
      url: https://flutter.googlesource.com/gallery-assets//修改为https://gitee.com/creatint/gallery-assets.git
      ref: d318485f208376e06d7e330d9f191141d14722b8</code></pre><p>修改了pubspec.ymal后package&ensp;get成功，但运行时又报了一大堆不认识的错误，心态爆炸。</p>
                            <pre><code>* Error running Gradle:
Exit code 1 from: C:\Android\flutter\examples\flutter_gallery\android\gradlew.bat app:properties:
Starting a Gradle Daemon, 1 incompatible and 1 stopped Daemons could not be reused, use --status for details


FAILURE: Build failed with an exception.

* Where:
Script &#39;C:\Android\flutter\packages\flutter_tools\gradle\flutter.gradle&#39; line: 194

* What went wrong:
A problem occurred configuring project &#39;:connectivity&#39;.
&gt; Could not find method debugProvided() for arguments [file collection] on object of type org.gradle.api.internal.artifacts.dsl.dependencies.DefaultDependencyHandler.

* Try:
Run with --stacktrace option to get the stack trace. Run with --info or --debug option to get more log output.

* Get more help at https://help.gradle.org

BUILD FAILED in 13s

Please review your Gradle project setup in the android/ folder.</code></pre><p>因为我能力有限，无法解决，最后建了个新项目，把demo的lib目录和修改好的pubspec.ymal复制过去，成功运行。</p>

                        </el-card>
                    </el-col>
                </el-row>
            </el-main>
        </el-container>
    </div>
</template>

<script>
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>

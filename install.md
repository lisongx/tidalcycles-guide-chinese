You can install TidalCycles on MacOS, Windows, and Linux. Locate the instructions
below for your specific operating system.

你可以在MacOS、Windows和Linux下安装**TidalCycles**

* [MacOS](#macos)
* [Windows](#windows)
* [Linux](#linux)



## macOS

### 1. 要求

你需要首先安装以下软件：Haskell, Atom, SuperCollider。你可以从他们的网站下载，点击以下链接去安装每个软件。

* [Haskell](https://www.haskell.org/platform/)
* [Atom](https://atom.io/)
* [SuperCollider](http://supercollider.github.io/download) (最新版本3.9.3)
* 你可能需要安装 [Git](https://git-scm.com/)

<!-- You will need the SuperCollider sc3-plugins for using many of the synths included in
SuperDirt. Most of the examples in the documentation will still work, so you could
skip this step and return to it later. You can install the latest version from
[github](https://github.com/supercollider/sc3-plugins) according to
the instructions there. -->

### 2. 安装 TidalCycles

>**NOTE** As of September 26 2017, There appears to be an issue with Cabal that is
>affecting installation on MacOS.  
>If you are unable to install TidalCycles with the directions below, please try
>these alternate installation instructions. From a terminal window, run this:

>~~~~bash
>stack setup
>stack install tidal
>~~~~

>Once that's done, you'll also need to change a configuration setting
>in Atom. Find the package settings for TidalCycles (*preferences >
>tidalcycles > settings*). Change the ```'ghci path'``` option to this:

>```stack ghci```

>Restart Atom and it should be able to start TidalCycles.

>**Skip ahead to MacOS Step #3 (Install the SuperDirt synth) if you used this method**

#### 标准Mac OS安装:

打开终端输入以下命令安装TidalCycles:

~~~~bash
cabal install tidal
~~~~

> 如果你不知道如何打开终端，在Mac OS下是 实用工具 下的 终端


### 3. 安装SuperDirt

打开SuperCollider，在编辑器窗口复制以下代码：

~~~~c
include("SuperDirt")
~~~~

通过一下方式执行这行代码：确保指针在这行代码所在的行，然后按下shift的同时按回车（enter）。

这时将会开始下载SuperDirt，在结束时你会看到右下角的窗口显示：

~~~~c
... the class library may have to be recompiled.
-> SuperDirt
~~~~

此时，你需要重启SuperCollider(或者，点击 "Language" 下的 "Recompile Class Library").

如果你看到这条信息：

~~~~c
  "ERROR: Quarks requires git to be installed"
~~~~

你需要在此安装Git：
[https://git-scm.com/downloads](https://git-scm.com/downloads)，然后回到 SuperCollider 去执行 `include("SuperDirt")` 。


### 4. 安装TidalCycles的Atom插件

开启 Atom 编辑器，在菜单中选择 `edit > settings > install` , 然后在搜索框中输入 “tidalcycles”。一旦安装成功，重启 Atom 。

## Windows

### 1. Prerequisites

You first need to install the following three pieces of software,
Haskell, Atom, and SuperCollider. You can download them from their
websites - click on each of the below:

* [Haskell](https://www.haskell.org/platform/)
* [Atom](https://atom.io/)
* [SuperCollider](http://supercollider.github.io/download) (version 3.7 or later)
* You may also need to install [Git](https://git-scm.com/)

**Important:** Make sure you follow Step 2 of the Haskell
installation [instructions](https://www.haskell.org/platform/#windows).

**Important:** When installing SuperCollider, you must also download the `sc3-plugins`
zip file. Run SuperCollider once in order to create user directories. Then open
the zip file and extract the `SC3plugins` directory to
`C:\Users\<username>\AppData\Local\SuperCollider\Extensions`. You may have to
manually create the `Extensions` directory. Restart SuperCollider so that it finds
the `SC3plugins` directory.

### 2. Install the TidalCycles pattern engine

Open a Terminal window and type in the following command, to install
TidalCycles:

~~~~bash
cabal install tidal
~~~~

> If you're unsure how to open a terminal window: in Windows it's
> "command prompt" under Accessories


### 3. Install the SuperDirt synth

Start SuperCollider, and in the editor window paste in the following line of code:

~~~~c
include("SuperDirt")
~~~~

Run the code by clicking on it, to make sure the cursor is on this
line, then hold down shift and press enter.

It will download SuperDirt and
you will see it has completed when the Post Window displays:

~~~~c
... the class library may have to be recompiled.
-> SuperDirt
~~~~

After it has completed, you will need to restart SuperCollider (or
alternatively, recompile the class library via the "Language" menu).

If you instead see a message like this:

~~~~c
  "ERROR: Quarks requires git to be installed"
~~~~

Then you will need install git from
[https://git-scm.com/downloads](https://git-scm.com/downloads), and
return to SuperCollider to run `include("SuperDirt")` again.

### 4. Install the TidalCycles Atom plugin

Start Atom, and install the TidalCycles plugin. You can find it via
the menus under `edit > settings > install`, then typing “tidalcycles”
into the search box. Once that's installed, restart atom.

<a id="linux">&nbsp;</a>
<hr class="marker">

## Linux

### 1. Prerequisites

你需要首先安装以下软件：

[Haskell Stack](https://www.haskellstack.org/),
[Atom](https://atom.io/),
[SuperCollider](http://supercollider.github.io/download) and
[Git](https://git-scm.com/).

Hopefully your Linux distribution makes these easily available to you
via a package manager. For example, if you are using recent version of
Ubuntu or similar, you can install supercollider and haskell with the
following command in a terminal window:

```
sudo apt-get install supercollider sc3-plugins haskell-stack git
```

Make sure the supercollider version is 3.7 or later. If it isn't
available in your Linux distribution, then you may have to compile a
newer version yourself, or upgrade your distribution.

### 2. Install the TidalCycles pattern engine

Open a Terminal window and type in the following command, to install
TidalCycles:

~~~~bash
stack install tidal
~~~~

> If you're unsure how to open a terminal window in Linux,
> it varies according to distribution but generally find
> "Terminal" in the menus).

### 3. Install the SuperDirt synth

Start SuperCollider (e.g. by typing `scide` in a terminal window, or
finding it in your menus), and in the editor window paste in the
following line of code:

~~~~c
include("SuperDirt")
~~~~

Run the code by clicking on it, to make sure the cursor is on this
line, then hold down shift and press enter.

It will download SuperDirt and a fairly large bank of default samples,
so might take quite a while. You will see it has completed when the
Post Window displays:

~~~~c
... the class library may have to be recompiled.
-> SuperDirt
~~~~

After it has completed, you will need to restart SuperCollider (or
alternatively, recompile the class library via the "Language" menu).

If you instead see a message like this:

~~~~c
  "ERROR: Quarks requires git to be installed"
~~~~

Then you will need install 'git', which you should be able to do via
your linux distribution's package manager.

### 4. Install the TidalCycles Atom plugin

Start Atom, and install the TidalCycles plugin. You can find it via
the menus under `edit > settings > install`, then typing “tidalcycles”
into the search box.

There is one configuration option that you will need to change. Go to
`edit -> preferences`, then `packages` and find the settings for
tidalcycles. Change the 'Ghci path' setting to read: `stack ghci`.

Once that's done, restart atom.

**That's it!** You're now ready to start TidalCycles and SuperDirt for
  the first time.

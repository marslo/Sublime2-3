Sublime Configure
==========

The configuration about Sublime 2 AND 3 in both linux and windows

# Ubuntu
## Configuration:
- Sublime 2
    - Copy the `Packages/*` to `$HOME/.config/sublime-text-2/Packages`
- Sublime 3
    - Copy `Ubuntu/sublime-text-3/.config/sublime-text-3` to `~/.config`


## Packages
Press `Ctrl + Shift + p` to open **Anything Panel**
- SublimeCodeIntel
- Vintage
- VintageEx
- [ConvertToUTF8](https://github.com/seanliang/ConvertToUTF8)
- [GBK Encoding Support](https://github.com/akira-cn/sublime-gbk)
- [Navigation History](https://github.com/timjrobinson/SublimeNavigationHistory)
- [GotoLastEdit](https://github.com/khrizt/GotoLastEdit)

### Package Installation
- [OpenSearchResult](https://github.com/abrookins/OpenSearchResult)
    <pre><code>$ git clone https://github.com/abrookins/OpenSearchResult.git ~/.config/sublime-text-3/Packages</code></pre>
- [Theme - Marslo](https://github.com/Marslo/marslo-theme)
    <pre><code>$ cd ~/.config/sublime-text-3/Packages
    $ git clone https://github.com/Marslo/marslo-theme.git "Theme - Marslo"</code></pre>

## Installation
- Download: http://www.sublimetext.com/
- Sublime2 Installation:
<pre><code># add-apt-repository ppa:webupd8team/sublime-text-2
$ sudo apt-get update;
$ sudo apt-get sublime-text-dev
</code></pre>
- Package Contrl Installation:
    - For Sublime2:
        - Press <code>Ctrl + `</code>
        - Input the following and press `Enter`:
        <pre><code>import urllib2,os; pf='Package Control.sublime-package'; ipp=sublime.installed_packages_path(); os.makedirs(ipp) if not os.path.exists(ipp) else None; urllib2.install_opener(urllib2.build_opener(urllib2.ProxyHandler())); open(os.path.join(ipp,pf),'wb').write(urllib2.urlopen('http://sublime.wbond.net/'+pf.replace(' ','%20')).read()); print('Please restart Sublime Text to finish installation')
        </code></pre>
    - For Sublime3:
        - Press <code>Ctrl + `</code>
        - Input the following code and press `Enter`:
        <pre><code>import urllib.request,os; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); open(os.path.join(ipp, pf), 'wb').write(urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ','%20')).read())
        </code></pre>
        - Older method:
        <pre><code>$ cd Packages/
        $ git clone https://github.com/wbond/sublime_package_control.git "Package Control"
        $ cd "Package Control"
        $ git checkout python3
        </code></pre>

## Crack (Sublime2):
- Open the execution file by binary:
<pre><code># vim -d /usr/lib/sublime-text-2/sublime_text
</code></pre>
- Change strings:
    - input:          `:%!xdd`
    - Search:         `/3342 3032`
    - Change to:      3242 3042
<pre><code>:%s/3342 3032/3242 3042/
</code></pre>
- Save and exit
<pre><code>:!xxd -r
:x
</code></pre>
- Open **Sublime** -> **Help** -> **Enter License**, and paste following contents [ALL of them]:
<pre><code>〞每BEGIN LICENSE〞每
hiwanz
Unlimited User License
EA7E-26838
5B320641E6E11F5C6E16553C438A6839
72BA70FE439203367920D70E7DEB0E92
436D756177BBE49EFC9FBBB3420DB9D3
6AA8307E845B6AB8AF99D81734EEA961
02402C853F1FFF9854D94799D1317F37
1DAB52730F6CADDE701BF3BE03C34EF2
85E053D2B5E16502F4B009DE413591DE
0840D6E2CBF0A3049E2FAD940A53FF67
〞每END LICENSE〞每
</code></pre>

# Windows (Win7)
## Installation
- Download(Sublime3Beta): http://www.sublimetext.com/3
- Package Control Installation (Reference: http://wbond.net/sublime_packages/package_control/installation#ST3):
    - Installation by manually:
        - Download git
        - Clone https://github.com/wbond/sublime_package_control.git as "Package Control" in foler **%appdata%\Sublime Text 3\Packages**
        For Example: <pre><code>$ cd /c/user/\<LOGINNAME\>/AppData/Roaming/Sublime\ Text\ 3/Packages
        $ git clone https://github.com/wbond/sublime_package_control.git "Package Control"
        $ cd "Package Control"
        $ git checkout python3
        </code></pre>
    - Installation by automation:
        - <code>ctrl + `</code>
        - Input:
        <pre><code>import urllib.request,os; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); open(os.path.join(ipp, pf), 'wb').write(urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ','%20')).read())
        </code></pre>

## Use specified configurations and themes:
- Copy all files in foler **Win7(Sublime3Beta)** to local path `%appdata%\Sublime Text 3\Packages`
- Restart Sublime 3

## Installed Packages:
- [Package Control](https://github.com/wbond/sublime_package_control)
- VintageEX
- Theme - Soda
- [ConvertToUTF8](https://github.com/seanliang/ConvertToUTF8)
- [GBK Encoding Support](https://github.com/akira-cn/sublime-gbk)
- [Vintageous](https://github.com/guillermooo/Vintageous)
- [Navigation History](https://github.com/timjrobinson/SublimeNavigationHistory)
- [GotoLastEdit](https://github.com/khrizt/GotoLastEdit)
- [OpenSearchResult](https://github.com/abrookins/OpenSearchResult)
- [Ctags](https://github.com/SublimeText/CTags)

## Shortcut Mapping
- `,x`: toggle comment
- `cmd`: Open Command and cd to the current file path
- `alt + shift + j`: navigation history back
- `alt + shift + l`: navigation history forward
- `alt + k`: scroll line (up)
- `alt + j`: scroll line (down)
- `alt + l`: go to next view
- `alt + h`: go to previous view
- `alt + b`: backward word (Emacs shortcut)
- `alt + f`: forward word (Emacs shortcut)
- `ctrl + ]`: navigation to definition
- `ctrl + t`: navigation jump back
- `ctrl + e`: go to the end of line (Emacs shortcut)
- `ctrl + a`: go to the beginning of line (Emacs shortcut)
- `ctrl + alt + o`: Open the file browser and to current directory

# Screenshot:
## Ubuntu
![Ubuntu_Sublime3](https://github.com/woainvzu/Sublime2and3_Config_Marslo/blob/master/Screenshot/sublime3screenshot_Marslo.png?raw=true)
## Windows:
![Sublime3BetaWin7](https://github.com/woainvzu/Sublime2_Config_Marslo/blob/master/Screenshot/Sublime3win7.png?raw=true)

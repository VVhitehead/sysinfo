<h2>System monitor extension for Argos with real CPU graph</h2>

This is a fork of an extension created specially for [Argos](https://github.com/p-e-w/argos) and linux-powered computers w/ GNOME shell.
This script uses power of SVG to draw charts.

As you see at screenshot, CPU chart has 3 colors: green for iowait consumption, dark grey for user comsumption, and light gray for overall CPU consumption.

Please note that the CPU consumption is approximate. It calculates by **/proc/stat** output, also as memory by **free**, temperature by **/sys/class/thermal/thermal_zone0/temp** and disks by **df** outputs.

This specific fork has visual and other tweaks most suitable 4 arch with dark gnome theme and will probably need to be retweaked for other combinations of distros and themes.

<h2>Known bugs</h2>

Different configurations of **top** utility provides different output.
You may need to open the script and replace `$7 / 4` to `$n / 4` where n is the %CPU column numbered value for the given process. Also you may need to change `head -n 19` to `head -n 15`(line 86), depending on the number of your CPU cores (2 to 4 for most CPU's). In case you don't have swap or are missing another field try `head -n 18` or `head -n 14`.

<h2>Screenshot</h2>

![](https://raw.githubusercontent.com/WhiteheadV/sysinfo/master/screen.jpg)

<h2>License</h2>
GNU GPL v3.0 - https://www.gnu.org/licenses/gpl-3.0.en.html

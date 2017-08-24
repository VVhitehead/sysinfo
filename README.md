<h2>System monitor extension for Argos with real CPU graph</h2>

This is a fork of an extension created specially for [Argos](https://github.com/p-e-w/argos) and linux-powered computers w/ GNOME shell.
This script uses power of SVG to draw charts.

As you see at screenshot, CPU chart has 3 colors: green for iowait consumption, dark grey for user comsumption, and light gray for overall CPU consumption.

Please note that the CPU consumption is approximate. It calculates by **/proc/stat** output, also as memory by **free**, temperature by **/sys/class/thermal/thermal_zone0/temp** and disks by **df** outputs.

This specific fork has visual and other tweaks most suitable 4 arch with dark gnome theme and will probably need to be retweaked for other combinations of distros and themes.

<h3>Known bugs</h3>

Different configurations of **top** utility doesn't allow to show processes and it's CPU consumtion (see opened issue here).
To fix this, open script in text editor and replace `$9 / 2` to `$7 / 2`. Also you may need to change `head -n 10` to `head -n 13`.
Also, you may need to change number of CPU cores (2, 4).
In case your **top** is not configured to sort processes by CPU usage, refer to the top(no phun intented) answer to [this](https://unix.stackexchange.com/questions/158584/change-tops-sorting-back-to-cpu) related question.
<h2>Screenshot</h2>

![](https://raw.githubusercontent.com/WhiteheadV/sysinfo/master/screen.png)

<h2>License</h2>
GNU GPL v3.0 - https://www.gnu.org/licenses/gpl-3.0.en.html

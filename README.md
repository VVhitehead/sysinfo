<h2>System monitor extension for Argos with real CPU graph</h2>

This is a 4rk of an extension created specially for [Argos](https://github.com/p-e-w/argos) and linux-powered computers w/ GNOME shell.
It is based on **free**, **top**, **df** and **vmstat** output and uses power of SVG to draw charts.

This specific fork has visual and other tweaks most suitable 4 arch with dark gnome theme and will probably need to be retweaked for other combinations of distros and themes.

Please note that the CPU consumption is **very** approximate. Also, the real time between script execution isn't 1 sec because of latency of top and vmstat output.

Install dependencies: `sudo pacman -S top sysstat` or `sudo apt install top sysstat`
(depending on your os and package manager)

<h3>Known bugs</h3>

Different configurations of **top** utility doesn't allow to show processes and it's CPU consumtion (see opened issue here).
To fix this, open script in text editor and replace `$9 / 2` to `$7 / 2`. Also you may need to change `head -n 10` to `head -n 13`.
In case your **top** is not configured to sort processes by CPU usage, refer to the top(no phun intented) answer to [this](https://unix.stackexchange.com/questions/158584/change-tops-sorting-back-to-cpu) related question.

<h2>Screenshot</h2>

![](https://lut.im/Ehimc1iQn6/GAWEv4Euy3exhLiI)

<h2>License</h2>
GNU GPL v3.0 - https://www.gnu.org/licenses/gpl-3.0.en.html

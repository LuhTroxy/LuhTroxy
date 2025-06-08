<h3 align="center">A developer from India</h3>

<p align="left"> <img src="https://komarev.com/ghpvc/?username=luhtroxy&label=Profile%20views&color=0e75b6&style=flat" alt="luhtroxy" /> </p>

<p align="left"> <a href="https://www.w3schools.com/cpp/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cplusplus/cplusplus-original.svg" alt="cplusplus" width="40" height="40"/> </a> <a href="https://golang.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/go/go-original.svg" alt="go" width="40" height="40"/> </a> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> </p>

<p>&nbsp;<img align="center" src="https://github-readme-stats.vercel.app/api?username=luhtroxy&show_icons=true&locale=en" alt="luhtroxy" /></p>

<p><img align="center" src="https://github-readme-streak-stats.herokuapp.com/?user=luhtroxy&" alt="luhtroxy" /></p>


```import time
import secrets
from wcwidth import wcswidth

alias = "Troxy"
id = hex(secrets.randbits(64))

contact = {
    "Discord": "@luhtroxy",
    "Telegram": "@TroxyTele",
    "GitHub": "https://github.com/LuhTroxy"
}

def supported_langs():
    return {
        "good": ["Python"],
        "learning": ["Go", "C++", "Lua"]
    }

def obsessions():
    return [
        "dark mode",
        "music",
        "automation"
    ]

class Terminal:
    editor = "VS Code"
    theme = "Dark Modern"
    rituals = ["Ctrl+C", "Ctrl+V"]

def status():
    uptime = time.perf_counter()
    return f"🟢 Active for {uptime:.2f} sec(s)"

def troxy(lines, padding=1, border_char="═"):
    width = max(wcswidth(line) for line in lines) + padding * 2
    print(f"╔{border_char * width}╗")
    for line in lines:
        line_width = wcswidth(line)
        print(f"║{' ' * padding}{line}{' ' * (width - line_width - padding)}║")
    print(f"╚{border_char * width}╝")

if __name__ == "__main__":
    langs = supported_langs()

    output = [
        f"👤 Loading profile: {alias} [{id}]",
        "",
        "📬 Contact:",
        *[f"• {platform}: {handle}" for platform, handle in contact.items()],
        "",
        "🧠 Languages:",
        f"✅ Good at: {', '.join(langs['good'])}",
        f"🚧 Learning: {', '.join(langs['learning'])}",
        "",
        "🎯 Obsessions:",
        *[f"- {obs}" for obs in obsessions()],
        "",
        "💻 Terminal Setup:",
        f"Editor: {Terminal.editor}",
        f"Theme: {Terminal.theme}",
        f"Rituals: {', '.join(Terminal.rituals)}",
        "",
        f"📡 Status: {status()}"
    ]

    troxy(output)```

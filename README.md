![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Go](https://img.shields.io/badge/go-%2300ADD8.svg?style=for-the-badge&logo=go&logoColor=white) ![C++](https://img.shields.io/badge/c++-%2300599C.svg?style=for-the-badge&logo=c%2B%2B&logoColor=white) ![Lua](https://img.shields.io/badge/lua-%232C2D72.svg?style=for-the-badge&logo=lua&logoColor=white)

<br>

![](https://nirzak-streak-stats.vercel.app/?user=luhtroxy&theme=transparent&hide_border=false)



```
import time
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

    troxy(output)
```

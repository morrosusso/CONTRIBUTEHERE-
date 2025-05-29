
import time
import random
import os

messages = [
    "Why did you run this?",
    "Still going...",
    "This is your fault!",
    "You can't stop me!",
    "Are we having fun yet?"
]

apps = [
    "com.android.settings/.Settings",
    "com.android.calculator2/.Calculator",
    "com.google.android.youtube/.HomeActivity",
    "com.android.chrome/com.google.android.apps.chrome.Main"
]

try:
    while True:
        print(random.choice(messages))
        os.system("termux-media-player play /system/media/audio/ui/Lock.ogg")
        os.system(f"am start -n {random.choice(apps)}")
        time.sleep(2)
except KeyboardInterrupt:
    print("You stopped me!")
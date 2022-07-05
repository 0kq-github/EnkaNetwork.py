# Enka Network Python
[EN](./README.md) | TH

ไลบารีสำหรับดึงข้อมูล JSON จากเว็บ https://enka.shinshin.moe

# 💾 วิธีการติดตั้ง
```
pip install enkanetwork.py
```

# ✨ วิธีใช้
```py
import asyncio

from enkanetwork import EnkaNetworkAPI

client = EnkaNetworkAPI()

async def main():
    data = await client.fetch_user(843715177)
    print("=== Player Info ===")
    print(f"Nickname: {data.player.nickname}")
    print(f"Level: {data.player.level}")
    print(f"Icon: {data.player.profile_picture.icon}")
    print(f"Signature: {data.player.signature}")
    print(f"Achievement: {data.player.achievement}")
    print(f"Abyss floor: {data.player.abyss_floor} - {data.player.abyss_room}")
    print(f"Cache timeout: {data.ttl}")

loop = asyncio.get_event_loop()
loop.run_until_complete(main())
```

```sh
=== Player Info ===
Nickname: mrwan2546
Level: 55
Icon: https://enka.shinshin.moe/ui/UI_AvatarIcon_Hutao.png
Signature: ?
Achievement: 395
Abyss floor: 8 - 3
Cache timeout: 300
```

หากต้องการดูข้อมูล API เพิ่มเติม ไปดูที่ [EnkaNetwork API Docs](https://github.com/EnkaNetwork/API-docs)

## ตัวอย่างการใช้งาน
ดูได้ที่โฟเดอร์ [example](./example/)

# LICENSE
[MIT License](./LICENSE)

![น้อง Keqing น่ารัก 💗](https://c.tenor.com/MnkpnVCLcb0AAAAC/keqing-dance.gif)

[รูปจาก KKOMDASTRO](https://twitter.com/KKOMDASTRO)
import random
import datetime

print("🔮 歡迎來到 Python 算命師！🔮")

name = input("請輸入你的名字：")
birth = input("請輸入你的生日（YYYY-MM-DD）：")
color = input("請輸入你最喜歡的顏色：")

# 轉換生日為數字
try:
    birth_num = sum([int(x) for x in birth if x.isdigit()])
except:
    birth_num = random.randint(1,100)

# 用亂數 + 規則生成指數
luck = (birth_num + random.randint(1, 100)) % 100
love = (len(name) * random.randint(1, 10)) % 100
study = (random.randint(1, 10) * len(color)) % 100

# 結果輸出
print("\n✨ 今日運勢 ✨")
print(f"姓名：{name}")
print(f"幸運顏色：{color}")
print(f"整體運勢：{luck}/100")
print(f"愛情運勢：{love}/100")
print(f"學業指數：{study}/100")

# 加上幽默語句
comments = [
    "今天是個寫 bug 寫到懷疑人生的日子。",
    "或許該重啟一下電腦，連運氣都卡住了。",
    "天上掉下來的不一定是運氣，也可能是 exception。",
    "Debug 也是一種修行。"
]
print("\n建議：" + random.choice(comments))


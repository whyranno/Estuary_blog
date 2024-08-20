# contact

* hello world
* hello world
import requests

# API URL
url = "https://uniteapi.dev/api/pokemon-stats"

# API 요청
response = requests.get(url)
data = response.json()

# Markdown 테이블 생성
markdown_table = "| 포켓몬     | 픽률 (%) | 승률 (%) |\n"
markdown_table += "|------------|---------|---------|\n"

for pokemon in data:
    name = pokemon['name']
    pick_rate = pokemon['pick_rate']
    win_rate = pokemon['win_rate']
    markdown_table += f"| {name} | {pick_rate}    | {win_rate}    |\n"

print(markdown_table)
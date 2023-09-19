## 인스타 크롤링
- 셀레니움, time import 과정
```python
from selenium import webdriver
import time
```
- 인스타에서 페이스북 로그인
``` python
driver.find_elements('css selector',"#loginForm > div > div:nth-child(5) > button")[0].click()
```
- 로그인 창
```python
# 로그인
input_id = driver.find_elements("css selector","#email")[0] #id 창
input_pw = driver.find_elements("css selector","#pass")[0] #pw 창
input_id.clear()
input_id.send_keys('ID')
input_pw.clear()
input_pw.send_keys('PW')
#페이스북 내에서 로그인
driver.find_elements('css selector',"#loginbutton")[0].click() #확인 창
```
## *인스타에서 활성화 버튼 나중에 누르기
```python
# 나중에 하기 선택!!!!
driver.find_elements('css selector',"body > div.x1n2onr6.xzkaem6 > div.x9f619.x1n2onr6.x1ja2u2z > div > div.x1uvtmcs.x4k7w5x.x1h91t0o.x1beo9mf.xaigb6o.x12ejxvf.x3igimt.xarpa2k.xedcshv.x1lytzrv.x1t2pt76.x7ja8zs.x1n2onr6.x1qrby5j.x1jfb8zj > div > div > div > div > div.x7r02ix.xf1ldfh.x131esax.xdajt7p.xxfnqb6.xb88tzc.xw2csxc.x1odjw0f.x5fp0pe > div > div > div._a9-z > button._a9--._a9_1")\
[0].click() # <- css selector ..

```

## 토트넘 해시태그 검색
```python
word='토트넘'
driver.get(f'http://www.instagram.com/explore/tags/{word}')
```
## 첫 페이지 클릭 버튼 
```python
driver.find_elements('css selector','div._aagw')[0].click() # 첫페이지 클릭
# 첫 피드 클릭
```
## 다음 페이지 버튼 클릭
```python
next_button = driver.find_elements('css selector','body > div.x1n2onr6.xzkaem6 > div.x9f619.x1n2onr6.x1ja2u2z > div > div.x1uvtmcs.x4k7w5x.x1h91t0o.x1beo9mf.xaigb6o.x12ejxvf.x3igimt.xarpa2k.xedcshv.x1lytzrv.x1t2pt76.x7ja8zs.x1n2onr6.x1qrby5j.x1jfb8zj > div > div > div > div > div:nth-child(1) > div > div > div._aaqg._aaqh > button')
next_button[0].click()
```





# 각각 본문, 좋아요, 태그, 작성일을 엑셀로 보내기

```python
data=[]
driver.find_elements('css selector','div._aagw')[0].click() # 첫페이지 클릭
while True:

    next_button = driver.find_elements('css selector','body > div.x1n2onr6.xzkaem6 > div.x9f619.x1n2onr6.x1ja2u2z > div > div.x1uvtmcs.x4k7w5x.x1h91t0o.x1beo9mf.xaigb6o.x12ejxvf.x3igimt.xarpa2k.xedcshv.x1lytzrv.x1t2pt76.x7ja8zs.x1n2onr6.x1qrby5j.x1jfb8zj > div > div > div > div > div:nth-child(1) > div > div > div._aaqg._aaqh > button')
    html = driver.page_source # 현재 페이지 값 가져오기 
    soup = BeautifulSoup(html,'html.parser')
    try:
        gap = soup.select('h1._aacl._aaco._aacu._aacx._aad7._aade')  #본문
        like = soup.select('a>span')
        time = soup.select('time')[0]
        gaps= gap[0].text # 본문 출력
        likes = re.findall('\d.+',like[-2].text)[0]# 좋아요 출력
        times= time.text # 시간출력
        tags = re.findall("#\w+", gap[0].text) # 태그 출력
        data.append([gaps,likes,tags,times])
        next_button[0].click()
    except:
        break
df= pd.DataFrame(data, columns=['내용','좋아요','태그','작성일'])
df.to_excel('Son.xlsx',index=False)


```

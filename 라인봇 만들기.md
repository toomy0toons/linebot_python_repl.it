# 라인봇 만들기

## 1.1 라인 개발자 계정 생성

[https://developers.line.biz](https://developers.line.biz/)

에서 개발자 계정 생성후 

`create new provider` 버튼 클릭해서 Provider 생성

## 1.2 채널 생성

`create new chanel` 으로 채널 생성후 

봇 을 만들거기 때문에 `messaging API ` 를 선택해준다

다음과 같은 화면이 나온다

![](%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%E1%84%87%E1%85%A9%E1%86%BA%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%80%E1%85%B5/76953006-FBCE-48B8-B931-5C050FEA2440.png)


## 1.3 봇 친구 추가

만들어진 봇을 클릭하면 세팅 페이지가 나온다 

밑으로 내리면 qr 코드가 있는데 핸드폰 라인앱을 켜서 친구추가를 해준다

![](%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%E1%84%87%E1%85%A9%E1%86%BA%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%80%E1%85%B5/5A0A10D6-8332-4B91-8A8D-984B34FEA165.png)


## 1.4 자동응답, 환영메세지 끄기

옆에 set message 눌러서
![](%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%E1%84%87%E1%85%A9%E1%86%BA%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%80%E1%85%B5/ED795521-CD36-4AA6-9B7B-ECBE1232F994.png)
다음과 같이 설정해준다

## 1.5 토큰 발급 
issue 버튼을 눌러
![](%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%E1%84%87%E1%85%A9%E1%86%BA%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%80%E1%85%B5/4C6AD889-3781-43B2-AD1D-A891C0CDC0B3.png)

![](%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%E1%84%87%E1%85%A9%E1%86%BA%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%80%E1%85%B5/06183A8B-1471-49D9-9542-D728D6F24711.png)

`channel secret`,` channel access token` 값을 잘 복사해서 따로 저장해둔다.

이값들은 봇의 아이디, 패스워드와 같은 인증수단으로 사용하기 때문에 공개되면 안된다. 

### 2.1 Repl.it 저장소 세팅 
https://repl.it/@toomy0toons/LineBot 접속한다

상단에 fork 버튼을 눌러 내 계정으로 복사한다.
![](%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%E1%84%87%E1%85%A9%E1%86%BA%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%80%E1%85%B5/17F80AA0-82C6-4FC1-AC3A-4999D7027A28.png)
 
### 2.2 env 파일 변경

좌측 env 파일옆에 아이콘을 누르면 rename 이 있다.
![](%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%E1%84%87%E1%85%A9%E1%86%BA%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%80%E1%85%B5/47F8F386-A314-484D-B928-1B39100C86B1.png)
클릭해서 파일 이름을 .env (앞에 . 있음) 으로 바꾼다.

![](%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%E1%84%87%E1%85%A9%E1%86%BA%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%80%E1%85%B5/3BFD295D-7E61-4CEE-8E49-7F4F2F5BCDFF.png)

### 2.3 .env 환경변수 입력
env 파일을 열어 LINE_CHANNEL_SECRET 과 LINE_CHANNEL_ACESS_TOKEN 에 해당하는 값을 넣어준다
![](%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%E1%84%87%E1%85%A9%E1%86%BA%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%80%E1%85%B5/BAE534FD-DB4D-4729-9F2C-03EA2B6C89E3.png)

### 3.1 repl.it 코드 실행

run 버튼을 눌러서 실행을 하면 
하얀 웹창이 나온다 

![](%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%E1%84%87%E1%85%A9%E1%86%BA%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%80%E1%85%B5/891218FE-788C-4637-A543-CFB7ACACBBD5.png)

이 주소창안의 주소를 잘 기억하자 이게 내 서버 주소이다. 
https://LineBot.toomy0toons.repl.co

### 3.2 callback 주소 세팅
네이버 라인 창으로 돌아가서 
![](%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%E1%84%87%E1%85%A9%E1%86%BA%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%80%E1%85%B5/E342DABA-F40D-49B6-A89F-A72512838099.png)
use webhook -> enabled 로 변환 하고
아래 webhook_URL 을
본인 주소 + /callback 입력한다
**verify 누르면 안되는게 정상이래.. 그니깐 누르지말자 애들아 누르면 서버터져** 

### 3.3 라인앱을 켜서 확인 

라인 앱을 켜서 확인해보자.
내가 채팅을 보내면 봇이 그 채팅을 그대로 돌려줄것이다. 

![](%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%E1%84%87%E1%85%A9%E1%86%BA%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%80%E1%85%B5/18D5F7E4-B72C-40F0-949C-F499DB89DD54.png)

### 4.1 profile 기능 활용하기

코드를 봐보자
``` python
@handler.add(MessageEvent, message=TextMessage)
def handle_text_message(event):
  text = event.message.text
```
handler 라는 기능을 활용하는데, 
MessageEvent 중에서도 TextMessage 즉 문자메세지가왔을 때 아래의 함수를 실행시켜주는 기능이다. (자동반복된다) 
두번째 줄을 보면 `text = event.message.text` 으로 사용자가 입력한 메세지의 내용을 저장한다. 

그 다음 `if text == 'profile':` profile 이라는 말이 입력 되었으면 밑의 기능을 실행하고, 
![](%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%E1%84%87%E1%85%A9%E1%86%BA%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%80%E1%85%B5/176342E1-C221-4057-9505-CAAB28A8E201.png)

예약된 명령어가 아닐경우에, 다시 되돌려준다. 
``` python
  else:
    line_bot_api.reply_message(
      event.reply_token,
      TextSendMessage(text=event.message.text))
```

앞으로 코딩할때는 
elif text = ‘명령어’:  식으로 계속해서 추가해주면된다. 

### 4.2 quick reply 기능 활용하기 

봇을 만들 때 입력하기가 귀찮을 수 있다. 

이때 quickreply 를 활용할 수 있다.

다음 코드를 잘 붙여넣기 해보자

``` html
  elif text == '메뉴':
        line_bot_api.reply_message(
            event.reply_token,
            TextSendMessage(
                text='중식 or 석식?',
                quick_reply=QuickReply(
                    items=[
                        QuickReplyButton(
                            action=MessageAction(label="중식", text="중식")
                        ),
                        QuickReplyButton(
                            action=MessageAction(label="석식", text="석식")
                        ),
                    ])))
```
위치는 맨밑에 else 와 줄을 맞춰서 넣어 주면 된다. 
![](%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%E1%84%87%E1%85%A9%E1%86%BA%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%80%E1%85%B5/0517CBA4-FD2A-4309-A0AB-8160745246AE.png)

여기서 label 은 표시되는 메뉴의 이름, text 는 사용자 대신해서 입력되는 말이다. 

![](%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%E1%84%87%E1%85%A9%E1%86%BA%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%80%E1%85%B5/B4E7953E-B005-4CB1-B26A-909F1258D5E3.png)

### 이외에도 많은 기능잉있어서ㅓ
[line-bot-sdk-python/app.py at master · line/line-bot-sdk-python · GitHub](https://github.com/line/line-bot-sdk-python/blob/master/examples/flask-kitchensink/app.py)
여기 참고

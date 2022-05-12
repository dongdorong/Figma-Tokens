# Figma-Tokens

### 링크

[Figma Tokens: Plugin Docs](https://docs.tokens.studio/)

[Material Design](https://material.io/design/color/the-color-system.html#color-theme-creation)

[A Visual Type Scale](https://type-scale.com/)

[Build software better, together](https://github.com/settings/tokens/new)

[[A1] Do more, with less. - 디자인 시스템, 그다음은?](https://youtu.be/LmLchZ4tCXc)

## Design Tokens Research 이유

- 디자인 토큰 리서치의 목표는 효율적인 디자인 시스템 관리를 하기 위함
- 일관된 디자인 토큰 - 시스템으로 작업 시간 & 운영 공수 줄이기

## Design Token 개요

- 디자인 토큰은 디자인 시스템 작업 시 디자인 속성을 다양한 방법으로 저장하는 방법입니다.
- 디자인 토큰은 디자인 시스템의 시각적 원자, 특히 시각적 디자인 속성을 저장하는 실체로 정의합니다. 확장 가능하고 일관된 시각적 시스템을 유지하기 위해 하드 코딩된 값 대신 이 값을 사용합니다.

## Design Token 적용 방법

### 1. Figma Plugin

- Figma Tokens를 설치 합니다.
    
    ![스크린샷 2022-04-28 오후 10.15.45.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c2e386d4-7604-4313-80ea-ab3cf93789ba/스크린샷_2022-04-28_오후_10.15.45.png)
    
    ![스크린샷 2022-04-20 오후 11.36.29.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8167256f-ea56-4291-a06e-8ba611566544/스크린샷_2022-04-20_오후_11.36.29.png)
    

### 2. 각 속성별 Token을 만듭니다.

- Global 속성의 Token을 만든다.
- 각 Theme에 대한 Token은 새로운 Set을 만들어 진행한다.

![스크린샷 2022-04-28 오후 2.40.23.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/19e32fa3-f85c-4788-bd05-28931d7ffb94/스크린샷_2022-04-28_오후_2.40.23.png)

![스크린샷 2022-04-28 오후 2.49.50.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1a180d7e-7883-420a-bbc8-f909b87bab8e/스크린샷_2022-04-28_오후_2.49.50.png)

[Available Tokens](https://www.notion.so/662e123244874ecfa130361580ab8e9d)

- 새로운 Theme의 Set을 만들면 사용하는 Token의 정확한 목적을 이름으로 정해야한다. [Adobe Spectrum link](https://spectrum.adobe.com/page/design-tokens/)
    - ex) button-cta-background-color
    - ex) button-cta-background-color-hover
    - ex) button-cta-background-color-focus
        
        ![design_tokens@2x_1649708322885.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/19e21c3f-e5d9-4efa-865c-37a707237e46/design_tokens2x_1649708322885.png)
        
    

### 3. Theme Set을 만듭니다.

- Theme에 맞는 스타일을 Global에 있는 속성을 가져와서 만들 수 있습니다.

![스크린샷 2022-04-28 오후 10.16.53.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c1a9fa43-bfb9-4935-8b65-e6c16ce07240/스크린샷_2022-04-28_오후_10.16.53.png)

### 4. 만들어진 디자인 토큰으로 디자인 시스템을 작업합니다.

## Figma File

[https://www.figma.com/file/NYXodUamR9NbXyXQ5bSt1z/Design-Tokens?node-id=0%3A1](https://www.figma.com/file/NYXodUamR9NbXyXQ5bSt1z/Design-Tokens?node-id=0%3A1)

## PD <> FE 협업 포인트

- 디자인 토큰은 개발까지 이어졌을 때 의미가 큼
- 전달/적용 방법을 사전에 PD<>FE 사이에 정의를 잘 해야함
- Github으로 저장한 tokens.json
    
    [Figma-Tokens/tokens.json at main · dongdorong/Figma-Tokens](https://github.com/dongdorong/Figma-Tokens/blob/main/tokens.json)
    
- Github에 저장된 토큰을 개발 중에 사용하는 방법
    
    [Figma Tokens: Plugin Docs](https://docs.tokens.studio/sync/github)
    

## 주의 사항

- CSS 코드와 같아서 변수명이 다르면 디자인 토큰이 적용이 안되니 이름을 틀리지 않게 주의해야함

![스크린샷 2022-04-28 오후 9.31.11.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6db49151-cd9a-4b19-a748-f80491d8eaf1/스크린샷_2022-04-28_오후_9.31.11.png)

```json
"typography": {
    "H1": {
      "Bold": {
        "value": {
          "fontFamily": "$fontFamilies.body",
          "fontWeight": "Bold",
          "lineHeight": "AUTO",
          "fontSize": "$fontSizes.h1",
          "letterSpacing": "0%",
          "paragraphSpacing": "0",
          "textDecoration": "none",
          "textCase": "none"
        },
        "type": "typography",
        "description": "h1"
      }
	}
}
```
TERMINOLOGY EXPLANATION

0. Frontend dev 
  > UX (User Experience) & UI (User Interface) 
  > basically the front page you see when you open a webpage
  > in this course, we learn HTML / CSS / Javascript

1. HTML / CSS / JapaScropt 
- HTML (HyperText Markup language)
  > defines the structure of a webpage (like a doc)

- CSS (Cascading Style Sheet)
  > designs a webpage built upon HTML

- Japascript
  > coding language for interactively & dynamically updating webpage
  > built upon HTML (structure) & CSS (design)

2. URL vs. URI
<img width="595" height="250" alt="image" src="https://github.com/user-attachments/assets/4c440d95-f025-42c5-ad1e-a589e4d9bbf9" />

- URI (Uniform Resource Identifier)
  ; a string of characters that identify a resource
  > parental category
  > purpose: IDENTFIY resource (can do by location or name, or both)
  ie. https://example.com
  
- URL (Uniform Resource Locator)
  ; a SUBSET of URI that provides location of a resource
  > more SPECIFIC
  > requires protocol to identify WHERE the resource is
  ie. https://example.com, mailto:user@example.com
_______________________________________________________________
1. <div> </div> element
* default block element (takes ALL available width, comes with line breaks before and after)
* often used to group sections of web page tgt (container!)
ie)
<div>
  <h2>London</h2>
  <p>London is the capital city of England.</p>
  <p>London has over 9 million inhabitants.</p>
</div>
_______________________________________________________________
1. FLEX vs. GRID
- both ways of organizing UI data

> FLEX
* 말 그대로 '유연' 한 정렬 방식
* 'display: flex" or "display: inline-flex' --> 지정한 컨테이너의 아이템을 유연하게 배치하는 방법
  -ve: 수평/수직/중앙 정렬 어려움
  -ve: 요소 간 간격 일정 배치 어려움
  -ve: 아이템 넘칠 때 줄바꿈 어려움
  -ve: 레이아웃 방법 어려움

> GRID
* 'display: grid" 또는 'display" inline-grid'를 넣은 부모요소의 container안에서 GRID 규칙이 적용된다.

2. FLEX 종류 (CCS)
> FLEX: flex-grow (말 그대로, 유연하게 늘린다)
* flex-grow: 1;
* flex-grow: 0; (default value

> FLEX: align-items (수직축 방향 정렬) / (한 줄을 기준으로 정렬)
<img width="560" height="703" alt="image" src="https://github.com/user-attachments/assets/ffc410d7-f6ca-4ab1-97ae-0c1362b26c48" />

* align-items: stretch;
* align-items: flex-start;
* align-items: flex-end;
* align-items: center;
* align-tems: baseline;

> FLEX: align-content (여러 행 정렬). > flex-wrap: wrap; 설정 후 사용!!!!!
(수직축을 기준으로 라인 자체가 정렬이 됨 / 두줄 이상일때만!!!)
<img width="663" height="719" alt="image" src="https://github.com/user-attachments/assets/293f60cd-1089-432e-9177-edd0aabd5235" />

* align-content: stretch;
* align-content: flex-start;
* align-content: flex-end;
* align-content: center;
* align-content: space-between;
* align-content: space-around;
* aling-content: space-evenly;

> FLEX: justify-content (메인축 방향 정렬 / flex container의 메인축을 따라 정렬하는 프로퍼티 / 배치방향대로 접었을 때로 생각)
along PRIMARY axis (row is default)
<img width="723" height="715" alt="image" src="https://github.com/user-attachments/assets/3450c53c-8137-44f6-9ef5-bc2c1edf5828" />

* justify-content: flex-start;
* justify-content: flex-end;
* justify-content: center;
* justify-content: space-between;
* justify-content: space-around;
* justify-content: space-evenly;
  
  예시 1)
  <img width="1919" height="180" alt="image" src="https://github.com/user-attachments/assets/4a71a011-36b0-48d2-aeaa-335cc02cdace" />

  <style>
    * {box-sizing: border-box;}
    html, body {margin: 0; padding: 0;} 
    /* display: flex */
    ul {display: flex;
      margin: 0; padding-left: 0; list-style-type: none; border: 1px solid #000;}
    li {flex-grow: 1; text-align: center; font-weight: bold; border: 1px solid #000;}
  </style>
</head>
<body>
  <ul>
		<li>A</li>
		<li>B</li>
		<li>C</li>
		<li>D</li>
		<li>E</li>
		<li>F</li>
	</ul>
</body>

--> 설명)
* ul = unordered list
* ol = ordered list

  예시 2) 
  <style>
    * {box-sizing: border-box;}
    html, body{margin:0; padding:0;}
    .body {display: flex; width: 100%; height: calc(100vh/6)} 
    -->  (여기서 width and height 픽셀 값으로 인풋 가능하나, 자동으로 계산하는 값으로 인풋함)
    .body div {flex-grow: 1;}
    .bg1 {background-color:aqua;}
    .bg2 {background-color:brown;}
   </style>
</head>
<body>
    <div class="body">
        <div class="bg1"></div>
        <div class="bg2"></div>
        <div class="bg1"></div>
    </div>
    <div class="body">
        <div class="bg2"></div>
        <div class="bg1"></div>
        <div class="bg2"></div>
    </div>
    <div class="body">
        <div class="bg1"></div>
        <div class="bg2"></div>
        <div class="bg1"></div>
    </div>
</body>
</html>

예시 3)
  <style>
    * {box-sizing: border-box;}
    html, body {margin: 0; padding: 0;}
    /* display: flex */
    ul { display: flex; gap: 10px; flex-direction: column;
    ul { display: flex; gap: 10px; flex-direction: column; 
      margin: 0; padding-left: 0; list-style-type: none; 
    }
    li { height: 50px; display: flex; align-items: center; justify-content: center;
  </style>
        
예시 4: style 만들고, body 에 div 제작하여 ) 
 <style>
    * {box-sizing: border-box;}
    html, body {margin: 0; padding: 0;}
    .body {display: flex; width: 100%; height: calc(100vh / 6);}
    .body div {flex-grow: 1;}
    .bg1 {background-color: aqua;}
    .bg2 {background-color: brown;}
  </style>
</head>
<body>
  <div class="body">
    <div class="bg1"></div>
    <div class="bg2"></div>
    <div class="bg1"></div>
    <div class="bg2"></div>
    <div class="bg1"></div>
    <div class="bg2"></div>
  </div>
  <div class="body">
    <div class="bg2"></div>
    <div class="bg1"></div>
    <div class="bg2"></div>
    <div class="bg1"></div>
    <div class="bg2"></div>
    <div class="bg1"></div>
  </div>
  <div class="body">
    <div class="bg1"></div>
    <div class="bg2"></div>
    <div class="bg1"></div>
    <div class="bg2"></div>
    <div class="bg1"></div>
    <div class="bg2"></div>
  </div>
  <div class="body">
    <div class="bg2"></div>
    <div class="bg1"></div>
    <div class="bg2"></div>
    <div class="bg1"></div>
    <div class="bg2"></div>
    <div class="bg1"></div>
  </div>
  <div class="body">
    <div class="bg1"></div>
    <div class="bg2"></div>
    <div class="bg1"></div>
    <div class="bg2"></div>
    <div class="bg1"></div>
    <div class="bg2"></div>
  </div>
  <div class="body">
    <div class="bg2"></div>
    <div class="bg1"></div>
    <div class="bg2"></div>
    <div class="bg1"></div>
    <div class="bg2"></div>
    <div class="bg1"></div>
  </div>
</body>




  

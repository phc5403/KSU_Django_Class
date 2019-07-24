Django - Model & Admin / QuerySet & Method / Detail.html / STATIC & MEDIA 
: 19. 5.21 ~ 19. 6. 4의 수업내용  
==========
  
**< 5.29(Wed) - Update Release >**  
● home.html : line 30 → 글쓰기를 URL 직접 조작 필요없이 NavBar의 메뉴로 동작할수있게끔 a태그 추가.  
● detail.html : line 27 → 글쓰기를 URL 직접 조작 필요없이 NavBar의 메뉴로 동작할수있게끔 a태그 추가.  
    
    <a class="nav-item nav-link" href="{% url 'new' %}">글쓰기</a>
***    
**< 5.31(Fri) - Update Release >**  
● portfolio APP 추가
    
    python manage.py startapp portfolio        
● portfolio.html : STATIC & MEDIA 활용을 위해 새롭게 생성 및 추가.
    
    python manage.py makemigrations
    python manage.py migrate
    python manage.py collectstatic
    pip install Pillow    
● 그외 settings.py / models.py / views.py / urls.py / portfolio.html-Bootstrap 수정      

**< 6. 5(Wed) - Update Release >**  
● Template 상속 및 URL 관리.

● base.html에 포트폴리오 메뉴로 이동 가능하게 추가함.
    
    <a class="nav-item nav-link" href="{% url 'portfolio' %}">포트폴리오</a>

● 주의사항 : base.html을 extends하기 위해 portfolio.html의 내용을 지울때 만약 동작이 안될경우, 
            head 태그와 body의 끝부분에있는 <script>들을 살려서 해볼것.

<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>청년창업 통합 홈페이지</title>

  <style>
    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: Arial, sans-serif;
      margin: 0;
      background-color: ivory;
    }

    header {
      background-color:ivory;
      color: black;
      padding: 20px;
      text-align: left;
      font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
      font-size: 36px;
      cursor: pointer;
    }

    nav.top {
      text-align: left;
      background-color: #444;
      padding: 20px 30px;
    }

    nav.top a {
      color: white;
      text-decoration: none;
      margin-right: 20px;
      font-weight: bold;
      cursor: pointer;
    }

    .container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 20px;
      padding: 40px;
      max-width: 1000px;
      margin: auto;
    }

    .card {
      background: #fff;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      padding: 20px;
      transition: transform 0.2s ease;
      cursor: pointer;
    }

    .card:hover {
      transform: translateY(-5px);
    }

    .section {
      display: none;
    }

    .section.active {
      display: block;
    }

    .startup-layout {
      display: flex;
      min-height: 70vh;
    }

    nav.side {
      width: 200px;
      background-color: #34495e;
      padding-top: 20px;
      display: flex;
      flex-direction: column;
    }

    nav.side a {
      color: white;
      padding: 15px 20px;
      text-decoration: none;
      font-weight: bold;
      border-bottom: 1px solid #2c3e50;
      cursor: pointer;
    }

    nav.side a:hover {
      background-color: #2c3e50;
    }

    .startup-content {
      flex: 1;
      padding: 40px;
    }

    .sub-section {
      display: none;
    }

    .sub-section.active {
      display: block;
    }

    .card-box {
      background: #fff;
      border-radius: 12px;
      padding: 20px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }

    .image-box {
      text-align: center;
      margin: 40px auto;
    }

    .image-box img {
      width: 90%;
      max-width: 1000px;
      border-radius: 12px;
    }
  </style>

  <script src="https://code.jquery.com/jquery-3.7.1.min.js"></script>
  <script>
    $(document).ready(function () {
      // 메인 섹션 전환
      $('.section').first().addClass('active');
      $('nav.top a').click(function (e) {
        e.preventDefault();
        var target = $(this).data('target');
        $('.section').removeClass('active');
        $('#' + target).addClass('active');
      });

      // 카드 클릭 시 청년창업 섹션으로 이동
      $('#card1, #card2').click(function () {
        $('.section').removeClass('active');
        $('#startup').addClass('active');
        $('.sub-section').removeClass('active');
        $('#gov').addClass('active'); // 기본 표시
      });

      // 청년창업 내부 메뉴 전환
      $('nav.side a').click(function () {
        var target = $(this).data('target');
        $('.sub-section').removeClass('active');
        $('#' + target).addClass('active');
      });

      // 헤더 클릭 시 홈으로 이동
      $('header').click(function () {
        $('.section').removeClass('active');
        $('#home').addClass('active');
      });
    });
  </script>
</head>

<body>
  <header>
    웹 프로그래밍 기말 프로젝트
  </header>

  <nav class="top">
    <a data-target="home">홈</a>
    <a data-target="about">소개</a>
  </nav>

  <div id="home" class="section active">
    <div class="container">
      <div id="card1" class="card">
        <h2>청년 창업 바로가기</h2>
        <p>클릭하면 청년 창업 정보를 확인할 수 있습니다.</p>
      </div>
      <div id="card2" class="card">
        <h2>Sub2</h2>
        <p>클릭하세요.</p>
      </div>
    </div>
    <div class="image-box">
      <img src="back.jpg" alt="홈 배경 이미지">
    </div>
  </div>

  <div id="about" class="section">
    <div class="container">
      <div class="card">
        <h2>소개</h2>
        <p>홈페이지 제작자 소개란</p>
      </div>
    </div>
    <div class="image-box">
      <img src="back.jpg" alt="소개 배경 이미지">
    </div>
  </div>

  <div id="startup" class="section">
    <div class="startup-layout">
      <nav class="side">
        <a data-target="gov">정부 지원</a>
        <a data-target="academy">청년 창업 사관학교</a>
        <a data-target="helper">청년 창업 지원 도우미</a>
      </nav>
      <div class="startup-content">

        <!-- 정부 지원 섹션 - 스크롤 이동 포함 -->
        <div id="gov" class="sub-section active">
          <div class="card-box">
            
            <h2>정부 지원</h2>
            <h3>창업에 관심 있는 분이라면 한 번쯤 '나도 창업 지원금을 받을 수 있나?' 하는 생각을 해보셨을 것 같습니다.</h3>
            <h3>'창업지원금'을 검색하거나 창업 포털 사이트를 찾아보면 수많은 공고를 보실 수 있는데요. 정보가 너무 많기 때문에 오히려 무엇부터 봐야 할지 막막할 수 있습니다.</h3>
            <h3>수많은 창업 지원 사업 중 정부에서 공식적으로 운영하고, 매년 정기적으로 모집하며, 규모가 비교적 큰 대표적인 지원 사업을 정리해 보았습니다.</h3>
            <hr>

            <h1>이것부터 확인하세요!</h1>
            <div>
                <ul>
                    <li>정부 지원 사업은 대부분 연초(1~2월)에 모집을 시작합니다. 지금부터 나에게 해당하는 사업과 관련 준비 사항을 미리 알아보고, 공고가 뜨면 바로 신청할 수 있도록 준비해 두는 것이 좋습니다.</li>
                    <li>공식 웹사이트를 통해 기존에 선정된 사업 리스트를 살펴볼 수 있습니다. 어떤 사업이 선정되었는지 살펴보고 나에게 적용할 만한 힌트를 얻어보세요.</li>
                    <li>지원 대상, 내용, 시기는 변경될 수 있습니다. 아래 정보는 2024년 모집 공고를 기준으로 작성되었으며, 반드시 모집 시기에 해당 사업 공고의 자세한 내용을 확인하세요. *2025년 2월 20일  업데이트</li>
                </ul>
            </div>
            <hr>
            <div style="margin-bottom: 20px;">
            <ul>
              <li><a href="#pre" style="margin-right: 15px; font-weight: bold; color: #2c3e50; cursor: pointer;">예비 창업자</a></li>
              <li><a href="#early" style="margin-right: 15px; font-weight: bold; color: #2c3e50; cursor: pointer;">초기 창업자(3년이내)</a></li>
              <li><a href="#growth" style="font-weight: bold; color: #2c3e50; cursor: pointer;">중기 창업자(3년~7년)</a></li>
            </ul>
            </div>

            <div id="pre" style="margin-top: 40px;">
              <h2>1. 예비 창업자</h2>
            </div>
            <div>
                <h3>예비창업패키지</h3>
                <ul>
                    <li>혁신적인 기술과 사업 모델(BM)을 보유한 예비창업자의 성공 창업을 지원하여 양질의 일자리를 창출합니다.</li>
                    <li>지원 대상: 공고일 기준 사업자 등록 및 법인 설립등기를 하지 않은 예비 창업자</li>
                    <li>지원 내용: 사업화 자금 (평균 0.5억 원), 창업프로그램 등</li>
                    <li>선정 규모: 일반분야 660명, 특화분야 120명 내외(여성 60명/소셜 벤처 60명/사내 벤처 30팀)</li>
                    <li>모집 일정: 사업 공고(2월) > 서류 평가(3월) > 인큐베이팅(4월) > 발표 평가(4월) > 선정 및 사업화 지원(4월~)</li>
                    <li>운영 기관: 창업진흥원 예비초기팀</li> 
                </ul>
            </div>
            <div>
                <h3>신사업 창업사관학교</h3>
                <ul>
                    <li>성장 가능성이 높은 유망 아이템으로 창업을 준비하는 예비 소상공인을 선발하여 기초 및 경영 교육, 상품화 지원, 사업화 자금 등을 지원합니다.</li>
                    <li>지원 대상: 신사업 아이디어 또는 유망 아이템으로 창업하고자 하는 예비 창업자<br>
신청 분야: 로컬크리에이터형 / 라이프스타일형</li>
                    <li>지원 내용: 사업화 자금(최대 4천만 원)</li>    
                    <li>선정 규모: 총 510명 이내 (지역별 모집 규모 상이)</li>
                    <li>모집 일정: 사업 공고(3월) > 서류, 발표 평가(4월) > 선정(4월) > 사업화 지원(4월~)</li>
                    <li>운영 기관: 소상공인시장진흥공단 창업지원실</li>
                </ul>
            </div>
            <div>
                <h3>창업중심대학 - 예비 창업자</h3>
                <ul>
                    <li>기준 지역별 또는 대학별 예비창업자의 우수한 기술창업 아이템, 비즈니스 모델의 사업화를 지원합니다.</li>
                    <li>지원 대상: 제시된 지역 또는 창업중심대학 기준을 충족하는 예비 창업자<br>
대학발 창업 / 지역 일반 유형으로 구분</li>
                    <li>지원 내용: 사업화자금(5천만 원 내외, 최대 1억 원), 창업 프로그램 등</li>    
                    <li>지원 규모: 총 351명 내외</li>
                    <li>모집 일정: 사업 공고(1월) > 신청·접수(1월) > 평가·발표(2월) > 사업화 지원(3월~)</li>
                    <li>운영 기관: 중소벤처기업부 창업진흥원</li>        
                </ul>
            </div>

            <div id="early" style="margin-top: 40px;">
              <h2>2.초기 창업자(3년이내)</h2>
            </div>
            <br>
            <div>
                <h3>초기창업패키지</h3>
                <ul>
                    <li>유망 창업 아이템 및 고급 기술을 보유한 초창기 기업에 필요한 사업화 자금을 지원합니다. (최대 1억 원)</li>
                    <li>지원 대상: 업력 3년 이내 초기 창업 기업</li>
                    <li>지원 내용: 사업화 자금 (최대 1억 원), 창업 프로그램 등</li>
                    <li>선정 규모: 총 430개사 내외</li>
                    <li>모집 일정: 사업 공고(2월) > 신청·접수(2월) > 서류평가 (3월) > 심층 인터뷰 (4월) > 발표평가 (4월) > 최종 선정 및 사업비  지원 (4월~)</li>
                </ul>
            </div>
            <div>
                <h3>창업성공패키지 청년창업사관학교 (입교생 모집)</h3>
                <ul>
                    <li>유망 창업 아이템 및 혁신 기술을 보유한 우수 창업자를 발굴하여 창업의 전 단계를 지원합니다.</li>
                    <li>지원 대상: 만 39세 이하, 창업 후 3년 이내 창업 기업의 대표자</li>
                    <li>지원 내용: 사업비 지원(최대 1억 원, 총사업비의 70% 이내), 창업 준비 공간 지원, 창업 교육 및 코칭, 기술 지원 등</li>
                    <li>선정 규모: 총 850명 (글로벌형 330명, 지역특화형 310명, 투자형 140명)</li>
                    <li>모집 일정: 사업 공고(1월) > 신청·접수(1~2월) > 평가·발표(2~3월) > 프로그램 진행(3월~)</li>
                    <li>운영 기관: 중소벤처기업부 중소벤처기업진흥공단 창업지원처 </li>
                </ul>
            </div>
            <div>
                <h3>창업중심대학 - 초기 창업기업</h3>
                <ul>
                    <li>기준 지역별 또는 대학별 초기 창업기업의 우수한 기술창업 아이템, 비즈니스 모델의 사업화를 지원합니다.</li>
                    <li>지원 대상: 제시된 지역 또는 창업중심대학 기준을 충족하는 3년 이내 창업자 (공고 상세 내용 확인)</li>
                    <li>지원 내용: 정부지원사업비(7천만 원 내외, 최대 1억 원), 창업 프로그램 등</li>
                    <li>선정 규모: 총 180개 내외 (대학발 창업 54개, 지역 일반 유형 126개)</li>
                    <li>모집 일정: 사업 공고(1월) > 신청·접수(1월) > 평가·발표(2월) > 사업비 지원(3월~)</li>
                    <li>운영 기관: 중소벤처기업부 창업진흥원</li>
                </ul>
            </div>
            

            <div id="growth" style="margin-top: 40px;">
              <h2>3.중기 창업자(3년~7년)</h2>
            </div>
            <div>
                <h3>창업도약패키지</h3>
                <ul>
                    <li>유망 기술창업 아이템을 보유한 도약기 창업 기업의 비즈니스 모델 혁신 및 제품‧서비스 고도화를 지원합니다.</li>
                    <li>2024년도 창업도약패키지 창업기업 모집은 ①대기업 협업형, ②일반형, ③투자병행, ④융자병행, 4가지 유형으로 분리하여 공고하며, 이 중 1개의 유형만 신청 가능합니다.</li>
                    <li>지원 대상: 창업 후 3년 초과 7년 이내 도약기 창업기업</li>
                    <li>지원 내용 및 선정 규모<br>
                        ①대기업 협업형: 사업화 자금(최대 2억 원), 창업 프로그램 / 100개사 내외<br>
                        ②일반형: 사업화 자금(최대 3억 원), 창업 프로그램 / 233개사 내외<br>
                        ③투자병행: 사업화 자금(최대 2억 원+투자 연계), 창업 프로그램 / 20개사 내외<br>
                        ④융자병행: 사업화 자금(최대 2억 원+융자 연계), 창업 프로그램 / 20개사 내외
                    </li>
                    <li>운영 기관: 중소벤처기업부 창업진흥원</li>
                </ul>
            </div>
            <div>
                <h3>창업중심대학 - 도약기 창업기업</h3>
                <ul>
                    <li>기준 지역별 또는 대학별 초기 창업기업의 우수한 기술창업 아이템, 비즈니스 모델의 사업화를 지원합니다.</li>
                    <li>지원 대상: 제시된 지역 또는 창업중심대학 기준을 충족하는 3년 초과 7년 이내 창업자</li>
                    <li>지원 내용: 정부지원사업비(최대 3억 원), 창업 프로그램 등</li>
                    <li>선정 규모: 총 102개 내외 (대학발 창업 유형 27개, 지역 일반 유형 75개)</li>
                    <li>모집 일정: 사업 공고(1월) > 신청·접수(1월) > 평가·발표(2월) > 사업비 지원(3월~)</li>
                    <li>운영 기관: 중소벤처기업부 창업진흥원</li>
                </ul>
            </div>
            <div>
                <h3>창업성공패키지 - 글로벌창업사관학교(입교생 모집)</h3>
                <ul>
                    <li>혁신 기술 및 글로벌 창업 아이템을 보유한 창업자의 성공적인 글로벌 사업화를 지원합니다.</li>
                    <li>지원 대상: 창업 7년 이내 기업 중 ① 글로벌 확장성이 높은 초격차･신산업･기후기술 분야 스타트업 또는 ➁ 글로벌 진출을 희망하는 청년창업사관학교 또는 글로벌창업사관학교 졸업기업</li>
                    <li>지원 내용: 사업화 자금 최대 1.5억 원 + 글로벌 5G 프로그램(멘토링, 해외 진출 준비, 투자 유치 등 프로그램)</li>
                    <li>선정 규모: 60명 (미국 35개사, 싱가포르 15개사, 베트남 10개사)</li>
                    <li>모집 일정: 사업 공고(1월) > 신청·접수(2월) > 평가·발표(3월) > 프로그램 진행(3월~)</li>
                    <li>운영 기관: 중소벤처기업진흥공단 창업지원처</li>
                </ul>
            </div>
          </div>
        </div>

        <div id="academy" class="sub-section">
          <div class="card-box">
            <h2>청년 창업 사관학교</h2>
            <p>청년 창업 사관학교는 아이템 검증부터 사업화까지 전 과정을 지원하는 맞춤형 창업 지원 기관입니다.</p>
          </div>
        </div>

        <div id="helper" class="sub-section">
          <div class="card-box">
            <h2>청년 창업 지원 도우미</h2>
            <p>창업 관련 정보, 상담, 멘토링을 제공하는 청년 창업 지원 도우미 플랫폼을 활용해 보세요.</p>
          </div>
        </div>

      </div>
    </div>
  </div>
</body>
</html>

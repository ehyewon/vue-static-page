<template>
  <div class="app">
    <!-- 🌕 상단 인사 문구 -->
    <header class="header">
      <h1>🌕 한가위 잘 보내세요 🌾</h1>
      <p>보름달처럼 풍성하고 따뜻한 명절이 되길 바랍니다.</p>
    </header>

    <!-- 🌾 메인 영역 -->
    <main class="main">
      <div class="moon"></div>
      <div class="text-box">
        <h2>🍂 풍요로운 가을, 따뜻한 한가위</h2>
        <p>
          가족, 친구, 그리고 사랑하는 사람들과 함께<br />
          마음이 가득 찬 한가위를 보내세요.
        </p>
      </div>
    </main>

    <!-- 🍁 푸터 -->
    <footer class="footer">
      <p>© 2025 HanGawi Web. Made with 🌙 & Vue + Vite + TS</p>
    </footer>
  </div>
</template>

<script setup lang="ts">
// 별도 로직 없음 — 정적인 명절 페이지니까 깔끔하게 유지
</script>

<style scoped>
/* 🌕 전체 레이아웃 */
.app {
  font-family: 'Pretendard', 'Noto Sans KR', sans-serif;
  background: linear-gradient(to bottom, #f9d976, #f39f86);
  color: #3b2f2f;
  text-align: center;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

/* 🏮 상단 */
.header {
  padding: 3rem 1rem 1rem;
}

.header h1 {
  font-size: 2.2rem;
  margin-bottom: 0.6rem;
  animation: fadeIn 1.5s ease-in-out;
}

/* 🌾 메인 */
.main {
  flex: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  position: relative;
}

.moon {
  width: 160px;
  height: 160px;
  background: radial-gradient(circle at 30% 30%, #fffde8, #f6d365 70%);
  border-radius: 50%;
  box-shadow: 0 0 40px 15px rgba(255, 248, 180, 0.6);
  animation: glow 3s ease-in-out infinite alternate;
  margin-bottom: 2rem;
}

.text-box h2 {
  font-size: 1.6rem;
  margin-bottom: 0.5rem;
}

.text-box p {
  line-height: 1.7;
  font-size: 1rem;
}

/* 🍁 푸터 */
.footer {
  background: rgba(255, 255, 255, 0.3);
  padding: 1rem;
  font-size: 0.9rem;
  backdrop-filter: blur(4px);
  border-top: 1px solid rgba(255, 255, 255, 0.4);
}

/* 🌙 애니메이션 */
@keyframes glow {
  from {
    box-shadow: 0 0 20px 10px rgba(255, 248, 180, 0.4);
  }
  to {
    box-shadow: 0 0 60px 25px rgba(255, 248, 180, 0.8);
  }
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(-10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>

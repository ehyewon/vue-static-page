<template>
  <div class="app">
    <!-- 🌕 상단 인사 -->
    <header class="header">
      <h1>🌕 한가위 잘 보내세요 🌾</h1>
      <p>보름달 아래에서 마음이 풍성해지는 시간 되세요.</p>
    </header>

    <!-- 🌙 메인 장면 -->
    <main class="main">
      <div class="sky">
        <div class="moon"></div>
        <div class="stars"></div>

        <!-- 🐇 토끼 -->
        <div class="rabbit">
          <div class="ear left"></div>
          <div class="ear right"></div>
          <div class="head"></div>
          <div class="body"></div>
          <div class="stick"></div>
          <div class="mochi"></div>
        </div>
      </div>

      <!-- 🌾 문구 -->
      <div class="text-box">
        <h2>🍂 달빛 아래 정겨운 한가위</h2>
        <p>가족과 함께 웃음 가득한 명절 보내세요.</p>
      </div>
    </main>

    <!-- 🍁 푸터 -->
    <footer class="footer">
      <p>© 2025 HanGawi Web. Made with 🌕 & Vue + Vite + TS</p>
    </footer>
  </div>
</template>

<script setup lang="ts">
// 여기는 로직 없이 그대로 유지 — 정적인 페이지용
</script>

<style scoped>
.app {
  font-family: 'Pretendard', 'Noto Sans KR', sans-serif;
  background: linear-gradient(to bottom, #0b132b, #1c2541, #3a506b);
  color: #fffbe6;
  text-align: center;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  overflow: hidden;
}

/* 🌾 헤더 */
.header {
  padding: 2.5rem 1rem 1rem;
}
.header h1 {
  font-size: 2rem;
  margin-bottom: 0.5rem;
  animation: fadeIn 2s ease-in-out;
}

/* 🌙 메인 */
.main {
  flex: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.sky {
  position: relative;
  width: 100%;
  height: 250px;
  background: transparent;
  overflow: visible;
}

/* 🌕 달 */
.moon {
  position: absolute;
  top: 30px;
  left: 50%;
  transform: translateX(-50%);
  width: 180px;
  height: 180px;
  background: radial-gradient(circle at 30% 30%, #fff9c4, #fbc02d 70%);
  border-radius: 50%;
  box-shadow: 0 0 60px 20px rgba(255, 242, 173, 0.6);
  animation: moonGlow 3s ease-in-out infinite alternate;
}

/* ✨ 별 */
.stars {
  position: absolute;
  width: 100%;
  height: 100%;
  background-image: radial-gradient(white 1px, transparent 1px);
  background-size: 50px 50px;
  opacity: 0.3;
  animation: twinkle 5s infinite alternate;
}

/* 🐇 토끼 (간단 도형 조합) */
.rabbit {
  position: absolute;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
  width: 120px;
  height: 120px;
  animation: hop 2.5s ease-in-out infinite;
}

.ear {
  position: absolute;
  width: 20px;
  height: 50px;
  background: #fff;
  border-radius: 10px;
  top: -30px;
}

.ear.left {
  left: 40px;
  transform: rotate(-10deg);
}
.ear.right {
  left: 60px;
  transform: rotate(10deg);
}

.head {
  position: absolute;
  top: 10px;
  left: 40px;
  width: 40px;
  height: 40px;
  background: #fff;
  border-radius: 50%;
}

.body {
  position: absolute;
  top: 40px;
  left: 30px;
  width: 60px;
  height: 60px;
  background: #fff;
  border-radius: 50%;
}

/* 🪵 떡방아 찧는 막대 */
.stick {
  position: absolute;
  bottom: 0;
  left: 100px;
  width: 8px;
  height: 60px;
  background: #d4a373;
  transform-origin: bottom center;
  animation: pound 1.5s infinite ease-in-out;
}

/* 🍡 떡 */
.mochi {
  position: absolute;
  bottom: 0;
  left: 90px;
  width: 30px;
  height: 10px;
  background: #fff9e6;
  border-radius: 5px;
  box-shadow: 0 0 5px rgba(255,255,255,0.5);
}

/* 🌾 텍스트 */
.text-box {
  margin-top: 2.5rem;
}
.text-box h2 {
  font-size: 1.4rem;
  margin-bottom: 0.4rem;
}
.text-box p {
  line-height: 1.6;
  font-size: 1rem;
}

/* 🍁 푸터 */
.footer {
  background: rgba(255, 255, 255, 0.1);
  padding: 1rem;
  font-size: 0.9rem;
  backdrop-filter: blur(3px);
}

/* 🌟 애니메이션 */
@keyframes fadeIn {
  from { opacity: 0; transform: translateY(-10px); }
  to { opacity: 1; transform: translateY(0); }
}

@keyframes moonGlow {
  from { box-shadow: 0 0 40px 10px rgba(255, 242, 173, 0.4); }
  to { box-shadow: 0 0 80px 25px rgba(255, 242, 173, 0.8); }
}

@keyframes twinkle {
  from { opacity: 0.3; }
  to { opacity: 0.6; }
}

@keyframes hop {
  0%, 100% { transform: translate(-50%, 0); }
  50% { transform: translate(-50%, -8px); }
}

@keyframes pound {
  0%, 100% { transform: rotate(0deg); }
  50% { transform: rotate(-30deg); }
}
</style>

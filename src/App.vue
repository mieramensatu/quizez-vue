<script setup>
import { ref, watch } from "vue";
import srcQuiz from "./data/quizes";
import QuizCard from "./components/QuizCard.vue";

const quizes = ref(srcQuiz);
const search = ref("");

watch(search, () => {
  quizes.value = srcQuiz.filter((quiz) => {
    return quiz.title.toLowerCase().includes(search.value.toLowerCase());
  });
});
</script>

<template>
  <main>
    <header>
      <h1 id="title">Quizez</h1>
      <input
        v-model.trim="search"
        id="search-input"
        type="text"
        placeholder="Search..."
      />
    </header>
    <section id="quiz-container">
      <!-- <div v-for="quiz in quizes" :key="quiz.id" class="card">
        <img :src="quiz.img" :alt="quiz.title" />
        <div class="card-body">
          <h2>{{ quiz.title }}</h2>
          <p>{{ quiz.questions.length }} Question</p>
        </div>
      </div> -->
      <QuizCard v-for="quiz in quizes" :key="quiz.id" :quiz="quiz"/>
    </section>
  </main>
</template>
<style scoped>
main {
  width: 70%;
  margin: auto;
}

header {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
#title {
  font-size: 2rem;
  color: #212121;
  font-weight: 400;
}
#search-input {
  height: 2rem;
  padding: 0 1rem;
  border: none;
  border-radius: 3px;
  color: #212121;
  font-size: 1rem;
  outline: none;
  background-color: #9c9c9c9c;
}
#search-input:focus {
  background-color: #e0e0e0;
  color: #212121;
  border: 1px solid #9c9c9c9c;
  border-radius: 3px;
}

#quiz-container {
  display: flex;
  flex-wrap: wrap;
  margin-top: 20px;
}
</style>

<template>
  <main>
    <header>
      <h1 id="title">Quizez</h1>
      <input id="search-input" type="text" placeholder="Search..." />
    </header>
    <section id="quiz-container">
      <div class="card">
        <img src="./assets/photo-1542831371-29b0f74f9713.jpg" alt="programming" width="30%">
        <div class="card-body">
          <h2>Programming</h2>
          <p>2 question</p>
        </div>
      </div>
      <div class="card">
        <img src="./assets/photo-1542831371-29b0f74f9713.jpg" alt="programming" width="30%">
        <div class="card-body">
          <h2>Programming</h2>
          <p>2 question</p>
        </div>
      </div>
    </section>
  </main>
</template>

<style scoped>

main{
  width: 70%;
  margin: auto;
}

header {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
#title{
  font-size: 2rem;
  color: #212121;
  font-weight: 400;
}
#search-input{
  height: 2rem;
  padding: 0 1rem;
  border: none;
  border-radius: 3px;
  color: #212121;
  font-size: 1rem;
  outline: none;
  background-color: #9c9c9c9c;
}
#search-input:focus{
  background-color: #e0e0e0;
  color: #212121;
  border: 1px solid #9c9c9c9c;
  border-radius: 3px;
}

#quiz-container{
  display: flex;
  flex-wrap: wrap;
  margin-top: 20px;
}

.card{
  width: 270px;
  margin-right: 30px;
  margin-bottom: 30px;
  border-radius: 5px;
  overflow: hidden;
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
}

.card img{
  width: 100%;
  height: 200px;
  object-fit: cover;
  margin: 0;
}


.card-body{
  padding: 0 15px;
}

.card-body h2{
  font-weight: bold;
}
</style>

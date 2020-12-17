<template>
<div>
  <ul class="cards" v-for="post in posts" :key="post.id">
    <li class="cards__item">
      <div class="card">
        <div class="card__image card__image--fence"></div>
        <div class="card__content">
          <div class="card__title">Текст поста</div>
          <p class="card__text">Среднерусский край во власти осени. Волна холода спадает, и опять водворяется тепло. Воздух прогрет, а на солнце так и припекает. В спокойном воздухе дрожат паутинки. Оживились скворцы, их бодрит тепло. По жнивью важно гуляют грачи, держатся вместе, чтобы приготовиться к скорому отлету. В лесу осинка закраснела, скоро лист начнет осыпаться. Стволы ее от избытка крахмала стали сизыми, словно припудрились. </p>
          <button class="btn">Подробнее</button>
        </div>
      </div>
    </li>
    <li class="cards__item">
      <div class="card">
        <div class="card__image card__image--fence"></div>
        <div class="card__content">
          <div class="card__title">Текст поста</div>
          <p class="card__text">Среднерусский край во власти осени. Волна холода спадает, и опять водворяется тепло. Воздух прогрет, а на солнце так и припекает. В спокойном воздухе дрожат паутинки. Оживились скворцы, их бодрит тепло. По жнивью важно гуляют грачи, держатся вместе, чтобы приготовиться к скорому отлету. В лесу осинка закраснела, скоро лист начнет осыпаться. Стволы ее от избытка крахмала стали сизыми, словно припудрились. </p>
          <button class="btn">Подробнее</button>
        </div>
      </div>
    </li>
    <li class="cards__item">
      <div class="card">
        <div class="card__image card__image--fence"></div>
        <div class="card__content">
          <div class="card__title">Текст поста</div>
          <p class="card__text">Среднерусский край во власти осени. Волна холода спадает, и опять водворяется тепло. Воздух прогрет, а на солнце так и припекает. В спокойном воздухе дрожат паутинки. Оживились скворцы, их бодрит тепло. По жнивью важно гуляют грачи, держатся вместе, чтобы приготовиться к скорому отлету. В лесу осинка закраснела, скоро лист начнет осыпаться. Стволы ее от избытка крахмала стали сизыми, словно припудрились. </p>
          <button class="btn">Подробнее</button>
        </div>
      </div>
    </li>
    <li class="cards__item">
      <div class="card">
        <div class="card__image card__image--fence"></div>
        <div class="card__content">
          <div class="card__title">Текст поста</div>
          <p class="card__text">Среднерусский край во власти осени. Волна холода спадает, и опять водворяется тепло. Воздух прогрет, а на солнце так и припекает. В спокойном воздухе дрожат паутинки. Оживились скворцы, их бодрит тепло. По жнивью важно гуляют грачи, держатся вместе, чтобы приготовиться к скорому отлету. В лесу осинка закраснела, скоро лист начнет осыпаться. Стволы ее от избытка крахмала стали сизыми, словно припудрились. </p>
          <button class="btn">Подробнее</button>
        </div>
      </div>
    </li>
    <li class="cards__item">
      <div class="card">
        <div class="card__image card__image--fence"></div>
        <div class="card__content">
          <div class="card__title">Текст поста</div>
          <p class="card__text">Среднерусский край во власти осени. Волна холода спадает, и опять водворяется тепло. Воздух прогрет, а на солнце так и припекает. В спокойном воздухе дрожат паутинки. Оживились скворцы, их бодрит тепло. По жнивью важно гуляют грачи, держатся вместе, чтобы приготовиться к скорому отлету. В лесу осинка закраснела, скоро лист начнет осыпаться. Стволы ее от избытка крахмала стали сизыми, словно припудрились. </p>
          <button class="btn">Подробнее</button>
        </div>
      </div>
    </li>
    <li class="cards__item">
      <div class="card">
        <div class="card__image card__image--fence"></div>
        <div class="card__content">
          <div class="card__title">Текст поста</div>
          <p class="card__text">Среднерусский край во власти осени. Волна холода спадает, и опять водворяется тепло. Воздух прогрет, а на солнце так и припекает. В спокойном воздухе дрожат паутинки. Оживились скворцы, их бодрит тепло. По жнивью важно гуляют грачи, держатся вместе, чтобы приготовиться к скорому отлету. В лесу осинка закраснела, скоро лист начнет осыпаться. Стволы ее от избытка крахмала стали сизыми, словно припудрились. </p>
          <button class="btn">Подробнее</button>
        </div>
      </div>
    </li>
  </ul>
</div>
</template>
<script>
export default {
  name: "app",
  data() {
    return {
      posts: []
    }
  },
  async mounted() {
    const res = await fetch('https://jsonplaceholder.typicode.com/posts?_limit=3')
    const posts = await res.json()
    this.posts = posts
  }
}
</script>
<style>
img {
  height: auto;
  max-width: 100%;
  vertical-align: middle;
}

.cards {
  display: -webkit-box;
  display: flex;
  flex-wrap: wrap;
  list-style: none;
  margin: 0;
  padding: 0;
}
.cards__item {
  display: -webkit-box;
  display: flex;
  padding: 1rem;
}
@media (min-width: 40rem) {
  .cards__item {
    width: 50%;
  }
}
@media (min-width: 56rem) {
  .cards__item {
    width: 33.3333%;
  }
}
.card {
  background-color: white;
  border-radius: 0.25rem;
  box-shadow: 0 20px 40px -14px rgba(0, 0, 0, 0.25);
  display: -webkit-box;
  display: flex;
  -webkit-box-orient: vertical;
  -webkit-box-direction: normal;
  flex-direction: column;
  overflow: hidden;
}
.card:hover .card__image {
  -webkit-filter: contrast(100%);
  filter: contrast(100%);
}
.card__content {
  display: -webkit-box;
  display: flex;
  -webkit-box-flex: 1;
  flex: 1 1 auto;
  -webkit-box-orient: vertical;
  -webkit-box-direction: normal;
  flex-direction: column;
  padding: 1rem;
}
.card__image {
  background-position: center center;
  background-repeat: no-repeat;
  background-size: cover;
  border-top-left-radius: 0.25rem;
  border-top-right-radius: 0.25rem;
  -webkit-filter: contrast(70%);
  filter: contrast(70%);
  overflow: hidden;
  position: relative;
  -webkit-transition: -webkit-filter 0.5s cubic-bezier(0.43, 0.41, 0.22, 0.91);
  transition: -webkit-filter 0.5s cubic-bezier(0.43, 0.41, 0.22, 0.91);
  transition: filter 0.5s cubic-bezier(0.43, 0.41, 0.22, 0.91);
  transition: filter 0.5s cubic-bezier(0.43, 0.41, 0.22, 0.91), -webkit-filter 0.5s cubic-bezier(0.43, 0.41, 0.22, 0.91);
}
.card__image::before {
  content: "";
  display: block;
  padding-top: 56.25%;
}
@media (min-width: 40rem) {
  .card__image::before {
    padding-top: 66.6%;
  }
}
.card__image--flowers {
  background-image: url(https://unsplash.it/800/600?image=82);
}
.card__image--river {
  background-image: url(https://unsplash.it/800/600?image=11);
}
.card__image--record {
  background-image: url(https://unsplash.it/800/600?image=39);
}
.card__image--fence {
  background-image: url(https://unsplash.it/800/600?image=59);
}
.card__title {
  color: #696969;
  font-size: 1.25rem;
  font-weight: 300;
  letter-spacing: 2px;
  text-transform: uppercase;
}
.card__text {
  -webkit-box-flex: 1;
  flex: 1 1 auto;
  font-size: 0.875rem;
  line-height: 1.5;
  margin-bottom: 1.25rem;
}
</style>

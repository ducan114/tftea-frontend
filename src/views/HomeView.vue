<template>
  <div class="parallax">
    <div class="parallax__content">
      <div class="parallax__layer parallax__layer--1"></div>
      <img
        class="image parallax__layer parallax__layer--2"
        src="@/assets/images/hero/layer-background-800w.png"
        srcset="
          @/assets/images/hero/layer-background-200w.png   200w,
          @/assets/images/hero/layer-background-400w.png   400w,
          @/assets/images/hero/layer-background-800w.png   800w,
          @/assets/images/hero/layer-background-1200w.png 1200w,
          @/assets/images/hero/layer-background-1600w.png 1600w,
          @/assets/images/hero/layer-background-2560w.png 2560w
        "
        alt="hero-image-background"
      />
      <img
        class="image parallax__layer parallax__layer--3"
        src="@/assets/images/hero/layer-1-800w.png"
        srcset="
          @/assets/images/hero/layer-1-200w.png   200w,
          @/assets/images/hero/layer-1-400w.png   400w,
          @/assets/images/hero/layer-1-800w.png   800w,
          @/assets/images/hero/layer-1-1200w.png 1200w,
          @/assets/images/hero/layer-1-1600w.png 1600w,
          @/assets/images/hero/layer-1-2560w.png 2560w
        "
        alt="hero-image-layer-1"
      />
      <img
        class="image parallax__layer parallax__layer--4"
        src="@/assets/images/hero/layer-2-800w.png"
        srcset="
          @/assets/images/hero/layer-2-200w.png   200w,
          @/assets/images/hero/layer-2-400w.png   400w,
          @/assets/images/hero/layer-2-800w.png   800w,
          @/assets/images/hero/layer-2-1200w.png 1200w,
          @/assets/images/hero/layer-2-1600w.png 1600w,
          @/assets/images/hero/layer-2-2560w.png 2560w
        "
        alt="hero-image-layer-2"
      />
      <img
        class="image parallax__layer parallax__layer--5"
        src="@/assets/images/hero/layer-3-800w.png"
        srcset="
          @/assets/images/hero/layer-3-200w.png   200w,
          @/assets/images/hero/layer-3-400w.png   400w,
          @/assets/images/hero/layer-3-800w.png   800w,
          @/assets/images/hero/layer-3-1200w.png 1200w,
          @/assets/images/hero/layer-3-1600w.png 1600w,
          @/assets/images/hero/layer-3-2560w.png 2560w
        "
        alt="hero-image-layer-3"
      />
      <h1 class="h1 parallax__title">
        Ch??o m???ng b???n ?????n v???i ?????u tr?????ng ch??n l?? m??a 7
      </h1>
      <h2 class="h2 parallax__layer parallax__layer--subtitle">
        H??y s???n s??ng b?????c v??o th??? gi???i r???ng r???ng l???n!
      </h2>
    </div>
    <section class="section">
      <div class="container section__content">
        <h2 class="h2">T?????ng</h2>
        <p>
          58 v??? t?????ng m???i v???i c??c t???c h??? ??a d???ng s???n s??ng nh???n l???nh! H??y ngay
          l???p t???c gh?? qua c???a h??ng ????? ??i t??m nh??n ph???m n??o!
        </p>
        <img
          class="image"
          src="@/assets/images/champion-cheatsheet.png"
          alt="champion_cheatsheet"
        />
        <RouterLink
          class="router-link btn btn--info btn--rounded btn--outlined"
          :to="{ name: 'champions' }"
        >
          T??m hi???u th??m
          <span class="material-symbols-outlined">arrow_right_alt</span>
        </RouterLink>
      </div>
    </section>
    <section class="section section--reversed">
      <div class="container section__content">
        <h2 class="h2">Trang b???</h2>
        <p>
          C??c trang b??? quen thu???c ???????c gi??? l???i v?? nhi???u trang b??? m???i ???????c th??m
          v??o. ?????c bi???t l?? s??? su???t hi???n c???a m???t s??? trang b??? ?????c tr??ng c???a
          t???c/h???!
        </p>
        <img
          class="image"
          src="@/assets/images/item-cheatsheet.jpg"
          alt="champion_cheatsheet"
        />
        <RouterLink
          class="router-link btn btn--info btn--rounded"
          :to="{ name: 'items' }"
        >
          T??m hi???u th??m
          <span class="material-symbols-outlined">arrow_right_alt</span>
        </RouterLink>
      </div>
    </section>
    <section class="section">
      <div class="container section__content">
        <h2 class="h2">X??y d???ng d???i h??nh</h2>
        <p>
          H??y v???n d???ng kh??? n??ng t?? duy s??ng t???o c???a b???n, s??? d???ng c??c v??? t?????ng v??
          c??c trang b??? c?? s???n ????? t???o n??n c??c ?????i h??nh m???nh m??? ??em ?????n nh???ng tr???n
          chi???n m??n nh??n, ?????y c???m x??c.
        </p>
        <p>
          Ch??ng t??i cung c???p cho b???n m???t c??ng c??? ti???n l???i ????? thi???t l???p v?? l??u
          tr??? nh???ng ?????i h??nh y??u th??ch!
        </p>
        <RouterLink class="router-link" :to="{ name: 'team-builder' }">
          <HexGrid :rows="4" :cellsPerRow="7" />
          <div class="text text--info">
            <span class="material-symbols-outlined">info</span>
            <span>Nh???p v??o s??n ?????u ????? b???t ?????u</span>
          </div>
        </RouterLink>
      </div>
    </section>
  </div>
</template>

<script setup>
import HexGrid from '@/components/HexGrid.vue';
</script>

<style scoped lang="scss">
.parallax {
  height: calc(100vh - var(--header-height));
  perspective: 10px;
  overflow-y: auto;
  overflow-x: hidden;
  scroll-behavior: smooth;

  &__title {
    color: transparent;
    background: linear-gradient(45deg, #bfacff, white, #b3ddf1);
    background-clip: text;
    -webkit-background-clip: text;
  }

  &__content {
    height: 100%;
    transform-style: preserve-3d;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    position: relative;
    z-index: -1;
  }

  &__layer {
    position: absolute;

    &--1,
    &--2,
    &--3,
    &--4,
    &--5 {
      inset: 0;
    }

    &--1 {
      background: linear-gradient(rgb(253, 206, 79), rgb(251, 102, 79));
      transform: translateZ(-30px) scale(4.05);
    }

    &--2 {
      transform: translateZ(-20px) scale(3.05);
    }

    &--3 {
      transform: translateZ(-10px) scale(2.05);
    }

    &--4 {
      transform: translateZ(-5px) scale(1.55);
    }

    &--5 {
      transform: translateZ(-8px) scale(1.85);
    }

    &--subtitle {
      color: transparent;
      background: linear-gradient(45deg, #bfacff, white, #b3ddf1);
      background-clip: text;
      -webkit-background-clip: text;
      top: 95%;
      transform: translateZ(2px) scale(0.8);
    }
  }
}

.section {
  color: var(--color-text);
  background-color: var(--color-background);
  padding: 1em 0;

  &--reversed {
    color: var(--color-background);
    background-color: var(--color-text);
  }

  &__content {
    display: flex;
    flex-direction: column;
    row-gap: 1em;
  }

  .btn {
    align-self: center;
  }
}

.router-link {
  .material-symbols-outlined:last-child {
    transition: transform 150ms ease-in-out;
  }

  &:hover {
    .material-symbols-outlined:last-child {
      transform: translateX(0.25em);
    }
  }
}

.text--info {
  display: flex;
  align-items: center;
  justify-content: center;
  column-gap: 0.5em;
}
</style>

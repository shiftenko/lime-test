<template>

<div class="news-item">
  <div class="cont">
    <a
      href="##"
      class="img"
    >
      <img
        src="~@/img/news/jbl.jpg"
        alt=""
      >
    </a>
    <a
      href="##"
      class="descr-and-gradient-mask"
    >
      JBL и DNS приглашают в Сочи Lorem ipsum dolor sit amet.
    </a>
  </div>
  <span class="date">26 февраля 2019 г. 10:41</span>
  <a href="##"></a>
</div>

</template>
<script>

export default {

};

</script>
<style scoped lang="scss">

.news-item {
  @include vhMedia(2vh, margin-right, (tablet: 15%));
  @include vhMedia(1.5vh, border-radius, (tablet: 15%));
  position: relative;
  flex: 1 1 0;
  height: 100%;
  overflow: hidden;
  border: $bord;

  @media (min-width: $media-pc) {
    padding: 16.728px 17.22px 14.76px;
    margin-right: 0;
    border: 0;
    border-bottom: $bord;
    border-radius: 0;

    &:first-child {
      padding-top: 0;
    }

    &:last-child {
      border-bottom: 0;
    }
  }

  &:last-child {
    margin-right: 0;
  }

  > a {
    @include hide-on-pc;
    position: absolute;
    top: 0;
    z-index: 20;
    width: 100%;
    height: 100%;
  }
}

.cont {
  position: relative;
  border-bottom: $bord;

  @media (min-width: $media-pc) {
    margin-bottom: 6%;
    border: 0;
  }
}

.img {
  display: block;

  @media (min-width: $media-pc) {
    margin-bottom: 7%;
    border: 0;
  }

  > img {
    display: block;
    width: 100%;
  }
}

.descr-and-gradient-mask {
  @include font(
    $size: 2.8vh,
    $color: $text-col-light,
    $lineHeight: 3.8vh,
    $weight: 600,
    $textAlign: center,
    $changePercOn: (tablet: 15%)
  );
  position: absolute;
  top: 0;
  align-items: center;
  z-index: 10;
  display: flex;
  width: 100%;
  height: 100%;
  padding: 0 6%;
  background: radial-gradient(
    circle at 5.92% 19.67%,
    rgba(130, 22, 22, 0.8) 0%,
    rgba(130, 25, 22, 0.8) 16.67%,
    rgba(118, 54, 8, 0.8) 57.47%,
    rgba(109, 12, 12, 0.8) 100%
  ) 105% 105%;

  @media (min-width: $media-pc) {
    @include font(
      $size: 13.776px,
      $color: currentColor,
      $lineHeight: 19.68px,
      $weight: 400,
      $textAlign: left
    );
    position: static;
    display: block;
    padding: 0;
    background: none;
  }
}

.date {
  @include font(
    $size: 2vh,
    $color: $text-col-dark,
    $changePercOn: (tablet: 15%)
  );
  display: block;
  padding: 0 5.5%;
  margin-top: 4.6%;

  @media (min-width: $media-pc) {
    padding: 0;
    margin: 0;
    font-size: 13.3px;
  }
}

</style>
<template>
  <section class="about">
    <h2 class="about-title">About</h2>
    <figure class="about-image">
      <img src="../../icon.jpg">
    </figure>
    <p class="about-name">ozaki futa</p>
    <p class="about-birthday">2001 / 08 / 26</p>
    <p class="about-skill">HTML / CSS / Javascript / Photoshop / Illustrator</p>
  </section>
</template>

<style lang="scss" scoped>
.about {
  padding: 16px 0;
  background-color: #39C;
  color: #fff;
  position: relative;
  min-height: 300px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  overflow: hidden;
  & > * {
    padding: 0 12px;
    margin: 0 auto;
    width: 100%;
    max-width: 896px;
  }
  &:after {
    margin: 0 auto;
    position: absolute;
    display: block;
    content: '';
    width: 2000px;
    height: 2000px;
    background-color: rgba(0, 0, 0, 0.1);
    transform: rotate(15deg);
    left: -1900px;
    right: 0;
  }
}
.about-title {
  margin: 0 auto 8px;
  font-size: 24px;
  position: relative;
  &:after {
    content: '';
    display: block;
    border-bottom: 1px solid #fff;
    width: 200px;
  }
}
.about-image {
  margin: auto;
  width: 130px;
  height: 130px;
  background-color: #fff;
  border-radius: 6px;
  position: absolute;
  top: 0;
  left: 720px;
  right: 20px;
  bottom: 0;

  @media screen and (max-width:600px) {
    margin: 10px auto;
    position: static;
  }
  @media screen and (max-width:884px) {
    left: auto;
  }
}
.about-name {
  font-size: 20px;
}
.about-birthday {
  font-size: 14px;
  margin-bottom: 16px;
}
.about-skill {
  font-size: 16px;
}
</style>
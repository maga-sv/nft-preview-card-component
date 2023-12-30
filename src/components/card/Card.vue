<script setup>
import EthereumIcon from "@/assets/images/EthereumIcon.vue";
import ViewIcon from "@/assets/images/ViewIcon.vue";
</script>

<template>
  <div class="card">
    <div class="card__img">
      <img src="@/assets/images/image-equilibrium.jpg" alt="" />
      <ViewIcon class="card__img-view" />
    </div>

    <a href="#!" class="card__name">Equilibrium #3429</a>

    <p class="card__txt">
      Our Equilibrium collection promotes balance and calm.
    </p>

    <div class="card__info">
      <div class="card__info-price">
        <EthereumIcon /> <span>0.041 ETH</span>
      </div>

      <span class="card__info-date">3 days left</span>
    </div>

    <div class="card__user">
      <a href="#!" class="card__user-ava">
        <img src="@/assets/images/image-avatar.png" alt="" />
      </a>

      <div class="card__user-info">
        <span class="card__user-info-txt">Creation of</span>

        <a href="#!" class="card__user-info-name">Jules Wyvern</a>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.card {
  background: var(--cardBg);
  padding: 25px;
  max-width: 350px;
  width: 100%;
  border-radius: 10px;

  &__img {
    border-radius: 10px;
    width: 300px;
    height: 300px;
    margin-bottom: 20px;
    cursor: pointer;
    overflow: hidden;
    position: relative;

    img {
      object-fit: cover;
      height: 100%;
      width: 100%;
    }

    &-view {
      position: absolute;
      bottom: -100%;
      left: 0;
      height: 100%;
      width: 100%;
      background: var(--secondaryColorHover);
      transition: 400ms;
      z-index: 0;
      opacity: 0;
    }
    
    &:hover &-view {
      bottom: 0;
      opacity: 1;
      z-index: 1;
    }
  }

  &__name {
    display: inline-block;
    margin-bottom: 20px;
    color: var(--accentColor);
    font-size: 22px;
    transition: 400ms;

    &:hover {
      color: var(--secondaryColor);
    }
  }

  &__txt {
    margin-bottom: 20px;
    font-size: 18px;
    color: var(--primaryColor);
  }

  &__info {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;

    &-price {
      color: var(--secondaryColor);
      display: flex;
      align-items: center;
      gap: 6px;
      font-size: 18px;
      flex-direction: row;
    }

    &-date {
      color: var(--primaryColor);
    }
  }

  &__user {
    display: flex;
    padding: 15px 0;
    align-items: center;
    gap: 15px;
    border-top: 1px solid var(--lineColor);

    &-ava {
      width: 40px;
      height: 40px;
      border-radius: 50%;
      border: 2px solid var(--accentColor);

      img {
        object-fit: cover;
        height: 100%;
        width: 100%;
      }
    }

    &-info {
      font-size: 18px;
      display: flex;
      gap: 5px;

      &-txt {
        color: var(--primaryColor);
      }

      &-name {
        color: var(--accentColor);
        transition: 400ms;

        &:hover {
          color: var(--secondaryColor);
        }
      }
    }
  }
}
</style>

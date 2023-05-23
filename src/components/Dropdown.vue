<template>
  <div class="dropdown" @click.stop="toggleDropdown">
    <div class="dropdown__container">
      <div class="dropdown__header">
        <button class="dropdown__btn" @click="toggleDropdown">
          <slot name="header"></slot>
        </button>
        <div class="dropdown__content" :class="{open: isOpen}">
          <ul class="dropdown__content-list">
            <li class="dropdown__content-item">
              <a class="dropdown__content-link" href="#">Profile</a>
            </li>
            <li class="dropdown__content-item">
              <a class="dropdown__content-link" href="#">Settings</a>
            </li>
            <li class="dropdown__content-item">
              <a class="dropdown__content-link" href="#">Exit</a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Dropdown",
  props: {
    links: {
      type: Array,
    }
  },
  data() {
    return {
      isOpen: false,
    }
  },
  methods: {
    toggleDropdown() {
      let dropdownContent = this.$el.querySelector('.dropdown__content')
      if (this.isOpen) {
        dropdownContent.style.top = '0'
        dropdownContent.style.opacity = '0'
        setTimeout(() => {
          dropdownContent.style.visibility = 'hidden'
        }, 100)
      } else {
        dropdownContent.style.top = '45px'
        dropdownContent.style.opacity = '1'
        dropdownContent.style.visibility = 'visible'
      }
      this.isOpen = !this.isOpen
    }
  }
}
</script>

<style lang="scss" scoped>
ul, li {
  list-style: none;
}

.dropdown {
  &__header {
    position: relative;
  }
  &__btn {
    background-color: transparent;
    border: none;
    outline: none;
  }
  &__content {
    position: absolute;
    top: 0;
    opacity: 0;
    visibility: hidden;

    min-width: 100%;
    padding: 10px 0;
    background-color: #edf2f7;
    border-radius: 10px;

    transition: top .2s linear, opacity .2s linear;
  }
  &__content .open {
    top: calc(100% + 15px);
    opacity: 1;
  }
  &__content-list {
    display: flex;
    justify-content: center;
    flex-direction: column;
    gap: 5px;
  }
  &__content-item {
    display: flex;
    transition: background-color .1s linear;
    &:hover {
      background-color: #b4e3fb;
    }
  }
  &__content-link {
    text-decoration: none;
    color: #000;
    width: 100%;
    padding: 5px 0 5px 10px;
  }
}
</style>
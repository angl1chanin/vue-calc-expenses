<template>
  <aside class="nav" :class="{hide: isHide}">
    <div class="nav__container">
      <div class="nav__logo">
        <p v-if="!isHide">Expenses Calculator</p>
        <p v-else>EC</p>
      </div>
      <div class="nav__expand">
        <button class="nav__expand-btn" @click="toggleNav">
          <svg xmlns="http://www.w3.org/2000/svg" width="800px" height="800px" viewBox="0 0 15 15" fill="none">
            <path fill-rule="evenodd" clip-rule="evenodd" d="M2.14645 11.1464C1.95118 11.3417 1.95118 11.6583 2.14645 11.8536C2.34171 12.0488 2.65829 12.0488 2.85355 11.8536L6.85355 7.85355C7.04882 7.65829 7.04882 7.34171 6.85355 7.14645L2.85355 3.14645C2.65829 2.95118 2.34171 2.95118 2.14645 3.14645C1.95118 3.34171 1.95118 3.65829 2.14645 3.85355L5.79289 7.5L2.14645 11.1464ZM8.14645 11.1464C7.95118 11.3417 7.95118 11.6583 8.14645 11.8536C8.34171 12.0488 8.65829 12.0488 8.85355 11.8536L12.8536 7.85355C13.0488 7.65829 13.0488 7.34171 12.8536 7.14645L8.85355 3.14645C8.65829 2.95118 8.34171 2.95118 8.14645 3.14645C7.95118 3.34171 7.95118 3.65829 8.14645 3.85355L11.7929 7.5L8.14645 11.1464Z" fill="#000000"/>
          </svg>
        </button>
      </div>
      <ul class="nav__items">
        <li class="nav__item">
          <router-link class="nav__item-link" to="/dashboard">
            <svg width="800px" height="800px" viewBox="0 0 24 24" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
              <title>Align-Right</title>
              <g id="Page-1" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
                <g id="Align-Right">
                  <rect id="Rectangle" fill-rule="nonzero" x="0" y="0" width="24" height="24">

                  </rect>
                  <line x1="5" y1="6" x2="19" y2="6" id="Path" stroke="#0C0310" stroke-width="2" stroke-linecap="round">

                  </line>
                  <line x1="5" y1="14" x2="19" y2="14" id="Path" stroke="#0C0310" stroke-width="2" stroke-linecap="round">

                  </line>
                  <line x1="11" y1="10" x2="19" y2="10" id="Path" stroke="#0C0310" stroke-width="2" stroke-linecap="round">

                  </line>
                  <line x1="11" y1="18" x2="19" y2="18" id="Path" stroke="#0C0310" stroke-width="2" stroke-linecap="round">

                  </line>
                </g>
              </g>
            </svg>
            <p class="nav__item-name">Dashboard</p>
          </router-link>
        </li>
        <li class="nav__item">
          <router-link class="nav__item-link" to="/budget">
            <svg fill="#000000" width="800px" height="800px" viewBox="0 0 24 24" id="Main" xmlns="http://www.w3.org/2000/svg"><title/><path d="M18.23,2H5.77A3.77,3.77,0,0,0,2,5.77V18.23A3.77,3.77,0,0,0,5.77,22H18.23A3.77,3.77,0,0,0,22,18.23V5.77A3.77,3.77,0,0,0,18.23,2ZM20,18.23A1.77,1.77,0,0,1,18.23,20H5.77A1.77,1.77,0,0,1,4,18.23V5.77A1.77,1.77,0,0,1,5.77,4H18.23A1.77,1.77,0,0,1,20,5.77Z"/><path d="M8,11H7a1,1,0,0,0,0,2H8a1,1,0,0,0,0-2Z"/><path d="M8,14H7a1,1,0,0,0,0,2H8a1,1,0,0,0,0-2Z"/><path d="M13,11H11a1,1,0,0,0,0,2h2a1,1,0,0,0,0-2Z"/><path d="M13,14H11a1,1,0,0,0,0,2h2a1,1,0,0,0,0-2Z"/><path d="M8,17H7a1,1,0,0,0,0,2H8a1,1,0,0,0,0-2Z"/><path d="M13,17H11a1,1,0,0,0,0,2h2a1,1,0,0,0,0-2Z"/><path d="M17,11H16a1,1,0,0,0,0,2h1a1,1,0,0,0,0-2Z"/><path d="M18,5H6A1,1,0,0,0,5,6V9a1,1,0,0,0,1,1H18a1,1,0,0,0,1-1V6A1,1,0,0,0,18,5ZM17,8H7V7H17Z"/><rect height="5" rx="1" width="3" x="15" y="14"/></svg>
            <p class="nav__item-name">Budget</p>
          </router-link>
        </li>
        <li class="nav__item">
          <router-link class="nav__item-link" to="/add-expenses">
            <svg width="800px" height="800px" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">

              <title/>

              <g id="Complete">

                <g data-name="add" id="add-2">

                  <g>

                    <line fill="none" stroke="#000000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" x1="12" x2="12" y1="19" y2="5"/>

                    <line fill="none" stroke="#000000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" x1="5" x2="19" y1="12" y2="12"/>

                  </g>

                </g>

              </g>

            </svg>
            <p class="nav__item-name">Add expenses</p>
          </router-link>
        </li>
      </ul>
    </div>
  </aside>
</template>

<script>
import Dropdown from "@/components/Dropdown";

export default {
  name: "Sidebar",
  components: { Dropdown },
  data() {
    return {
      isHide: false,
    }
  },
  methods: {
    toggleNav() {
      this.isHide = !this.isHide
    },
  }
}
</script>

<style lang="scss" scoped>

ul, li, p {
  padding: 0;
  margin: 0;
  list-style: none;
}

button {
  border: none;
  background: none;
  cursor: pointer;
}

.nav {
  width: 250px;
  height: 100vh;
  background-color: #fff;
  transition: width .2s linear;

  &.hide {
    width: 75px;
  }

  &__container {}

  &__logo {
    text-align: center;
    padding: 20px;
    margin-bottom: 10px;

    p {
      font-size: 20px;
    }
  }

  &__expand {
    display: flex;
    justify-content: flex-end;
    padding: 20px;
  }

  &.hide &__expand {
    justify-content: center;
  }

  &__expand-btn {
    svg {
      width: 20px !important;
      height: 20px !important;
    }
  }

  &__items {
    display: flex;
    flex-direction: column;
    gap: 30px;
  }

  &__item {
    width: 100%;

    &:hover {
      background-color: #F7FBFF;
      .nav__item-name, svg {
        color: #3D82BE;
        fill: #3D82BE;
      }
      line {
        stroke: #3D82BE;
      }
    }
  }

  &__item-link {
    padding: 10px 0 10px 20px;
    display: flex;
    align-items: center;
    flex-wrap: nowrap;
    height: 100%;
    gap: 10px;
    text-decoration: none;
  }

  &.hide &__item-link {
    padding: 10px;
    justify-content: center;
  }

  svg {
    transition: .2s linear;
    width: 25px;
    height: 25px;
    fill: #9FB1C3;
  }

  line {
    transition: .2s linear;
    stroke: #9FB1C3;
  }


  &__item-name {
    transition: .2s linear;
    font-weight: 400;
    color: #5E646B;
    text-transform: capitalize;
  }

  &.hide &__item-name {
    display: none;
  }
}
</style>
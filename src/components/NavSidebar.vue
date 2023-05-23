<template>
  <aside class="menu">
    <div class="menu__container">
      <div class="menu__logo">
        <p>Expenses Calculator</p>
      </div>
      <ul class="menu__items">
        <li class="menu__item">
          <router-link class="menu__item-link" to="/dashboard">
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
            <p class="menu__item-name">Dashboard</p>
          </router-link>
        </li>
        <li class="menu__item">
          <router-link class="menu__item-link" to="/budget">
            <svg fill="#000000" width="800px" height="800px" viewBox="0 0 24 24" id="Main" xmlns="http://www.w3.org/2000/svg"><title/><path d="M18.23,2H5.77A3.77,3.77,0,0,0,2,5.77V18.23A3.77,3.77,0,0,0,5.77,22H18.23A3.77,3.77,0,0,0,22,18.23V5.77A3.77,3.77,0,0,0,18.23,2ZM20,18.23A1.77,1.77,0,0,1,18.23,20H5.77A1.77,1.77,0,0,1,4,18.23V5.77A1.77,1.77,0,0,1,5.77,4H18.23A1.77,1.77,0,0,1,20,5.77Z"/><path d="M8,11H7a1,1,0,0,0,0,2H8a1,1,0,0,0,0-2Z"/><path d="M8,14H7a1,1,0,0,0,0,2H8a1,1,0,0,0,0-2Z"/><path d="M13,11H11a1,1,0,0,0,0,2h2a1,1,0,0,0,0-2Z"/><path d="M13,14H11a1,1,0,0,0,0,2h2a1,1,0,0,0,0-2Z"/><path d="M8,17H7a1,1,0,0,0,0,2H8a1,1,0,0,0,0-2Z"/><path d="M13,17H11a1,1,0,0,0,0,2h2a1,1,0,0,0,0-2Z"/><path d="M17,11H16a1,1,0,0,0,0,2h1a1,1,0,0,0,0-2Z"/><path d="M18,5H6A1,1,0,0,0,5,6V9a1,1,0,0,0,1,1H18a1,1,0,0,0,1-1V6A1,1,0,0,0,18,5ZM17,8H7V7H17Z"/><rect height="5" rx="1" width="3" x="15" y="14"/></svg>
            <p class="menu__item-name">Budget</p>
          </router-link>
        </li>
        <li class="menu__item">
          <router-link class="menu__item-link" to="/add-expenses">
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
            <p class="menu__item-name">Add expenses</p>
          </router-link>
        </li>
      </ul>
    </div>
  </aside>
</template>

<script>
export default {
  name: "Sidebar",
  methods: {

  }
}
</script>

<style lang="scss" scoped>
ul, li, p {
  padding: 0;
  margin: 0;
  list-style: none;
}

.menu {
  width: 100%;
  height: 100vh;
  background-color: #fff;

  &__logo {
    text-align: center;
    padding: 20px;
    margin-bottom: 50px;

    p {
      font-size: 20px;
    }
  }

  &__items {
    display: flex;
    flex-direction: column;
    gap: 30px;
  }

  &__item {
    padding: 10px 0 10px 20px;
    width: 100%;

    &:hover {
      background-color: #F7FBFF;
      .menu__item-name, svg {
        color: #3D82BE;
        fill: #3D82BE;
      }
      line {
        stroke: #3D82BE;
      }
    }
  }

  &__item-link {
    display: flex;
    align-items: center;
    height: 100%;
    gap: 10px;
    text-decoration: none;
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
}
</style>
<template>
  <div>
    <b-navbar toggleable="lg" class="fixed-top">
      <b-container>
        <b-navbar-toggle target="nav-collapse" @click="onHideSearchMobile"></b-navbar-toggle>
        <b-navbar-brand href="#">Logo</b-navbar-brand>
        <div class="icon_search icon_mobile">
          <b-icon icon="search" @click="onShowSearchMobile"></b-icon>
          <div class="input_search input_search_mobile" v-if="showSearchMobile">
            <b-form-input type="text" v-model="search" placeholder="Search..."></b-form-input>
            <div class="icon_close" @click="onHideSearchMobile">
              <b-icon icon="x"></b-icon>
            </div>
          </div>
        </div>
        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav class="ml-auto">
            <b-nav-item href="#" active>Home</b-nav-item>
            <b-nav-item href="#">Discover</b-nav-item>
            <b-nav-item href="#">Register</b-nav-item>
            <div class="icon_search icon_desktop">
              <b-icon icon="search" @click="onShowInput"></b-icon>
            </div>
          </b-navbar-nav>
          <div class="box_search" v-if="showSearch">
            <div class="input_search">
              <b-form-input type="text" v-model="search" placeholder="Search..."></b-form-input>
              <div class="icon_close" @click="onHideInput">
                <b-icon icon="x"></b-icon>
              </div>
            </div>
          </div>
        </b-collapse>
      </b-container>
    </b-navbar>
  </div>
</template>

<script>
export default {
  data() {
    return {
      search: '',
      showSearch: false,
      showSearchMobile: false
    }
  },
  methods:{
    onShowInput(){
      this.showSearch = true
    },
    onHideInput(){
      this.showSearch = false
    },
    onShowSearchMobile(){
      this.showSearchMobile = true
    },
    onHideSearchMobile(){
      this.showSearchMobile = false
    }
  }
}
</script>

<style scoped lang="scss">
  .icon_mobile {
    display: none;
    @media only (max-width : 991px) {
      display: block;
      cursor: pointer;
    }
    svg {
      font-size: 19px;
    }
    .input_search_mobile {
      position: absolute;
      width: 100%;
      left: 0;
      top: 55px;
      input {
        border-radius: 0px;
      }
      .icon_close {
        position: absolute;
        top: 0;
        right: 0;
        height: 100%;
        width: 35px;
        text-align: center;
        background: #dddddd;
        svg {
          font-size: 21px;
          position: relative;
          top: 7px;
        }
      }
    }
  }
  @media only (max-width : 991px) {
    .navbar-toggler {
      border: 0px;
      padding: 0px;
      &:focus {
        outline: 0px;
      }
    }
    .icon_desktop {
      display:none;
    }
  }
  .navbar {
    background: #f7f9f9;
    .navbar-collapse {
      position:relative;
      ul {
        li {
          width: 110px;
          @media only screen and (min-width : 320px) and (max-width : 640px) {
            width: 100%;
            text-align: left;
          }
          a {
            color: #353535;
            font-size: 15px;
            &.active {
              background: #e0e2e2;
              border-radius: 20px;
              @media only screen and (min-width : 320px) and (max-width : 640px) {
                background: transparent;
              }
            }
          }
        }
        .icon_search {
          svg {
            position: relative;
            top: 9px;
            cursor: pointer;
          }
        }
      }
      .box_search {
        position: absolute;
        right: 0;
        width: 370px;
        .input_search {
          position: relative;
          .icon_close {
            position: absolute;
            top: 0px;
            right: 0;
            height: 100%;
            width: 35px;
            cursor: pointer;
            text-align: center;
            background: #dddddd;
            svg {
              position: relative;
              top: 8px;
              font-weight: 600;
              font-size: 18px;
            }
          }
        }
      }
    }
  }
</style>

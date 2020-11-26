<template>
  <div>
    <b-container class="py-5">
      <b-row>
        <b-col col lg="6" class="mx-auto">
          <div class="heading">
            <img class="img-fluid" src="@/assets/img/icon-discover.png" alt="icon discover" />
            <h2>DISCOVER</h2>
            <p>BOOKED TOOL</p>
          </div>
          <div class="tabs_discover">

            <div class="box_tabs">
              <div class="box_img_tabs">
                <div class="tab_img">
                  <img v-if="onShow1" class="img-fluid" src="@/assets/img/discover.png" alt="discover 1" />
                  <img v-if="onShow2" class="img-fluid" src="@/assets/img/banner2.jpg" alt="discover 2" />
                  <img v-if="onShow3" class="img-fluid" src="@/assets/img/discover.png" alt="discover 3" />
                  <img v-if="onShow4" class="img-fluid" src="@/assets/img/banner2.jpg" alt="discover 4" />
                </div>
              </div>
              <div class="menu_tabs">
                <ul>
                  <li>
                    <p id="discover1" class="active" @click="show1">Discover A</p>
                  </li>
                  <li>
                    <p id="discover2" @click="show2">Discover B</p>
                  </li>
                  <li>
                    <p id="discover3" @click="show3">Discover C</p>
                  </li>
                  <li>
                    <p id="discover4" @click="show4">Discover D</p>
                  </li>
                </ul>
              </div>
              <div class="box_content_tabs">
                <div class="content_tabs content_1" v-if="onShow1">
                  <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s to make a type specimen book. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s to make a type specimen book.</p>
                </div>
                <div class="content_tabs content_2" v-if="onShow2">
                  <p>It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged like Aldus PageMaker including versions. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged like Aldus PageMaker including versions.</p>
                </div>
                <div class="content_tabs content_3" v-if="onShow3">
                  <p>It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software  of Lorem Ipsum.It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software  of Lorem Ipsum.</p>
                </div>
                <div class="content_tabs content_4" v-if="onShow4">
                  <p>It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout. The point of using Lorem Ipsum is that it has a more-or-less.It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout. The point of using Lorem Ipsum is that it has a more-or-less.</p>
                </div>
              </div>
            </div>

          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      onShow1: true,
      onShow2: false,
      onShow3: false,
      onShow4: false,
    }
  },
  methods: {
    show1(){
      this.onShow1 = true
      this.onShow2 = false
      this.onShow3 = false
      this.onShow4 = false
      let el1 = document.getElementById("discover1");
      el1.classList.add("active");
      let el2 = document.getElementById("discover2");
      el2.classList.remove("active");
      let el3 = document.getElementById("discover3");
      el3.classList.remove("active");
      let el4 = document.getElementById("discover4");
      el4.classList.remove("active");
    },
    show2(){
      this.onShow1 = false
      this.onShow2 = true
      this.onShow3 = false
      this.onShow4 = false
      let el1 = document.getElementById("discover1");
      el1.classList.remove("active");
      let el2 = document.getElementById("discover2");
      el2.classList.add("active");
      let el3 = document.getElementById("discover3");
      el3.classList.remove("active");
      let el4 = document.getElementById("discover4");
      el4.classList.remove("active");
    },
    show3(){
      this.onShow1 = false
      this.onShow2 = false
      this.onShow3 = true
      this.onShow4 = false
      let el1 = document.getElementById("discover1");
      el1.classList.remove("active");
      let el2 = document.getElementById("discover2");
      el2.classList.remove("active");
      let el3 = document.getElementById("discover3");
      el3.classList.add("active");
      let el4 = document.getElementById("discover4");
      el4.classList.remove("active");
    },
    show4(){
      this.onShow1 = false
      this.onShow2 = false
      this.onShow3 = false
      this.onShow4 = true
      let el1 = document.getElementById("discover1");
      el1.classList.remove("active");
      let el2 = document.getElementById("discover2");
      el2.classList.remove("active");
      let el3 = document.getElementById("discover3");
      el3.classList.remove("active");
      let el4 = document.getElementById("discover4");
      el4.classList.add("active");
    }
  }
}
</script>

<style scoped lang="scss">
  .tabs_discover {
    .box_tabs {
      .box_img_tabs {
        .tab_img {
          margin-bottom: 15px;
          img {
            border-radius: 8px;
          }
        }
      }
      .menu_tabs {
        ul {
          width: 100%;
          padding: 0px;
          display: inline-flex;
          border-bottom: 2px solid #dddddd;
          li {
            float: left;
            width: 100px;
            margin: 0px 8px;
            list-style: none;
            p {
              cursor: pointer;
              margin-bottom: 0px;
              padding-bottom: 5px;
              &.active {
                border-bottom: 4px solid #468fcc;
              }
              @media only screen and (min-width : 320px) and (max-width : 480px) {
                font-size: 13px;
              }
            }
          }
        }
      }
      .box_content_tabs {
        .content_tabs {
          p {
            text-align: left;
            font-size: 14px;
          }
        }
      }
    }
  }
</style>

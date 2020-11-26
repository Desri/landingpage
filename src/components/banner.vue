<template>
  <div>
    <b-container fluid>
      <div class="box_banner">
        <b-row>
          <b-col col-xs="12" sm="6" lg="6" class="p-0">
            <div class="banner_1">
              <div class="bg_img_banner">
                <div class="box_caption_banner">
                  <div class="caption_banner">
                    <h1><strong>Booked Tool</strong> enables you to create Interactive Advertisement</h1>
                    <button>What is it?</button>
                  </div>
                </div>
              </div>
            </div>
          </b-col>
          <b-col col sm="6" lg="6" class="p-0">
            <div class="banner_2">
              <img class="img-fluid" src="@/assets/img/banner2.jpg" alt="Banner 2" />
            </div>
          </b-col>
        </b-row>
      </div>
    </b-container>

    <section id="box_newsletter">
      <b-container>
        <b-row>
          <b-col col sm="12" lg="10" class="mx-auto">
            <b-form inline>
              <p class="mb-2 mr-sm-3 mr-lg-5 mb-sm-0 text-left">Please log in to start using <br><span><strong>Booked Tool</strong></span> </p>
              <b-form-input type="email" v-model="email" class="mb-2 mr-sm-3 mb-sm-0" placeholder="Email"></b-form-input>
              <b-form-input type="password" v-model="password" class="mb-2 mr-sm-3 mb-sm-0" placeholder="Password"></b-form-input>
              <b-button variant="primary">Login</b-button>
            </b-form>
          </b-col>
        </b-row>
      </b-container>
    </section>
    
  </div>
</template>

<script>
export default {
  data() {
    return {
      email: '',
      password: ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .box_banner {
    height: 490px;
    max-height: 490px;
    @media only screen and (min-width : 320px) and (max-width : 640px) {
      height: 390px;
      max-height: 390px;
    }
    .banner_1 {
      position: absolute;
      width: 110%;
      height: 100%;
      @media only screen and (min-width : 320px) and (max-width : 640px) {
        width: 100%;
      }
      .bg_img_banner {
        height: 490px;
        max-height: 490px;
        background-size: cover;
        background-image: url('./../assets/img/banner1.jpg');
        @media only screen and (min-width : 320px) and (max-width : 640px) {
          height: 390px;
          max-height: 390px;
        }
        .box_caption_banner {
          width: 100%;
          position: absolute;
          top: 40%;
          @media only screen and (min-width : 320px) and (max-width : 640px) {
            position: relative;
            top: 62%;
          }
          .caption_banner {
            width: 330px;
            float: right;
            text-align: left;
            padding-right: 80px;
            @media only screen and (min-width : 320px) and (max-width : 640px) {
              width: 100%;
              padding: 15px;
            }
            h1 {
              font-size: 17px;
              @media only screen and (min-width : 320px) and (max-width : 640px) {
                font-size: 19px;
              }
            }
            button {
              width: 95px;
              height: 35px;
              color: #ffffff;
              font-size: 13px;
              border-radius: 5px;
              background: #468fcc;
              border: 1px solid #468fcc;
              &:focus {
                outline: 0px;
              }
            }
          }
        }
      }
    }
    .banner_2 {
      img {
        width: 100%;
        height: 420px;
      }
      @media only screen and (min-width : 320px) and (max-width : 640px) {
        display: none;
      }
    }
  }
  
  #box_newsletter {
    padding: 40px 0px;
    background: #e2e3e4;
    form {
      input {
        height: 40px;
        border-radius: 0px;
        @media only screen and (min-width : 481px) and (max-width : 1040px) {
          width: 215px;
        }
        @media only screen and (min-width : 481px) and (max-width : 992px) {
          width: 191px;
        }
      }
      button {
        width: 95px;
        background: #468fcc;
        @media only screen and (min-width : 320px) and (max-width : 640px) {
          margin-top: 10px;
        }
      }
      p {
        font-size: 14px;
        line-height: 23px;
        @media only screen and (min-width : 320px) and (max-width : 768px) {
          width: 100%;
        }
        span {
          font-size: 24px;
        }
      }
    }
  }
</style>

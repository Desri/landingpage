<template>
  <div>

    <section id="box_contact">
      <b-container>
        <b-row>
          <b-col col lg="8" class="mx-auto">
            <div class="heading">
              <img class="img-fluid" src="@/assets/img/icon-contact.png" alt="icon contact" />
              <h2>Get in touch</h2>
              <p>Want to get in touch? We'd love to here from you. Here's how you can reach us.</p>
            </div>
            <div class="box_search">
              <div class="box_icon_search">
                <b-icon icon="search"></b-icon>
              </div>
              <b-form-input type="text" placeholder="Search..."></b-form-input>
            </div>
            <div class="box_maps">
              <b-row>
                <b-col col-xs="12" sm="6" lg="6" class="p-0">
                  <div class="maps">
                    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3966.620967517708!2d106.82200961402762!3d-6.181458095524855!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e69f42c022144c3%3A0xfe6941ee5d3ab9d8!2sWisma%20Antara%2C%20Jl.%20Medan%20Merdeka%20Sel.%20No.17%2C%20RT.11%2FRW.2%2C%20Gambir%2C%20Kecamatan%20Gambir%2C%20Kota%20Jakarta%20Pusat%2C%20Daerah%20Khusus%20Ibukota%20Jakarta%2010110!5e0!3m2!1sid!2sid!4v1606329472237!5m2!1sid!2sid" height="330" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe>
                  </div>
                </b-col>
                <b-col col-xs="12" sm="6" lg="6" class="p-0">
                  <div class="form_contact">
                    <h3>Feedback</h3>
                    <b-form>
                      <div class="form-row">
                        <div class="form-group col-md-6">
                          <b-form-input type="text" v-model="first" placeholder="First"></b-form-input>
                        </div>
                        <div class="form-group col-md-6">
                          <b-form-input type="text" v-model="last" placeholder="Last"></b-form-input>
                        </div>
                      </div>
                      <div class="form-group">
                        <b-form-input type="email" v-model="email" placeholder="Email"></b-form-input>
                      </div>
                      <div class="form-group">
                        <b-form-textarea v-model="message" placeholder="Message" rows="3"
                        ></b-form-textarea>
                      </div>
                      <button type="submit" class="btn btn-primary">Send</button>
                    </b-form>

                  </div>
                </b-col>
              </b-row>
              
              
            </div>
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
      first: '',
      last: '',
      email: '',
      message: ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  #box_contact {
    padding: 40px 0px;
    background: #f7f9f9;
    .box_search {
      position: relative;
      margin-bottom: 20px;
      .box_icon_search {
        width: 35px;
        position: absolute;
        height: 100%;
        svg {
          position: relative;
          top: 7px;
          font-size: 15px;
        }
      }
      input {
        padding-left: 35px;
      }
    }
    .box_maps {
      .maps {
        iframe {
          width: 100%;
          @media only screen and (min-width : 481px) and (max-width : 768px) {
            height: 384px;
          }
        }
      }
      .form_contact {
        padding: 25px;
        background: #ffffff;
        h3 {
          font-size: 19px;
          text-align: left;
          font-weight: 600;
        }
        form {
          text-align: left;
          button {
            width: 95px;
            background: #468fcc;
          }
        }
      }
    }
    
  }
</style>

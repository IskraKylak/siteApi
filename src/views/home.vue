<template>
  <div class="">
    <section class="section-1">
      <div class="box_slider slider-1">
        <!-- <div class="item">
          <a href="#" class="box_content">
            <div class="box_img">
              <img
                loading="lazy"
                src="@/assets/images/slider-1_img-1.webp"
                alt=""
                width="100%"
                height="auto"
              />
            </div>
            <div class="box_text">
              <div class="box_title">
                <h1 class="text-h1">
                  ВСЕУКРАЇНСЬКА АСОЦІАЦІЯ <br />БЕЗПЕРЕРВНОЇ ПРОФЕСІЙНОЇ ОСВІТИ
                  <br />ЛІКАРІВ ТА ФАРМАЦЕВТІВ
                </h1>
              </div>
            </div>
          </a>
        </div> -->
        <div class="item">
          <a href="#" class="box_content">
            <div class="box_img">
              <img
                v-if="info"
                loading="lazy"
                :src="info.banner1"
                alt=""
                width="100%"
                height="auto"
              />
            </div>
            <div class="box_text">
              <div class="box_title">
                <h1 class="text-h1">
                  ВСЕУКРАЇНСЬКА АСОЦІАЦІЯ <br />БЕЗПЕРЕРВНОЇ ПРОФЕСІЙНОЇ ОСВІТИ
                  <br />ЛІКАРІВ ТА ФАРМАЦЕВТІВ
                </h1>
              </div>
            </div>
          </a>
        </div>
        <div class="item">
          <a href="#" class="box_content">
            <div class="box_img">
              <img
                v-if="info"
                loading="lazy"
                :src="info.banner2"
                alt=""
                width="100%"
                height="auto"
              />
            </div>
            <div class="box_text">
              <div class="box_title">
                <h1 class="text-h1">
                  ВСЕУКРАЇНСЬКА АСОЦІАЦІЯ <br />БЕЗПЕРЕРВНОЇ ПРОФЕСІЙНОЇ ОСВІТИ
                  <br />ЛІКАРІВ ТА ФАРМАЦЕВТІВ
                </h1>
              </div>
            </div>
          </a>
        </div>
      </div>
    </section>
    <section class="section-2" v-if="info">
      <div class="box_content">
        <div class="box_left">
          <img
            width="100%"
            height="auto"
            loading="lazy"
            class="img_bg"
            :src="info.banner3"
            alt=""
          />
          <div class="box_link">
            <img
              width="225px"
              height="166px"
              loading="lazy"
              src="@/assets/images/sct-2_img-1.webp"
              alt=""
            />
            <a class="link_gallary" href="#">
              <svg
                class="mdi-icon"
                width="36"
                height="36"
                fill="currentColor"
                viewBox="0 0 24 24"
              >
                <path
                  d="M15.41,16.58L10.83,12L15.41,7.41L14,6L8,12L14,18L15.41,16.58Z"
                ></path>
              </svg>
              Галерея</a
            >
          </div>
        </div>
        <div class="box_right">
          <div class="box_inner">
            <div class="box_top">
              <h2 data-aos="fade-left">{{ info.title2 }}</h2>
              <p>
                {{ info.description2 }}
              </p>
            </div>
            <div class="box_bottom">
              <h2 data-aos="fade-left">{{ info.title3 }}</h2>
              <p class="p-1">
                {{ info.description3 }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="section-3" v-if="info">
      <div class="box_content container">
        <div class="box box-1">
          <h2 class="text-h2" data-aos="fade-right">{{ info.title4 }}</h2>
          <p>
            {{ description4[0] }}
          </p>
        </div>
        <div class="box box-2">
          <div class="box_mini box_mini-1">
            <div class="box_number">
              <p data-aos="zoom-in">
                {{ description4[1] }}
              </p>
            </div>
            <div class="box_text">
              <h3>
                {{ description4[2] }}
              </h3>
              <p>
                {{ description4[3] }}
              </p>
            </div>
          </div>
          <div class="box_mini box_mini-2">
            <div class="box_number">
              <p data-aos="zoom-in" data-aos-delay="300">
                {{ description4[4] }}
              </p>
            </div>
            <div class="box_text">
              <h3>{{ description4[5] }}</h3>
              <p>
                {{ description4[6] }}
              </p>
            </div>
          </div>
          <div class="box_mini box_mini-3">
            <div class="box_number">
              <p data-aos="zoom-in" data-aos-delay="600">
                {{ description4[7] }}
              </p>
            </div>
            <div class="box_text">
              <h3>{{ description4[8] }}</h3>
              <p>
                {{ description4[9] }}
              </p>
            </div>
          </div>
        </div>
        <div class="box-3">
          <h2>{{ info.title5 }}</h2>
          <p>
            {{ info.description5 }}
          </p>
          <div class="box_for_btn">
            <a :href="info.form" class="link" target="_blank">
              <span class="title">{{ info.form_name }}</span>
              <div class="line line-1"></div>
              <div class="line line-2"></div>
              <div class="line line-3"></div>
              <div class="line line-4"></div>
            </a>
          </div>
        </div>
      </div>
    </section>
    <section class="doctor container" v-if="info">
      <div class="doctor-row_info">
        <div class="doctor-row_info_desc">
          <div class="doctor-row_info_desc_wrapper">
            <div class="doctor-row_info_desc_label">
              {{ info.title6 }}
            </div>
            <div class="doctor-row_info_desc_text">
              {{ info.description6 }}
            </div>
          </div>
        </div>
        <div class="doctor-row_info_quantity">
          <div class="doctor-row_info_quantity_content">
            {{ info.title7 }}
          </div>
          <div class="Count">
            <span class="Count2">{{ String(info.counter)[0] }} </span>
            <span class="Count2">{{ String(info.counter)[1] }} </span>
            <span class="Count2">{{ String(info.counter)[2] }} </span>
            <!-- <span class="Count1">{{ counter[1] }}</span>
            <span class="Count1">{{ counter[2] }}</span> -->
          </div>
        </div>
      </div>
      <div class="doctor-row_info_bottom">
        <div class="doctor-row_info_bottom_content">
          {{ info.title8 }}
        </div>
      </div>
      <div class="wrap_btns_pdf">
        <a
          :href="info.manual"
          class="doctor-row_info_bottom_btn_wrapper"
          target="_blank"
        >
          {{ info.manual_title }}
        </a>
        <a
          :href="info.statement"
          class="doctor-row_info_bottom_btn_wrapper"
          target="_blank"
        >
          {{ info.statement_title }}
        </a>
        <a
          :href="info.bill"
          class="doctor-row_info_bottom_btn_wrapper"
          target="_blank"
        >
          {{ info.bill_title }}
        </a>
      </div>
    </section>
    <section class="section-4" v-if="info">
      <div class="box_content">
        <div class="box_mini box_mini-1">
          <a href="#" class="box_img">
            <img
              width="150px"
              height="150px"
              loading="lazy"
              :src="info.first_logo"
              alt=""
              data-aos="zoom-in"
            />
          </a>
        </div>
        <div class="box_mini box_mini-2">
          <a href="#" class="box_img">
            <img
              width="401px"
              height="93px"
              loading="lazy"
              :src="info.second_logo"
              alt=""
              data-aos="zoom-in"
              data-aos-delay="300"
            />
          </a>
        </div>
        <!-- <div class="box_mini box_mini-3">
          <a href="#" class="box_img">
            <img
              width="240px"
              height="158px"
              loading="lazy"
              src="../images/sct-4_logo-3.webp"
              alt=""
              data-aos="zoom-in"
              data-aos-delay="600"
            />
          </a>
        </div> -->
      </div>
    </section>
  </div>
</template>

<script>
import { mapActions } from "vuex";
export default {
  data() {
    return {};
  },
  methods: {
    ...mapActions(["GET_INFO_FROM_API"]),
  },
  mounted() {
    this.GET_INFO_FROM_API();
    $(function () {
      AOS.init({ disable: "mobile" });
      $(".slider-1").slick({
        dots: true,
      });
    });
  },
  computed: {
    info() {
      return this.$store.getters.getInfoApi;
    },
    description4() {
      return String(this.$store.getters.getInfoApi.description4).split("\r\n");
    },
    counter() {
      return String(this.$store.getters.getInfoApi.counter);
    },
  },
};

import AOS from "aos";
import "@/assets/js/slick.min.js";
var block_show = false;

function scrollTracking() {
  if (block_show) {
    return false;
  }

  var wt = $(window).scrollTop();
  var wh = $(window).height();
  if ($(".Count").length) {
    var et = $(".Count").offset().top;
  }
  var eh = $(".Count").outerHeight();
  var dh = $(document).height();

  if (wt + wh >= et || wh + wt == dh || eh + et < wh) {
    block_show = true;

    $(".Count").css("opacity", "1");
    $(".Count1").each(function () {
      var $this = $(this);
      $({ Counter: 0 }).animate(
        { Counter: $this.text() },
        {
          duration: 1000,
          easing: "swing",
          step: function () {
            $this.text(Math.ceil(this.Counter));
          },
        }
      );
    });
  }
}

$(window).scroll(function () {
  scrollTracking();
});

$(function () {
  scrollTracking();

  $(window).scroll(function () {
    if ($(this).scrollTop() != 0) {
      $("#toTop").fadeIn();
    } else {
      $("#toTop").fadeOut();
    }
  });

  $("#toTop").click(function () {
    $("body,html").animate({ scrollTop: 0 }, 800);
  });

  $(window).scroll(function () {
    if ($(this).scrollTop() > 0) {
      $(".main-header").addClass("header-scroll");
      $(".main_page").addClass("active");
    } else {
      $(".main-header").removeClass("header-scroll");
      $(".main_page").removeClass("active");
    }
  });
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.doctor-row_info {
  display: flex;
  justify-content: space-between;
}

@media screen and (max-width: 1070px) {
  .doctor-row_info {
    flex-direction: column;
  }

  .doctor-row_info_quantity {
    margin: 60px 0;
  }
}

.doctor-row_info_desc_label,
.doctor-row_info_quantity_content,
.doctor-row_info_bottom_content {
  font-weight: 600;
  font-size: 32px;
  color: var(--main-color);
  position: relative;
  display: inline-block;
  text-transform: uppercase;
  padding-top: 18px;
  margin-bottom: 22px;
}

.doctor-row_info_desc_wrapper {
  max-width: 662px;
}

.doctor-row_info_desc_label:before,
.doctor-row_info_quantity_content:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 52%;
  height: 2px;
  background: #002678;
}

.doctor-row_info_quantity_content {
  max-width: 300px;
}

.doctor-row_info_bottom_btn_wrapper {
  height: 44px;
  max-width: 264px;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  color: #fa5c18;
  border: 2px solid #fa5c18;
  box-sizing: border-box;
  transition: all 0.3s ease;
}

.doctor-row_info_bottom_btn_wrapper:hover {
  background: #fa5c18;
  color: #fff;
}

.wrap_btns_pdf {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  max-width: 850px;
  margin-top: 50px;
}

@media screen and (max-width: 900px) {
  .wrap_btns_pdf {
    display: block;
  }

  .doctor-row_info_bottom_btn_wrapper {
    margin-bottom: 10px;
  }
}

.doctor.container {
  padding: 85px 15px;
}

.Count {
  opacity: 0;
  transition: all 0.3s ease;
}

.Count span {
  display: inline-block;
  background-color: #002678;
  border-radius: 4px;
  color: #fff;
  max-width: 50px;
  height: 57px;
  line-height: 50px;
  font-size: 49px;
  margin-right: 3px;
  padding: 5px 10px;
}
</style>

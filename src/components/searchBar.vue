<template>
  <div>
    <div class="search-bar d-flex justify-content-between">
      <div class="input-wrapper">
        <input type="text" placeholder="Search" />
        <svg
          class="icon-search"
          width="14"
          height="14"
          viewBox="0 0 14 14"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M11.2028 9.85174C11.1006 9.74954 11.0866 9.57314 11.165 9.45134C11.781 8.50354 12.1422 7.37514 12.1422 6.16274C12.1422 2.81394 9.4178 0.0909424 6.0718 0.0909424C2.723 0.0909424 0 2.81394 0 6.16274C0 9.51014 2.723 12.2331 6.0718 12.2331C7.3752 12.2331 8.582 11.8145 9.5732 11.1117C9.6894 11.0277 9.8644 11.0389 9.9666 11.1397L12.1366 13.3097C12.1506 13.3237 12.166 13.3377 12.1814 13.3489C12.2066 13.3699 12.3116 13.4679 12.4124 13.5701L12.67 13.8263C12.7722 13.9271 12.9374 13.9271 13.0382 13.8263L13.923 12.9415C14.0252 12.8393 14.0252 12.6741 13.9244 12.5719L11.2028 9.85174ZM9.744 8.99074C9.5438 9.25114 9.3184 9.48914 9.0692 9.70054C8.26 10.3879 7.2142 10.8051 6.0718 10.8051C3.5112 10.8051 1.428 8.72194 1.428 6.16274C1.428 3.60354 3.5112 1.51894 6.0718 1.51894C8.631 1.51894 10.7142 3.60214 10.7142 6.16274C10.7142 7.22674 10.3488 8.20674 9.744 8.99074Z"
            fill="#CACCCF"
          />
        </svg>
      </div>
      <div class="awatar d-flex align-items-center">
        <b-avatar class="avatar-notif" badge badge-top badge-offset="-2px">
          <svg
            width="22"
            height="22"
            viewBox="0 0 22 22"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M19.2223 17.3815C19.1479 17.2135 19.1311 16.9687 19.1935 16.7959C19.6759 15.4279 20.1703 14.0671 20.6839 12.7087C21.2311 11.2663 21.6559 9.8143 21.4423 8.2375C21.1999 6.4471 20.4655 4.8967 19.1431 3.6727C18.4975 3.0775 17.7415 2.6095 16.9927 2.0527C17.0503 1.8943 17.1439 1.6471 17.2351 1.3999C17.3839 0.991901 17.2687 0.672701 16.9255 0.545501C16.5727 0.415901 16.2775 0.562301 16.1119 0.958301C16.0039 1.2127 15.9079 1.4695 15.8023 1.7335C14.8039 1.4887 13.8175 1.3903 12.8167 1.5343C9.8335 1.9615 7.6807 3.5263 6.5167 6.3175C5.8039 8.0335 5.2159 9.8023 4.5823 11.5495C4.5055 11.7655 4.3831 11.8927 4.1743 11.9863C3.1135 12.4615 2.0599 12.9511 0.999097 13.4335C0.715897 13.5607 0.504697 13.7407 0.511897 14.0767C0.519097 14.4247 0.763897 14.5639 1.0519 14.6671C3.0319 15.3775 5.0071 16.0951 6.9919 16.7911C7.2895 16.8967 7.3927 17.0143 7.3759 17.3431C7.2751 19.5463 9.3415 21.1879 11.4799 20.6287C12.3463 20.4031 13.0063 19.8967 13.5031 19.1431C13.6063 19.1791 13.6999 19.2127 13.7935 19.2439C15.8047 19.9639 17.8159 20.6839 19.8271 21.4087C20.1295 21.5167 20.4079 21.5623 20.6575 21.3055C20.9167 21.0367 20.8087 20.7607 20.6743 20.4775C20.1799 19.4527 19.6879 18.4231 19.2223 17.3815ZM10.1191 19.4599C9.1615 19.1839 8.5279 18.3247 8.5951 17.3455C9.8479 17.7919 11.0743 18.2311 12.3055 18.6703C11.9551 19.3423 10.9495 19.6999 10.1191 19.4599Z"
              fill="#CACCCF"
            />
          </svg>
          <span class="number-notification">9</span>
        </b-avatar>
        <div class="avatar-img">
          <img src="../assets/images/img-avatar.png" alt="" />
        </div>
      </div>
    </div>

    <div class="row">
      <div class="col-md-3" v-for="(element, index) in card" :key="index">
        <div class="area-card">
          <div class="card-item d-flex align-items-center">
            <div>
              <img :src="element.img" alt="" />
            </div>
            <div>
              <h4 class="title">{{ element.title }}</h4>
              <p class="title-number">{{ element.titleNumber }}</p>
            </div>
          </div>
        </div>
      </div>
      <!-- <pre>{{card}}</pre> -->
    </div>
  </div>
</template>
<script>
export default {
  name: "searchBar",
  props: {
    card: {
      type: Object,
      default: () => {
        [];
      },
    },
  },
};
</script>
<style lang="scss" scoped>
.search-bar {
  .input-wrapper {
    position: relative;
    input {
      background: #ffffff;
      border-radius: 100px;
      font-family: Lato;
      font-size: 13px;
      line-height: 16px;
      letter-spacing: 0.1px;
      padding: 12px 16px 12px 42px;
      width: 350px;
      border: 1px solid #f6f8fb;
      outline: none;
    }
    .icon-search {
      position: absolute;
      top: 15px;
      left: 16px;
    }
  }
  .awatar {
    .avatar-img {
      border: 3px solid #e8e8e8;
      border-radius: 50%;
      margin-left: 16px;
    }
    .avatar-notif {
      position: relative;
      .number-notification {
        position: absolute;
        top: 5px;
        right: 0;
        border-radius: 50%;
        background: #ff6760;
        border: 2px solid #f6f8fb;
        width: 16px;
        height: 16px;
        font-family: Lato;
        font-weight: bold;
        font-size: 10px;
        line-height: 12px;
        text-align: center;
        letter-spacing: 0.2px;
        color: #ffffff;
      }
    }
  }
}
.area-card {
  margin: 30px 0;
  cursor: pointer;
  .card-item {
    padding: 24px;
    background: #ffffff;
    box-shadow: 0px 12px 26px rgba(16, 30, 115, 0.06);
    border-radius: 8px;
    img{
      margin-right: 24px;
    }
    .title {
      font-family: Lato;
      font-weight: bold;
      font-size: 14px;
      line-height: 20px;
      letter-spacing: 0.1px;
      color: #25282b;
      margin-bottom: 4px;
    }
    .title-number {
      font-family: Lato;
      font-size: 18px;
      line-height: 24px;
      letter-spacing: 0.1px;
      color: #336cfb;
      margin: 0;
    }
  }
}
</style>

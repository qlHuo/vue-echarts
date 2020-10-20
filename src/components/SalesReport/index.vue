<template>
  <div class="sale-reports">
    <div class="header">
      电商商品销售趋势图
    </div>
    <div class="content">
      <div class="content-title-wrapper">月销售增长率</div>
      <div class="content-index-wrapper">
        <span class="arrow-up">
          <svg data-v-666af9e5="" aria-hidden="true" focusable="false" data-prefix="fas" data-icon="angle-up" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512" class="svg-inline--fa fa-angle-up fa-w-10"><path data-v-666af9e5="" fill="currentColor" d="M177 159.7l136 136c9.4 9.4 9.4 24.6 0 33.9l-22.6 22.6c-9.4 9.4-24.6 9.4-33.9 0L160 255.9l-96.4 96.4c-9.4 9.4-24.6 9.4-33.9 0L7 329.7c-9.4-9.4-9.4-24.6 0-33.9l136-136c9.4-9.5 24.6-9.5 34-.1z"></path></svg>
        </span>
        <span class="percentage">34<span>%</span></span>
        <span class="text">+14,400</span>
      </div>
      <div id="content-chart"></div>
      <div class="content-circle-wrapper">
        <div 
        :class="['circle', selectedIndex === index ? 'selected' : '']" 
        v-for='(item, index) in circle' 
        :key="index"
        @click="change(index)"
        ></div>
      </div>
      <div class="content-bottom-wrapper">销售趋势</div>
    </div>
    <div class="footer"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      circle: new Array(3),
      selectedIndex: 0
    }
  },
  methods: {
    change(index) {
      this.selectedIndex = index
    }
  }
}
</script>

<style lang="scss" scoped>
.sale-reports {
  display: flex;
  flex-direction: column;
  width: 100%;
  height: 100%;
  background-color: #fff;
  box-shadow: 0 2px 8px rgba(4, 5, 9, .7);
  .header {
    width: 100%;
    height: 50px;
    border-bottom: 1px solid #ccc;
    box-sizing: border-box;
    line-height: 50px;
    padding-left: 20px;
  }
  .content {
    display: flex;
    flex-direction: column;
    padding: 28px;
    flex: 1;
    width: 100%;
    box-sizing: border-box;
    .content-title-wrapper {
      padding-bottom: 10px;
    }
    .content-index-wrapper {
      display: flex;
      align-items: center;
      .arrow-up {
        svg {
          width: 25px;
          color: #3ac47d;
        }
      }
      .percentage {
        padding: 0 10px;
        font-size: 28px;
        font-weight: 700;
        span {
          font-size: 24px;
          font-weight: 400;
          color: #999;  
        }
      }
      .text {
        font-size: 16px;
        color: #3ac47d;
      }
    }
    #content-chart {
      flex: 1;
      width: 100%;
    }
    .content-circle-wrapper {
      display: flex;
      justify-content: center;
      align-items: center;
      .circle {
        width: 10px;
        height: 10px;
        border: 2px solid #3f6ad8;
        border-radius: 50%;
        margin: 0 5px;
        &.selected {
          width: 12px;
          height: 12px;
          border: 3px solid #3f6ad8;
        }
      }
    }
    .content-bottom-wrapper {
      height: 28px;
      line-height: 28px;
      color: #999;
    }
  }
  .footer {
    width: 100%;
    height: 120px;
    border-top: 1px solid #ccc;
    box-sizing: border-box;
    // background-color: blue;
  }

}
  
</style>
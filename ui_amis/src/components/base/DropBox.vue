<template>
  <div>
    <div class="drop-box">
      <span>Thực hiện hàng loạt</span>
      <div
        class="icon-16 dropdown-while"
        v-on:click="isShow = !isShow"
      ></div>
    </div>
    <div class="multi-delete" v-if="isShow" @click="multiDelete">
      <p>Xoá</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isShow: false,
    };
  },
  methods: {

    /**
     * Thuc hien xoa
     */
    multiDelete(){
      this.$emit('multiDelete')
      this.isShow = false
    }
  },
  
};
</script>

<style>
.drop-box {
  position: relative;
  width: 180px;
  height: 36px;
  background-color: #ffffff;
  box-sizing: border-box;
  display: flex;
  align-items: center;
  border-radius: 20px;
  border: 2px solid #3b3c3f;
  cursor: pointer;
}
.drop-box:hover {
  background-color: #d2d3d6;
}
.drop-box span {
  padding: 4px 4px 4px 16px;
  font-family:  Notosans-Regular;
  font-size: 13px;
  text-align: center;
  font-weight: 600;
}
.multi-delete {
  position: absolute;
  top: 146px; 
  left: 103px;
  height: 34px;
  width: 104px;
  display: flex;
  align-items: center;
  background-color: #ffffff;
  border: 1px solid #babec5;
  z-index: 999;
  cursor: pointer;
}
.multi-delete p {
  font-size: 13px;
  text-decoration: none solid rgb(17, 17, 17);
  text-align: left;
  padding: 5px 10px 5px 10px;
}
.multi-delete:hover {
  background-color: #e8e9ec;
}
.icon-16 {
  height: 16px;
  width: 16px;
  min-width: 16px;
  min-height: 16px;
  
}
</style>
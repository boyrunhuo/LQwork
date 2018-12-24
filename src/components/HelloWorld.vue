<template>
  <div id="homepage">
    <div class="select-warp">
      <el-select v-model="type" placeholder="请选择类型" style="margin-right: 100px;">
        <el-option v-for="item in typeList" :key="item.key" :value="item.key" :label="item.value">
        </el-option>
        </el-select>
         <el-date-picker
      v-model="date"
      align="right"
      type="date"
      placeholder="选择日期"
      >
    </el-date-picker>
    </div>
    <div class="main-warp">
 <el-table
    :data="tableData"
    border
    style="width: 100%">
     <el-table-column
      fixed
      prop="order"
      label="序号"
      width="80">
    </el-table-column>
    <el-table-column
      fixed
      prop="type"
      label="类型"
     >
    </el-table-column>
    <el-table-column
      fixed
      prop="date"
      label="日期"
      >
    </el-table-column>
    <el-table-column
      prop="name"
      label="姓名"
      >
    </el-table-column>
    <el-table-column
      prop="province"
      label="省份"
      >
    </el-table-column>
    <el-table-column
      prop="city"
      label="市区"
      >
    </el-table-column>
    <el-table-column
      prop="address"
      label="地址"
      >
    </el-table-column>
    <el-table-column
      prop="zip"
      label="邮编"
      >
    </el-table-column>
    <el-table-column
      fixed="right"
      label="操作"
      >
      <template slot-scope="scope">
        <el-button type="text" size="small">查看</el-button>
      </template>
    </el-table-column>
  </el-table>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      type: '',
      date: '',
      typeList: [
        {key: 'common', value: '普通类型'},
        {key: 'special', value: '特殊类型'}
      ],
      tableData: [{
        type: '普通类型',
        order: '1',
        date: '2018-05-03',
        name: '王小虎',
        province: '广东',
        city: '广州市',
        address: '番禺区大学城',
        zip: 200333
      }, {
        type: '普通类型',
        order: '2',
        date: '2018-05-02',
        name: '王小虎',
        province: '广州市',
        city: '番禺区',
        address: '番禺区大学城',
        zip: 200333
      }, {
        type: '普通类型',
        order: '3',
        date: '2018-05-04',
        name: '王小虎',
        province: '广州市',
        city: '番禺区',
        address: '番禺区大学城',
        zip: 200333
      }, {
        type: '普通类型',
        order: '4',
        date: '2018-05-01',
        name: '王小虎',
        province: '广东',
        city: '广州市',
        address: '番禺区大学城',
        zip: 200333
      },
      {
        type: '普通类型',
        order: '5',
        date: '2018-05-03',
        name: '王小虎',
        province: '广东',
        city: '广州市',
        address: '番禺区大学城',
        zip: 200333
      }, {
        type: '普通类型',
        order: '6',
        date: '2018-05-02',
        name: '王小虎',
        province: '广东',
        city: '广州市',
        address: '番禺区大学城',
        zip: 200333
      }, {
        type: '普通类型',
        order: '7',
        date: '2018-05-04',
        name: '王小虎',
        province: '广东',
        city: '广州市',
        address: '番禺区大学城',
        zip: 200333
      }, {
        type: '特殊类型',
        order: '8',
        date: '2018-05-01',
        name: '刘群',
        province: '广东',
        city: '广州市',
        address: '番禺区大学城',
        zip: 200333
      }]
    }
  }
}
</script>

<style>
#homepage {
  width: 1200px;
  position: absolute;
  left: 50%;
  transform: translateX(-50%)
}
.select-warp {
  margin-bottom: 40px;
  display: flex;
  justify-content: flex-start;
}
</style>

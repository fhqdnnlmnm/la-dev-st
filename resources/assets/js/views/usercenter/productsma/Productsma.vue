<template>
    <div>
        <el-table
        :data="tableData"
        :stripe="use"
        style="width: 100%">
        <el-table-column
          prop="date"
          label="日期"
          width="180">
        </el-table-column>
        <el-table-column
          prop="name"
          label="姓名"
          width="180">
        </el-table-column>
        <el-table-column
          prop="address"
          label="地址">
        </el-table-column>
      </el-table>
      中文名称
      英文名称
      国家
      海关编码
      税率(%)
      单价 (USD)
      材质
      材质比例
      用途
      品牌
      厂家
      厂家地址
      操作
    </div>
</template>
<script>
import ProductsmaJS from './Productsma.js';
export default ProductsmaJS
</script>

<style scoped>

</style>
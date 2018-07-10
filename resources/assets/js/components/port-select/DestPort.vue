<template>
<el-col :span="Number(col)">
  <el-tag>{{label}}</el-tag>
  <el-select :value="value" @input="$emit('input',$event)" :placeholder="placeholder">
    <el-option-group
      v-for="group in options"
      :key="group.label"
      :label="group.label">
      <el-option
        v-for="item in group.options"
        :key="item.value"
        :label="item.label"
        :value="item.value">
      </el-option>
    </el-option-group>
  </el-select>
</el-col>
</template>

<script>
  export default {
    name:'dest-port',
    props:['value','options','placeholder','col','label'],
    data() {
      return {
        
      }
    }
  }
</script>
<template>
    <el-col :span="Number(col)">
        <el-tag>{{label}}</el-tag>
        <el-select  
            :value="value"
            @input="$emit('input',$event)"
            :placeholder="placeholder"
            filterable
            remote
            reserve-keyword
            :remote-method="remoteMethod"
            :loading="loading">
            <el-option
                v-for="item in options"
                :key="item.value"
                :label="item.label"
                :value="item.value">
            </el-option>
        </el-select>
    </el-col>
</template>

<script>
import OriginPortJs from './OriginPort.js'
export default OriginPortJs
</script>


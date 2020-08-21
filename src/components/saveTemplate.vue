<template>
  <div class="table_template">
    <div class="menu_item" v-if="tableShow" style="text-align: center;">
      <el-row>
        <el-col :span="21">
          <el-table :data="templateList" border fit highlight-current-row>
            <el-table-column :label="'品牌'" align="center" fixed>
              <template slot-scope="scope">
                <span>{{scope.row.Brand}}</span>
              </template>
            </el-table-column>

            <el-table-column :label="'型号'" width="200px" align="center">
              <template slot-scope="scope">
                <span>{{scope.row.Spec}}</span>
              </template>
            </el-table-column>

            <el-table-column :label="'毛重'" align="center">
              <template slot-scope="scope">
                <span>{{scope.row.GrossWeight}}</span>
              </template>
            </el-table-column>
            <el-table-column :label="'净重'" align="center">
              <template slot-scope="scope">
                <span>{{scope.row.NetWeight }}</span>
              </template>
            </el-table-column>

            <el-table-column :label="'箱数'" align="center">
              <template slot-scope="scope">
                <span>{{scope.row.NumberOfCases}}</span>
              </template>
            </el-table-column>
            <el-table-column :label="'产地'" width="150px" align="center">
              <template slot-scope="scope">
                <span>{{scope.row.Origin}}</span>
              </template>
            </el-table-column>
            <el-table-column :label="'客户料号'" width="200px" align="center">
              <template slot-scope="scope">
                <span>{{scope.row.PartNo}}</span>
              </template>
            </el-table-column>
            <el-table-column :label="'单价'" align="center">
              <template slot-scope="scope">
                <span>{{scope.row.Price}}</span>
              </template>
            </el-table-column>
            <el-table-column :label="'品名'" align="center">
              <template slot-scope="scope">
                <span>{{scope.row.ProductName}}</span>
              </template>
            </el-table-column>
            <el-table-column :label="'数量'" align="center" fixed="right">
              <template slot-scope="scope">
                <span>{{scope.row.Quantity}}</span>
              </template>
            </el-table-column>
          </el-table>
        </el-col>
        <el-col :span="3">
          <el-button type="primary">导出</el-button>
        </el-col>
      </el-row>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    templateList: Array,
    tableShow: Boolean,
  },
  data() {
    return {};
  },
};
</script>


<style>
.menu_item .el-table td,
.menu_item .el-table th {
  padding: 5px 0 !important;
}
.menu_item .el-row {
  padding: 50px 10px 50px 20px;
}
.menu_item .el-button {
  padding: 8px 15px;
}

.menu_item .el-table__empty-block {
  background: #404040;
}
</style>
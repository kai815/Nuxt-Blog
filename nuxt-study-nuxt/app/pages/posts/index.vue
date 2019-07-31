<template>
  <section class="container posts-page">
    <el-card>
      <div slot="header" class="clearfix">
        <span>新規投稿</span>
      </div>
      <el-table 
        :data="showPosts"
        style="width: 100%"
        class="table"
      >
        <el-table-column
          prop="title"
          label="タイトル">
        </el-table-column>
        <el-table-column
          prop="user.id"
          label="投稿者"
          width="180">
        </el-table-column>
        <el-table-column
          prop="created_at"
          label="投稿日時"
          wdidth="240">
        </el-table-column>
      </el-table>
    </el-card>
  </section>
</template>
<script>
export default {
    computed: {
        showPosts(){
            return [
                {
                    id: '001',
                    title: 'Nuxt1',
                    body: 'Nuxt1 body',
                    created_at: '2019/07/28 19:00',
                    user: {
                        id: "hideo"
                    }
                },
                                {
                    id: '002',
                    title: 'Nuxt2',
                    body: 'Nuxt2 body',
                    created_at: '2019/07/28 19:30',
                    user: {
                        id: "kaizuka"
                    }
                },
            ]
        }
    }

}
</script>
<style>
.posts-page .el-table__row {
    cursor: pointer;
}
</style
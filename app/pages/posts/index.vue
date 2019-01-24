<template>
  <section class="container posts-page">
    <el-card style="flex: 1">
      <div slot="header" class="clearfix">
        <span>新着投稿</span>
      </div>
      <el-table :data="showPosts" style="width: 100%" class="table">
        <el-table-column prop="title" label="タイトル"></el-table-column>
        <el-table-column prop="user.id" label="投稿者" width="180"></el-table-column>
        <el-table-column prop="created_at" label="投稿日時" width="240"></el-table-column>
      </el-table>
    </el-card>
  </section>
</template>

<script>
export default {
  computed: {
    showPosts() {
      return [
        {
          id: "001",
          title: "How to development Nuxt.js Application",
          body: "texttexttexttexttexttexttexttexttexttexttexttext...",
          created_at: "2018/08/10 13:00:00",
          user: {
            id: "testman"
          }
        },
        {
          id: "002",
          title: "Development Nuxt.js Application to Heroku",
          body: "texttexttexttexttexttexttexttexttexttexttexttext...",
          created_at: "2018/08/10 13:00:00",
          user: {
            id: "testman"
          }
        }
      ];
    }
  }
};
</script>

<style>
.posts-page .el-table__row {
  cursor: pointer;
}
</style>

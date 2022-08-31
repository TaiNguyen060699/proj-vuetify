<template>
  <nav>
    <v-toolbar flat app>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title class="text-uppercase grey--text">
        <span>Todo</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn flat color="grey">
        <span>Sign Out</span>
        <v-icon right>exit_to_app</v-icon>
      </v-btn>
    </v-toolbar>

    <v-navigation-drawer v-model="drawer" app class="primary">
      <v-list>
        <v-list-item-title v-for="item in lists" :key="item.text" router :to="item.route">
          <v-list-item-icon>
            <v-icon x-large>{{ item.icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item>
            <v-list-item-title>{{ item.text }}</v-list-item-title>
          </v-list-item>
        </v-list-item-title>
      </v-list>
    </v-navigation-drawer>
  </nav>
  <!-- <div>
    <div class="wrapper">
        <img src="https://i.picsum.photos/id/103/235/176.jpg?hmac=5BhdgE_XvV40UjfC6fP3S-5zBQAc0lFjAMmUn4i1VyQ" alt="">
        <div class="inner">
          <p class="title">Cách chọn xe phù hợp với dáng người cho nam có thể bạn chưa biết.</p>
          <p class="content">Theo bạn, tại sao pháp luật lại quy định cần có bảo hiểm bắt buộc xe máy?</p>
          <div class="tag">
            <span>Xe & Đời Sống</span>
            <span>28.08.2022</span>
          </div>
        </div>
    </div>
  </div> -->
</template>

<script>

export default {
  name: 'HelloWorld',

  data: () => ({
    drawer: false,
    lists: [
      { icon: 'mdi-home', text: 'Dashboard', route: '/' },
      { icon: 'mdi-folder', text: 'My Projects', route: '/projects' },
      { icon: 'mdi-flag', text: 'Conversions', route: 'conversions' },
    ]
  }),
}
</script>

<style lang="css" scoped>
  .v-list-item-title {
  }
</style>

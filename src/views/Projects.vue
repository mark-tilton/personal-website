<template>
  <div>
    <ul>
      <li>
        <Project
          projectName="This website"
          link="https://github.com/mark-tilton/personal-website"
          description="A website made to highlight some of my personal projects."
          img="vue_logo.png"
        />
        <Project
          projectName="Quoridor"
          link="https://github.com/mark-tilton/quoridor"
          description="An implementation of the board game Quoridor in C++. 
          Two AI compete to get to the other side by either moving, or
          placing walls. Algorigthms used are Minimax and Monte Carlo Tree Search (MCTS)"
          img="quoridor_img.png"
        />
      </li>
    </ul>
  </div>
</template>

<script>
import Project from "@/components/Project.vue";

export default {
  name: "Projects",
  components: {
    Project
  }
};
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
}
a {
  color: #42b983;
}
</style>

<template>
  <div id="Card">
    <img id="thumbnail" :src="require(`../assets/${img}`)" />
    <h3 id="header">
      <a :href="link">{{ projectName }}</a>
    </h3>
    <p id="description">{{ description }}</p>
  </div>
</template>

<script>
export default {
  name: "project",
  props: {
    projectName: String,
    link: String,
    description: String,
    img: String
  }
};
</script>

<style scoped>
#Card {
  padding: 0px;
  margin: 10px 5px;
  display: grid;
  grid-template-rows: auto 100%;
  grid-template-columns: 128px auto;
  border: 1px;
  border-color: #2a3536;
  border-style: solid;
  border-radius: 10px;
}

#header {
  margin: 5px 10px;
  font-weight: bold;
  color: #dae4ee;
  justify-self: left;
  grid-row: 1 / 2;
  grid-column: 2 / 3;
  height: fit-content;
}

#header a {
  padding: 0px;
  text-decoration: none;
}

#header a:visited {
  color: #dae4ee;
}

#description {
  margin: 5px 10px;
  grid-row: 2 / 3;
  grid-column: 2 / 3;
  justify-self: left;
  text-align: left;
}

#thumbnail {
  width: 128px;
  height: 128px;
  grid-row: 1 / 3;
  grid-column: 1 / 2;
  border-radius: 5px 0px 0px 5px;
  padding: 0px;
  margin: 0px;
}
</style>

<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <ForceDirectedGraph
      id="mytest"
      width="900"
      height="600"
      :nodes="nodes"
      :edges="edges"
    />
  </div>
</template>

<script>
import ForceDirectedGraph from "./ForceDirectedGraph.vue";

export default {
  components: { ForceDirectedGraph },
  data() {
    return {
      msg: "ForceDirectedGraph",
      nodes: [
        { name: "天津大学" },
        { name: "南京大学" },
        { name: "武汉大学" },
        { name: "浙江大学" },
        { name: "人民大学" },
        { name: "清华大学" },
      ],
      // 边集
      edges: [
        { source: 2, target: 0, relation: "学生1", value: 2.7 },
        { source: 2, target: 1, relation: "学生2", value: 3.7 },
        { source: 2, target: 2, relation: "学生3", value: 1.7 },
        { source: 2, target: 3, relation: "学生4", value: 1.7 },
        { source: 2, target: 4, relation: "学生5", value: 1.7 },
        { source: 2, target: 5, relation: "学生6", value: 1.7 },
        { source: 2, target: 5, relation: "学生7", value: 1.7 },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>

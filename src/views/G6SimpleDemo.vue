<template>
    <div>
        <div id="mountNode"></div>
    </div>
</template>

<script>
import G6 from "@antv/g6"

export default {
    name: "G6Demo",
    data() {
        return {
            graph: null,
            graphData: {
                nodes: [
                    {
                        id: "node1",
                        x: 100,
                        y: 200
                    },
                    {
                        id: "node2",
                        x: 300,
                        y: 200
                    }
                ],
                edges: [
                    {
                        source: "node1",
                        target: "node2"
                    }
                ]
            }
        }
    },
    mounted() {
        this.graph = new G6.Graph({
            container: "mountNode",
            width: 500,
            height: 500
        })
        this.graph.data(this.graphData)
        this.graph.render()
    }
}
</script>

<style scoped></style>

<script>
    export default { 
        // Add code in appropriate places
        data() {
            return {
                items: ['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter'],
                input: ""
            }
            
        },
        methods: {
            addItem() {
                if (this.input.trim() !== "") {
                    this.items.push(this.input.trim())
                    this.input = ""
                }
            },
            deleteItem(index) {
                this.items.splice(index, 1)
            }
        }
    }
</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
    <ul>
        <li v-for="item, index in items">{{ item }}
            <button @click="deleteItem(index)"> Delete! </button>
        </li>
    </ul>
    <input v-model="input"></input><button @click="addItem()"> Add! </button>
</template>

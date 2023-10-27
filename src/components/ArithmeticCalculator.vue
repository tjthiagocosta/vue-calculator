<template>
    <div>
        <input type="number" v-model.number="num1" />
        <select v-model="operation">
            <option value="add">+</option>
            <option value="subtract">-</option>
            <option value="multiply">*</option>
            <option value="divide">/</option>
        </select>
        <input type="number" v-model.number="num2" />

        <p>Resultado: {{ result }}</p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            num1: 0,
            num2: 0,
            operation: 'add'
        };
    },
    computed: {
        result() {
            switch (this.operation) {
                case 'add':
                    return this.num1 + this.num2;
                case 'subtract':
                    return this.num1 - this.num2;
                case 'multiply':
                    return this.num1 * this.num2;
                case 'divide':
                    return this.num2 !== 0 ? this.num1 / this.num2 : 'Impossivel dividir por 0';
                default:
                    return 'Invalid operation';
            }
        }
    }
};

</script>

<style scoped>

input,
select {
    padding: 10px 15px;
    margin: 5px;
    border: none;
    border-radius: 5px;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
    font-size: 16px;
    outline: none;
}

p {
    margin-top: 20px;
    font-size: 20px;
    color: #333;
}
</style>
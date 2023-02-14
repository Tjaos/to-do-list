<template>


    <div id="input-main">
        <form @submit.prevent="submitForm">
            <input type="text" class="input" id="atividade" name="atividade" v-model="input_atividade"
                placeholder="Atividade">
            <input type="text" class="input" id="descricao" name="descricao" v-model="input_descricao"
                placeholder="Descrição">
            <input type="text" class="input" id="data-inicial" name="data-inicial" v-model="input_data1"
                placeholder="Data Inicial">
            <input type="text" class="input" id="data-final" name="data-final" v-model="input_data2"
                placeholder="Data Final">
            <button type="submit">Enter</button>

        </form>
    </div>

    <table id="table-main" style="width:100%;">
        <thead>
            <tr>
                <th>Atividade</th>
                <th>Descrição</th>
                <th>Status</th>
                <th>Data início</th>
                <th>Data fim</th>
            </tr>
        </thead>

        <tbody>
            <tr id="" :key="index" v-for="( dado, index ) in dados">
                <td>{{ dado.atividade }}</td>
                <td>{{ dado.descricao }}</td>
                <td>{{ dado.status }}</td>
                <td>{{ dado.data1 }}</td>
                <td>{{ dado.data2 }}</td>
                <button id="btn-td" @click.prevent="deletar(index)">excluir</button>
            </tr>
        </tbody>
    </table>

    
    <!--
        <div>
            <div id="row" :key="index" v-for="( dado, index ) in dados">{{ dado }}
                <div id="btn">
                    <button @click.prevent="deletar(index)">deletar</button>
                </div>
            </div>
    
        </div>
    -->
</template>

<script>
export default {
    name: "Input",
    data() {
        return {
            input_atividade: "",
            input_descricao:"",
            input_data1:"",
            input_data2:"",
            dados: []
        }
    },
    methods: {
        submitForm() {
            console.log(this.input_atividade);
            this.dados.push({
                atividade: this.input_atividade,
                descricao: this.input_descricao,
                data1: this.input_data1,
                data2: this.input_data2
            });

            //Limpa o input
            this.input_atividade = "";
            this.input_descricao = "";
            this.input_data1 = "";
            this.input_data2 = "";
        },
        deletar(index) {
            console.log(index)
            this.dados.splice(index, 1)
        }

    }

}


</script>

<style scoped>
#input-main {
    margin-top: 40px;
    width: 100%;
    height: 30px;
    align-items: center;
    display: flex;
    justify-content: center;
}

.input {
    font-size: 20px;
    font-family: Georgia, 'Times New Roman', Times, serif;
    border-radius: 5px;
    height: 80%;
    width: 400px;
}

button {
    margin-left: 30px;
    height: 100%;
    width: 80px;
    cursor: grab;
}

#table-main {
    margin-top: 30px;
}

#row {
    margin-top: 50px;
    align-items: center;
    justify-content: left;
    display: flex;
    padding-left: 30px;
}

#btn-td {
    width: 56px;
    align-items: center;
    justify-content: right;
    display: flex;
    background-color: red;
    color: aliceblue;
    font-size: 15px;
    border: none;
    border-radius: 5px;
}

table,
tr,
th,
td {
    border: 1px solid black;
}
</style>
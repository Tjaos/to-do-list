<template>
    <div id="footer">
        <div id="div-icon">
            <img id="icon-to-do-list" src="../assets/icon.png" alt="icon to-do-list">
        </div>
        <div id="h1"> 
            <h1>To Do list</h1>
        </div>
       
    </div>
</template>

<script>
export default{
    name: "Footer"
}
</script>

<style scoped>
#footer{
    justify-content: center;
    align-items: center;
    margin-left: 50%;
    transform: translate(-50%);
    height: 150px;
    width:50%;
    display: flex;
    border: 1px solid black;
    background-color: rgba(133, 161, 172, 0.5);
    border-radius: 10px;
}   

#icon-to-do-list{
    height: 80px;
    width: 80px;
    position: start;
}

#div-icon{
    justify-content: flex-start;
    padding-left: 30px;
    align-items: center;
    width: 30%;
}

#h1{
    justify-content: center;
    align-items: center;
    width: 60%;
}
</style>
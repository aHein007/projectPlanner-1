<template>
   <div class="project">
        <div class="flexing">
            <div>
                <h3  @click="showDetail=!showDetail">{{ project.title }}</h3>
            </div>

            <div class="spacing">
                <i class="fa-solid fa-trash"></i>
                <i class="fa-solid fa-edit"></i>
                <i class="fa-solid fa-check"></i>
            </div>
        </div>
        <p v-if="showDetail">{{ project.detail }}</p>
        
    </div>
</template>

<script>
export default {
    props:[
        "project"
    ],

    data(){
        return{
            showDetail:false
        }
    }
}
</script>

<style>
.project{
    padding: 20px;
    background-color: #f2f2f2;
    border-radius: 6px;
    border-left: 6px solid pink;
    margin: 10px;
    user-select: none;
}

.flexing{
    display: flex;
    justify-content: space-between;
    align-items: center;
}

i{
    margin-right: 8px;
    cursor: pointer;
}

.spacing{
    margin-right: 10px;
}

h3{
    color: indigo;
    user-select: none;
    cursor: pointer;
}


i:hover{
    color: #777;
}
</style>
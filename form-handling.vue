<template>
    <div>
      <pre>
        {{ JSON.stringify(formValues,null,2) }}
      </pre>
    </div>
    <form @submit="submitForm">
      <div>
        <label for="name">Name</label>
        <input type="text" id="name" v-model="formValues.name">  
      </div>
    <div>
      <label for="profile">Profile summary</label>
      <input type="text" id="profile" v-model="formValues.profileSummary">
    </div>
    <div>
      <label for="country">country</label>
      <select id="profile" v-model="formValues.country">
        <option values="">select</option>
        <option values="india">india</option>
        <option values="china">china</option>
        <option values="bhutan">bhutan</option>
      </select>
    </div>

    <div>
      <label for="job-location">joblocation</label>
      <select id="job-location" multiple v-model="formValues.joblocation">
        <option values="">select</option>
        <option values="india">india</option>
        <option values="china">china</option>
        <option values="bhutan">bhutan</option>
      </select>
    </div>

    <div>
      <input type="checkbox" id="remoteWork" v-model="formValues.remotework" true-value="yes" false-value="no"/>
      <label for="remotework">open to relocate</label>
    </div>


    <div>
      <label>skill set</label>
      <input type="checkbox" id="html" value="html" v-model="formValues.skillset"/>      
      <label for="html">html</label>
      <input type="checkbox" id="js" value="js" v-model="formValues.skillset"/>          
      <label for="js">js</label>
      <input type="checkbox" id="css" value="css" v-model="formValues.skillset"/>      
      <label for="css">css</label>
    </div>

    <div>
      <label>yearsOfExperience</label>
      <input type="radio" id="0-2" value="0-2" v-model="formValues.yearsOfExperience"/>
      <label for="0-2">0-2</label>
      <input type="radio" id="3-2" value="3-5" v-model="formValues.yearsOfExperience"/>
      <label for="0-2">3-5</label>
    </div>
    <div>
      <button>submit</button>
    </div>
  </form>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {     
      formValues : {
        name: '',
     profileSummary : '',
     country : '',
     joblocation : [],
     remotework:'no',
     skillset:[],
     yearsOfExperience:''
    },
  }
},
  methods: {
    submitForm(event) {
      event.preventDefault()
      console.log('Forem values',this.formValues)
    }     
  }  
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
label {
  font-weight:bold;
  display: flex;
  margin-bottom: 5px;
}
input + label {
  font-weight:bold;
  display: inline-flex;
  margin-right: 20px;
}
input[type="text"],
textarea,
select {
  display: block;
  width:400px;
  padding:6px,12px;
  font-size:14px;
  color:grey;
  background-color: #fff;
  background-image: none;
  border-radius:4px;
}
</style>

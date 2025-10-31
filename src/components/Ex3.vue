<script>
export default { 
    data() {
        return {
            loginOption: "username" // default option
        }
    }
}
</script>

<template>
    <h1>Please select your login option</h1>

    <select v-model="loginOption">
        <option value="username">Username login</option>
        <option value="email">Email login</option>
    </select>
    
    <div v-if="loginOption === 'username'">
        <label>Username</label>
        <input placeholder="Enter your username">
    </div>

    <div v-else-if="loginOption === 'email'">
        <label>Email</label>
        <input placeholder="Enter your email">
    </div>
</template>
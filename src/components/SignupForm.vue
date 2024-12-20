<template>
  <form class="form-container">
    <label for="email" class="form-label">Email:</label>
    <input type="email" id="email" class="form-input" required />

    <!-- Example for additional fields -->
    <label for="password" class="form-label">Password:</label>
    <input type="password" id="password" class="form-input" required />

    <button type="submit" class="form-button">Submit</button>
  </form>
</template>

<script>
export default {};
</script>

<style scoped>

.form-container {
  max-width: 400px;
  margin: 0 auto;
  padding: 20px;
  background-color: #f9f9f9; 
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); 
  font-family: Arial, sans-serif;
}

.form-label {
  display: block;
  margin-bottom: 8px;
  font-weight: bold;
  color: #333;
  font-size: 14px;
}

.form-input {
  width: 100%;
  padding: 10px;
  margin-bottom: 20px; 
  border: 1px solid #ccc;
  border-radius: 4px;
  font-size: 14px;
  box-sizing: border-box;
  transition: border-color 0.3s ease, box-shadow 0.3s ease;
}

.form-input:focus {
  border-color: #007BFF;
  box-shadow: 0 0 4px rgba(0, 123, 255, 0.3); 
  outline: none;
}

.form-button {
  display: block;
  width: 100%;
  padding: 10px 15px;
  background-color: #007BFF; 
  color: white;
  border: none;
  border-radius: 4px;
  font-size: 16px;
  font-weight: bold;
  cursor: pointer;
  text-align: center;
  transition: background-color 0.3s ease, transform 0.2s ease;
}

.form-button:hover {
  background-color: #0056b3; 
}

.form-button:active {
  transform: scale(0.98); 
}
</style>

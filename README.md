# Exp 5 – React Lab Exercise: Form Handling in React

## NAME : Hariharan S
## REG NO : 2305001009

## Aim
To develop a simple Student Registration Form using React and handle form input values using the `useState` Hook.

## Objectives
- To create a form using React.
- To create input fields such as Name, Register Number, and Department.
- To use `useState()` to store form data.
- To handle input changes using `onChange`.
- To handle form submission using `onSubmit`.
- To display submitted student details.

## Program

### Step 1 – Create React Project

```bash
npm create vite@latest react-form
cd react-form
npm install
npm run dev
```

Select React as the framework and JavaScript as the variant.

### Step 2 – App.jsx

```jsx

import React, { useState } from "react";
import "./App.css";

function App() {
  const [name, setName] = useState("");
  const [registerNo, setRegisterNo] = useState("");
  const [department, setDepartment] = useState("");

  const handleSubmit = (event) => {
    event.preventDefault();

    alert(
      "Name: " + name +
      "\nRegister Number: " + registerNo +
      "\nDepartment: " + department
    );
  };

  return (
    <div className="container">
      <h1>Student Registration Form</h1>

      <form onSubmit={handleSubmit}>
        <label>Name:</label>
        <input
          type="text"
          value={name}
          onChange={(event) => setName(event.target.value)}
          placeholder="Enter your name"
          required
        />

        <label>Register Number:</label>
        <input
          type="text"
          value={registerNo}
          onChange={(event) => setRegisterNo(event.target.value)}
          placeholder="Enter register number"
          required
        />

        <label>Department:</label>
        <input
          type="text"
          value={department}
          onChange={(event) => setDepartment(event.target.value)}
          placeholder="Enter department"
          required
        />

        <button type="submit">Submit</button>
      </form>
    </div>
  );
}

export default App;

```

### Step 3 – App.css

```css

.container {
  width: 400px;
  margin: 50px auto;
  padding: 25px;
  border: 1px solid gray;
  border-radius: 10px;
}

h1 {
  text-align: center;
  color: blue;
}

label {
  display: block;
  margin-top: 15px;
  font-weight: bold;
}

input {
  width: 100%;
  padding: 10px;
  margin-top: 5px;
  box-sizing: border-box;
}

button {
  margin-top: 20px;
  padding: 10px 20px;
  background-color: blue;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}
```

## Output

### Entered Student Details
<img width="1920" height="919" alt="Screenshot 2026-10-30 091148" src="https://github.com/user-attachments/assets/767549f4-8312-42ef-bb38-1f6174c67d92" />


### Submitted Details – Alert Box
<img width="1920" height="911" alt="Screenshot 2026-10-30 091221" src="https://github.com/user-attachments/assets/fc243736-d46d-49f8-8af6-c903ef1240fa" />


## Result

Thus, a Student Registration Form was successfully created using React. Form input values were managed using the `useState()` Hook, input changes were handled using `onChange`, and form submission was handled using `onSubmit`. The submitted student details were successfully displayed using an alert box.

<!--HTML-->
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Contact Form</title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" type="text/css" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/7.0.1/css/all.min.css">
    <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
    <div class="Contact-container">
        <h1>Contact Us</h1>
        <div class="contact-wrapper">
            <div class="Contact-form">
                <form action="">
                    <div class="form-group">
                        <input type="text" id="name" placeholder="Your Name" required>
                    </div>
                    <div class="form-group">
                        <input type="email" id="email" placeholder="Your Email" required>
                    </div>
                    <div class="form-group">
                        <textarea name="message" id="message" rows="5" placeholder="Your message" required></textarea>
                    </div>
                    <button type="submit">Send Message</button>
                    <p class="status" id="statusMsg"></p>
                </form>
            </div>
            <div class="contact-info">
                <h2>Contact Information</h2>
                <p><i class="fas fa-phone"></i>+1 123 456 788</p>
                <p><i class="fas fa-envelope"></i>info@gmail.com</p>
                <p><i class="fas fa-map-marker alt"></i>148 Street, City, Country</p>
            </div>
        </div>
    </div>

    <script src="script.js"></script>

</body>
</html>


<!--CSS-->
*{
    margin: 0px;
    padding: 0px;
    box-sizing: border-box;
    font-family: "Arial", sans-serif;
}
body{
    background: linear-gradient(135deg, #e0f7fa,#fff0f6);
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 30px;
}
.Contact-container{
    background-color: #fff;
    border-radius: 16px;
    box-shadow: 0 10px 30px rgba(0, 0, 0 , 0.1);
    max-width: 900px;
    width: 100%;
    padding: 32px;
}
.Contact-container h1{
    text-align: center;
    margin-bottom: 25px;
    color: black;
    font-size: 32px;
}
.contact-wrapper{
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-gap:50px;
}
.form-group{
    margin-bottom: 22px;
}
input, textarea{
    width: 100%;
    height: 50px;
    padding: 12px, 16px;
    border: 1px solid #999;
    border-radius: 8px;
    font-size: 16px;
    background-color: #f0f0f0;
}
input:focus, textarea:focus{
    border-color: #007bff;
    box-shadow: 0 0 5px rgba(0, 172, 193, 0.5);
    outline: none;
}
textarea{
    resize: vertical;
    min-height: 120px;
}
button{
    display: block;
    margin: auto;
    background-color: #4caf50;
    color: #fff;
    border: none;
    padding: 12px;
    font-size: 16px;
    border-radius: 8px;
    cursor: pointer;
    transition: 0.3s;
}
button:hover{
    background-color: #0056b3;
}
.contact-info{
    text-align: left;
}
.contact-info h2{
    font-size: 24px;
    margin-bottom: 20px;
    color: #333;
}
.contact-info p{
    margin-bottom: 10px;
    color: #555;
}
.contact-info i{
    color: #4caf50;
    margin-right: 10px;
}
.status{
    text-align: center;
    margin-top: 10px;
    font-size: 5000;
}
@media (max-width: 600px){
    .Contact-container{
        padding: 20px;
    }
}

<!--JAVASCRIPT-->
const form = document.getElementById("Contact-container");
const statusMsg = document.getElementById("statusMsg");

form.addEventListener("submit", function (e){
    e.preventDefault();
    const name = document.getElementById("name").Value.trim();
    const email = document.getElementById("email").Value.trim();
    const message = document.getElementById("message").ariaValueMax.trim();
    if(name === "" || email === "" || message === ""){
        statusMsg.textContent = "Please Fill in all fields.";
        statusMsg.style.color = 'red';
        return;
    }
    form.reset();
})


<!--TODO LIST-->
<!--HTML-->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,
    300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap" rel="stylesheet">
</head>
<body>
    <div class="main">
        <div class="box">
            <h2>To Do List</h2>
            <div class="inp">
                <input type="text" placeholder="Add your task here" id="todo">
                <button id="btn">Add</button>
            </div>
            <div class="list">
                <ul id="list-con">
                    <!--<li class="checked">task-1</li>
                    <li>task-2</li>
                    <li>task-3</li>-->
                </ul>
            </div>
        </div>
    </div>
    


   <script src="script.js"></script>

</body>
</html>

<!--CSS-->
*{
    font-family: "Poppins", sans-serif;
    padding: 0px;
    margin: 0px;
    box-sizing: border-box;
}
.main{
    height: 100vh;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    background-image: linear-gradient(to top, #5ee7df 0%, #b490ca 100%);
}
.box{
    width: 100%;
    max-width: 540px;
    background-color: #fff;
    margin: 100px auto 20px;
    padding: 40px 30px 70px;
    border-radius: 10px;
}
.box h2{
    color: #2e3434;
    font-size: 28px;
    margin-bottom: 30px;
}
.inp{
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin: 10px 0px;
    overflow: hidden;
    border-radius: 60px;
    background-color: #f3f3f3;
    margin-bottom: 40px;
}
.inp input{
    width: 80%;
    height: 60px;
    outline: none;
    border: none;
    font-size: 17px;
    padding: 0px 30px;
    background-color: #f3f3f3;
    color: #2e3434;
}
.inp button{
    font-size: 17px;
    padding: 18px 60px;
    border-radius: 60px;
    background-color: #96ceff;
    border: none;
    outline: none;
    color: #2e3434;
}
ul li{
    list-style: none;
    padding: 12px 8px 12px 50px;
    user-select: none;
    cursor: pointer;
    position: relative;
    margin-left: 24px;
    font-size: 20px;
    text-wrap: wrap;
}
ul li::before{
    content: "";
    height: 32px;
    position: absolute;
    width: 32px;
    background-image: url("radio.png");
    background-size: cover;
    background-position: center;
    top: 8px;
    left: 0px;
}
ul li.checked{
    color: #2e3434a4;
    text-decoration: line-through;
}
ul li.checked::before{
    content: "";
    height: 28px;
    position: absolute;
    width: 28px;
    background-image: url("check.png");
    background-size: cover;
    background-position: center;
    top: 8px;
    left: 0px;
}
ul li span{
    position: absolute;
    right: 10px;
    top: 12px;
    font-size: 29px;
}

<!--JAVASCRIPT-->
const input = document.querySelector("#todo");
const btn = document.querySelector("#btn");
const listCon = document.querySelector("#list-con");

function addTask(){
    if(input.value === ""){
        alert("You have to enter any task");
    }else{
        const li = document.createElement("li");
        li.innerHTML = input.value;
        listCon.appendChild(li);
        const span = document.createElement("span");
        span.innerHTML = "\u00d7";
        li.appendChild(span);
    }
    input.value = "";
}
btn.addEventListener("click",()=>{
    addTask();
})

listCon.addEventListener("click",(e)=>{
    if(e.target.tagName === "LI"){
        e.target.classList.toggle("checked");
    }else if(e.target.tagName === "SPAN"){
        e.target.parentElement.remove();
    }
})


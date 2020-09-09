### Hi there 👋👋👋

- ***Personal details***
    - First name ___RATTAMNOON___
    - Last name ___KIRATIPISUT___
    - Nickname  ___UN___
    - Age __23__ year old
    - Contact number (optional)
        - :telephone: ___Thailand +66 95 894 0136___
    - Gender (optional) 
        - :man: ___Male___
    - Date of birth (optional)
        - :date: ___17 Nov 1996___
    - Email 
        - :email: ___rattamnoon.kir@gmail.com___
    - Social
        - [facebook](https://web.facebook.com/RATTAMNOON)

- ***Education*** 👨‍🎓
    - [x] Institute ___Naresuan University.___
    - [x] Education level ___Degree.___
    - [x] Major ___Science Program in Physics.___
    - [x] Graduation Year ___2018.___

- ***Work experience*** 👨‍🏭
    - [x] Company ___WORLD MONEY LTD.___
    - [x] Position ___Frontend developer (Web application)___
    - [x] Employment period ___Apr 2020 - Present___
    - [x] Job function ___Sofyware Development.___
    - [x] Job industry ___Financial Services.___
    - [x] Roles and responsibilities (optional)
        - ***UX / UI design***
        - ***RESTFUL API*** send GET, POST, PUT, DELETE
        - ***Studying Blockchain*** (Starting to study the ***Smart contract***)

- ***Languages***
    - Thai 
    - English 
        - [ ] Excellent   
        - [ ] Good        
        - [x] Fair
        - [ ] Communicable  

- ***Current status*** 
    - [x] Live in ```Thailand Bangkok Dindaeng```
    - [x] Nationality ```Thailand```
    - [x] Highest education ```Degree```
    - [x] Total years of experience ```Less than one year```
    - [x] Employment period ```Apr 2020 - Present```

- ***Language and Freamwork***
    - **Language**
        - JavaScript
        - Python 
        - HTML
    - **Freamwork**
        - Djago
        - ReactJS
        - Node js
        - Bootstrap  
        - CSS

- ## ***Project***
    - Project ***WORLD MONEY*** about ***finance*** and ***blockchain to smart contract***

####ReactJS RESTFUL API 

```javascript
import axios from "axios"; // CONNECT NODE MODULES AXIOS 

const API_URL = 'http://localhost:8080/api-worldmoney_'; // SEND INFORMATION  OF USER.ID 

// FOR LOGIN, LOGOUT AND REGISTER !
export default new class AuthService {
  // SYSTEM LOGIN WITH EMAIL AND PASSWORD
  login(email, password) {
    return axios
      .post(API_URL + "/v2/auth/signin", {
        email,
        password
      })
      .then(res => {
        if (res.data.accessToken) {
          localStorage.setItem("_user", JSON.stringify(res.data));
        }

        return res.data;
      });
  }
  // SYSTEM LOGIN
  logout() {
    localStorage.removeItem("_user");
  }
  // SYSTEM REGISTER WITH EMAIL AND PASSOWRD
  register(email, password) {
    return axios.post(API_URL + "/v1/auth/signup", {
      email,
      password,
    });
  }

  // GET INFORMATION IN SYSTEM BACKEND WITH API 
  getCurrentUser() {
    return JSON.parse(localStorage.getItem('_user')); // STORE LOCALSTORAGE IN BOWSER
  }

}

```
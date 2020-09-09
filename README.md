### Hi there 👋👋👋

- ***Personal details***
    - First name ___RATTAMNOON___
    - Last name ___KIRATIPISUT___
    - Nickname  ___UN___
    - Age __23__ year old
    - Contact number (optional)
        - :iphone: ___Thailand +66 95 894 0136___
    - Gender (optional) 
        - :man: ___Male___
    - Date of birth (optional)
        - :date: ___17 Nov 1996___
    - Email 
        - :mailbox: ___rattamnoon.kir@gmail.com___
    - Social
        - :link: [facebook](https://web.facebook.com/RATTAMNOON)

- ***Education*** 👨‍🎓
    - :ballot_box_with_check: Institute ___Naresuan University.___
    - :ballot_box_with_check: Education level ___Degree.___
    - :ballot_box_with_check: Major ___Science Program in Physics.___
    - :ballot_box_with_check: Graduation Year ___2018.___

- ***Work experience*** 👨‍🏭
    - :ballot_box_with_check: Company ___WORLD MONEY LTD.___
    - :ballot_box_with_check: Position ___Frontend developer (Web application)___
    - :ballot_box_with_check: Employment period ___Apr 2020 - Present___
    - :ballot_box_with_check: Job function ___Sofyware Development.___
    - :ballot_box_with_check: Job industry ___Financial Services.___
    - :ballot_box_with_check: Roles and responsibilities (optional)
        - ***UX / UI design***
        - ***RESTFUL API*** send GET, POST, PUT, DELETE
        - ***Studying Blockchain*** (Starting to study the ***Smart contract***)

- ***Languages***
    - Thai 
    - English 
        - :white_large_square: Excellent   
        - :white_large_square: Good        
        - :ballot_box_with_check: Fair
        - :white_large_square: Communicable  

- ***Current status*** 
    - :ballot_box_with_check: Live in ```Thailand Bangkok Dindaeng```
    - :ballot_box_with_check: Nationality ```Thailand```
    - :ballot_box_with_check: Highest education ```Degree```
    - :ballot_box_with_check: Total years of experience ```Less than one year```
    - :ballot_box_with_check: Employment period ```Apr 2020 - Present```

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
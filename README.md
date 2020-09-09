### Hi there 👋👋👋

- ***Personal details***
    - First name ___RATTAMNOON___
    - Last name ___KIRATIPISUT___
    - Nickname  ___UN___
    - Age __23__ year old
    - Contact number (optional)
        - :telephone_receiver: ___Thailand +66 95 894 0136___
    - Gender (optional) 
        - :man: ___Male___
    - Date of birth (optional)
        - :date: ___17 Nov 1996___
    - Email 
        - :mailbox: ___rattamnoon.kir@gmail.com___
    - Social
        - :link: [facebook](https://web.facebook.com/RATTAMNOON)

- ***Education*** 👨‍🎓
    - :school: Institute ___Naresuan University.___
    - :mortar_board: Education level ___Degree.___
    - :white_check_mark: Major ___Science Program in Physics.___
    - :white_check_mark: Graduation Year ___2018.___

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
        - :white_check_mark: Fair
        - :white_large_square: Communicable  

- ***Current status*** 
    - :round_pushpin: Live in ```Thailand Bangkok Dindaeng```
    - :heavy_check_mark: Nationality ```Thailand```
    - :heavy_check_mark: Total years of experience ```Less than one year```
    - :heavy_check_mark: Employment period ```Apr 2020 - Present```

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
    ```
       There are 4 systems to develop.
          > systems frontend ReactJs, CSS, Bootstrap 
          > systems backend Node js, Mysql, express
          > systems backoffice (Collect data)
          > systems credit scoring Python (Data analysis)
    ```

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
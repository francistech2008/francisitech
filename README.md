

    <title>age checker</title>

    <meta charset='utf-8'>

    <meta name='viewport' content='width=device-width, initial-scale=1.0, user-scalable=no' />

    <meta name="blue" content="#00BFFF" />

    <meta name="yallow" content="#00BFFF" />

    <meta name="yellow" content="#ffffff" />

    <meta name="navigation-bar-button-hasshadow" content="false" />

    <style>

       body{

         font-family: Verdana, sans-serif;

         background-color:#6f00ff;

         color:white;        

       }

       input[type=text],textarea {

          -webkit-appearance: none;

          -moz-appearance: none;

          appearance: none;

       }

       input[type = checkbox] {

          -webkit-appearance: checkbox;

          -moz-appearance: checkbox;

          appearance: checkbox;

       }

       article{

          background-color:#00BFFF;     

          border-radius:5px;

          box-shadow:0px 0px 20px 1px white;

          padding:20px;

          max-width:480px;

          margin:auto;

          margin:auto;

          margin-top:40px;             

       }

       label,select{

          font-style:bold;

          font-size:20px;

       }

       input,select{

          border-radius:5px;

          box-shadow:0px 0px 3px 1px white;

          color:black;

          border:none;

          border-radius:5px;

          font-style:bold;

          font-size:25px;

          padding:5px;

          background-color:white;

       }

       input[type=text],input[type=date]{

          width:100%;

       }

       input[type=button]{

          -webkit-appearance: none;

          -moz-appearance: none;

          appearance: none;

          background-color:#48ff00;

          color:white;

          padding:5px 25px ;

       }

       h1{

          font-size:30px;

          margin:0px;

       }



       .text-align-center{

          text-align:center;

       }

       .title-header{

          border-radius:20px;

          box-shadow:0px 0px 10px 1px white;

          text-shadow:-1px 1px 2px black;

          padding:3px;

       }

       .calculator-info{

          border-radius:20px;

          text-shadow:-1px 1px 2px black;

          padding:3px;

          font-size:20px;

          display:none;

       }

    </style>



    <header>

    



    </header>

    <nav>

  

    </nav>

    <section>

       <div class = "text-align-center">     

       </div>

       <article>

        <div class = "title-header text-align-center">

        <h1>Age Calculator<h1>

        </div>

        <br/>

        <label>Name </label>

        <br/>

        <br/>

        <input type='text' id='nametxt' required />

        <br/>

        <br/>

        <label>Last Name</label>

        <br/>

        <br/>

        <input type='text' id='lastnametxt' required />

        <br/>

        <br/>

        <label>Birth date</label>

        <br/>

        <br/>

        <input type='date' id="birthdate" placeholder="Select date">

        <br/>

        <br/>

        <label>To</label>

        <br/>

        <br/>

        <input type='date' id="todate" placeholder="Select date">

        <br/>

        <br/>

        <div id='personinfo' class = "calculator-info text-align-center">

          No selection    

        </div>

        <br/>

        <input type='button' id='showinfobtn' onclick='showInfo()' value='Get age' />

        <script>

            var getName = document.getElementById('nametxt');

            var getLastName = document.getElementById('lastnametxt');      

            var getBirthDate = document.getElementById('birthdate'); 

            var getToDate = document.getElementById('todate'); 

            function showInfo() {

              this.personinfo.style.display="unset";

              if(getName.value=="" || getLastName.value==""){

                this.personinfo.innerHTML="Please write your first name and last name.<br/>";

                this.personinfo.style.color="red";

                return;

              }

                var birthDateValue=new Date(getBirthDate.value);

                var toDateValue=new Date(getToDate.value);               

                var outPutYears="";

                var outPutMonths="";

                if(toDateValue.getFullYear() >= birthDateValue.getFullYear()){

                    outPutYears = (toDateValue.getFullYear() - birthDateValue.getFullYear());                 

                }else{

                    this.personinfo.innerHTML="'Birthdate' value must be less than 'To' date value.<br/>";

                    this.personinfo.style.color="red";

                    this.personinfo.style.textShadow="-1px 1px 2px white"

                    return;

                }

                if(toDateValue.getMonth() > birthDateValue.getMonth()){

                    outPutMonths = (toDateValue.getMonth() - birthDateValue.getMonth());                

                }else{

                    outPutMonths = (birthDateValue.getMonth() - toDateValue.getMonth());               

                }

                this.personinfo.innerHTML = getName.value + ' ' + getLastName.value + ' is ' +  outPutYears  + ' years and ' + outPutMonths + ' months old.<br/>';               

                this.personinfo.style.color="#ffffff";

                this.personinfo.style.textShadow="-1px 1px 2px green"

            }

        </script>

    </article>

    </section>

    <footer>



    </footer>


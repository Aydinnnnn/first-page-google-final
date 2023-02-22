<template>
  <div>
    <v-row>
      <v-col cols="12">
        <div class="header">
          <div class="header-left">
            <button class="btn-header-about">About </button>
            <button class="btn-header-store">Store </button>
          </div>

          <div class="header-right">
            <button class="btn-header-Gmail">Gmail </button>
            <button class="btn-header-Images">Images </button>
            <img class="googleApp-pic" src="../assets/grid.png" alt="1">

            <img @click="visibility = 1" class="info-pic" src="../assets/AydinPic.jpg" alt="1">

          </div>


        </div>
      </v-col>
      <v-col cols="6" v-if="visibility === 1">
        <v-card
            class="card"
            max-width="350"
            height="300"


        >
          <v-list-item three-line>
            <v-list-item-content>
              <div class="text-overline mb-4 ">
                <img @click="visibility = 0" class="cross" src="../assets/cross.png" alt="cross">
              </div>
              <v-list-item-title class="text-h5 mb-1">
                <p>Aydin Habibi</p>

                <v-btn variant="outlined" class="mt-0" >
                  Manage

                </v-btn><br>

               <p class="text-button"> Add another account</p>
              </v-list-item-title>
              <v-list-item-subtitle>Sign Out</v-list-item-subtitle><br>
              <div class="v-data-footer">
              <v-list-item-subtitle>Privacy Policy</v-list-item-subtitle>
              <v-list-item-subtitle>Terms Of Services</v-list-item-subtitle>
              </div>
            </v-list-item-content>
          </v-list-item>



        </v-card>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12">
        <div class="main">
          <div class="main-logo">
            <img class="main-logo-pic" src="../assets/googlelogo_color_272x92dp.png" alt="2">
          </div>

          <div class="search-bar" >
            <input @click="showResult=1" class="main-search-bar" type="text" >



            <div class="main-search-bar-btn">
              <img @click="showResult" class="magnifier " src="../assets/magnifier.png" alt="3">

              <img class="mic" src="../assets/Google_mic.png" alt="4">
              <img class="camera" src="../assets/camera.png" alt="5">
            </div>

          </div>

        </div>
      </v-col>
    </v-row>


    <v-row>
      <v-col cols="12">
        <div class="main-button">
          <button  class="btn-google-search">Google Search</button>
          <button class="btn-feel-lucky"> I'm Feeling Lucky</button>
        </div>
        <div class="Google-offered-in">
          <p>Google offered in</p> <a class="link-below" href="#">: Deutsch</a>
        </div>
      </v-col>
    </v-row>
    <v-row>
      <v-col  v-show ="showResult === 1">

        <div class="modal-search-box">
          <ul>
            <li>what is vuex</li>
            <li>differences between localStorage and cookies</li>
            <li>how to use v-menu</li>
            <li>v-card in vue </li>
            <li>component in vue js</li>
          </ul>

        </div>

      </v-col>
    </v-row>
<!--    <script>-->
<!--      const elm = document.getElementsByClassName('main-search-bar')-->
<!--      document.addEventListener('click',function (event) {-->
<!--        if (event.target.closest('.main-search-bar')) return-->
<!--        elm.style.display('none')-->
<!--      })-->
<!--    </script>-->
  </div>

</template>

<script>
  export default {
    name: 'HelloWorld',



    data(){
    return{
      showResult: null,
      visibility: null,


    }
    },

    methods: {




  }
  }

</script>
<style>
.header{
  display: flex;
  justify-content:space-between;

}
.header-left{
  margin-top: 20px;
  margin-left: 40px;
}
.header-right{
  display: flex;
  gap:20px;

}
.main-search-bar-btn{
  margin-top: 5px;
}
.btn-header-about,
.btn-header-store,
.btn-header-Gmail,
.btn-header-Images{
  font-size: small;
  margin: 10px 0 20px 0;

}
.btn-header-about{

  margin-right: 15px;
}
.googleApp-pic{
  width: 30px;
  height: 30px;
  margin: 15px 0 20px 0;
}
.info-pic{
  width: 35px;
  height: 35px;
  border-radius: 100px;
  margin: 10px 20px 0  0;


}

.search-bar{
  position: absolute;
  left: 50%;
  margin-left: -300px;
  /*right: 50%;*/
  /*margin-right: -300px;*/

}
.main-logo-pic{
  width:  250px;
  height: 90px;
  margin-top: -40px
}
.main-search-bar{

  width: 600px;
  height: 45px;
  border-radius:30px;
  border:1px solid rgb(223,225,229);
  margin-top: 20px;
 padding-left: 60px
}
.main-search-bar:hover{
  border: none;
  border-bottom-left-radius: 5px;
  border-bottom-right-radius: 5px;
  box-shadow: 0 0 3px 3px rgb(227,227,228);
  outline: none;
}
.magnifier{
  position: absolute;
  right: 260px;
  bottom: 16px;
  width: 20px;
  height: 20px;
  margin-right: 300px;

  opacity: .5;
}
.mic{
  position: absolute;
  bottom: 16px;
  right: 70px;
  width: 15px;
  height: 20px;

}
.camera{
  position: absolute;
  bottom: 16px;
  right: 20px;
  width: 20px;
  height: 20px;
}
.main-button{
  display: flex;
  justify-content: center;
  margin-top: 100px;



}
.btn-google-search,
.btn-feel-lucky{
  font-size: large;
  padding: 10px;
  margin-right: 30px;
}

.btn-feel-lucky:hover,
.btn-google-search:hover{
  border: 1px solid grey;
  border-radius: 5px;
  background-color: rgb(248,249,250);
}
.Google-offered-in{
  margin-top: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.Google-offered-in p{
  font-size: large;
}
.link-below{
  text-decoration: none;
  margin-bottom: 15px;

}
.main-logo{
  display: flex;
  justify-content: center;
  align-items: center;
}
.card{
  position: fixed;
  left: 980px;
  margin-top: -30px;
  border-radius: 100px;
  z-index: 1000
}
.cross{
  width: 20px;
  height: 20px;
}
.modal-search-box{
  position: absolute;
  z-index: 1000;
  margin: -195px 0 0  375px;
  width: 600px;
  background-color: white;
  border-radius: 10px;
  text-decoration: none;
  border: 1px solid rgb(223,225,229);



}
.modal-search-box ul li{
  margin: 20px
}



</style>
<template>
    <div>
       
        <header class="header">
            <div class="logo hidden">
                <img class="logo" src="/../images/logo.png" alt="logo">
            </div>
            <div class="menu hidden">
                <span class="menu__button" @click="open">&#9776;</span>
            </div>
              
            <div class="desktop__header flex__nav">
             <div>
                <img class="logo" src="/../images/logo.png" alt="logo">
                 
             </div>
             <div>

             </div>
             
                <!-- <div class="contact">
                    <div class="contact__item">
                    <img class="icon" src="/../images/mail.png" alt="">
                    <a href="mailto:test@gmail.com"> info@gmail.com</a> 
                    </div>
                    <div class="contact__item">
                    <img class="icon" src="/../images/phone.png" alt="">
                    <a href="tel:+221777102353">+221777102353</a>
                      
                     </div>
                </div> -->
            </div>
        </header>
      <nav class="nav">
          <router-link to="/" class="nav__links" >QUI SOMMES-NOUS ?</router-link>
          <router-link to="/" class="nav__links">FUNCTIONLITES</router-link>
          <router-link to="/" class="nav__links">SERVICES</router-link>
          <router-link to="" class="nav__links">TARIFS</router-link>
          <router-link to="/" class="nav__links">API</router-link>
          <router-link to="" class="nav__links">POUR QUI?</router-link>
             <router-link to="" class="nav__links">CONTACT</router-link>
      </nav>
      </div>
    
</template>

<script>
    export default {
        methods:{
            open(){
              if( document.querySelector(".nav").style.left == "-1900px"){
                  document.querySelector(".nav").style.left = "0";
                  
              }
              else{
                  document.querySelector(".nav").style.left ="-1900px"
              }
            }

        }
    }
</script>

<style lang="scss" scoped>

.logo{
    width: 300px;
}

.header{
    display: flex;
    padding: 1rem;
    align-items: center;
}
.desktop__header{
    display: none;
}
.menu{
    margin-left: auto;
    background:#854dff;
    color: #FFFFFF;
    padding: .5rem;
    font-size: 1.5rem;
    border-radius: 5px;
    cursor: pointer;
    font-weight: bolder;
    
    &__button{
          cursor: pointer;
    }
   

}

.nav{
  background: #061551;
  position: fixed;
  width: 100%;
  top: 4rem;
  bottom: 0;
  padding-top: 4rem;
  text-transform: capitalize;
  right: -1900px;
  transition: all .5s;
 
       &__links{
           display: block;
           text-decoration: none;
           color: #FFFFFF;
           padding-top: 2rem;
           font-weight: bolder;
           font-size: 1.2rem;
          
          
           
          
       }
     
   }

   @media(min-width: 64rem){
       
       .nav{
           position: static;
           display: flex;
           align-items: center;
           padding-top: 0;

           &__links{
               padding:2rem;

           }
       }

       .flex__nav{
           display: flex;
       }
       .hidden{
           display: none;
       }
       .desktop__header{
         
          width: 60%;
          margin: 0 auto;
          align-items: center;
       }
       .contact{
           display: flex;
           margin-left: auto;
        
            
            a{
                 color: #000;
            font-size: 1.2rem;
            }
       }
    //    .icon{
    //        padding-left: 1rem;
           
    //    }
    .contact__item{
        display: flex;
        margin-left: 2rem;
        align-items: center;
        
        
    }
   }
</style>
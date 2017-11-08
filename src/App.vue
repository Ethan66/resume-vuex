<template>
  <div id="app">
    <div class=page>
           <header>
             <Topbar/>
           </header>
           <main>
             <ResumeEditor/>
             <ResumePreview/>
           </main>
    </div>
  </div>
</template>

<script>
  import 'normalize.css/normalize.css'
  import './assets/reset.scss'
  import Topbar from './components/Topbar'
  import ResumeEditor from './components/ResumeEditor'
  import ResumePreview from './components/ResumePreview'
  import icons from './assets/icons'
export default {
  name: 'app',
  components: {Topbar, ResumeEditor, ResumePreview},
  created(){
        document.body.insertAdjacentHTML('afterbegin', icons) //
      }

}
</script>

<style lang="scss">
#app {

}
.page{
     height: 100vh;
     display: flex;
     flex-direction: column;
  background: #EAEBEC;
  >main{
         flex-grow: 1;
       }
       >main{
         min-width: 1024px;
         max-width: 1440px;
         margin-top: 16px;
         margin-bottom: 16px;
         display: flex;
         justify-content: space-between;
         padding: 0 16px;
         width: 100%; /* 试试不加这句会怎样 */
         align-self: center;
       }
      }
</style>

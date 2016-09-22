<template>


  <div class="logo">
      <img src="assets/images/starfall-2014.png" width="220" height="60" alt="Starfall">
  </div>

  <div class="header row" :class="{'expand': show.mobileNav}">
    <div class="row">
      <button class="mobile-nav-toggle btn btn-info" @click.prevent="show.mobileNav = !show.mobileNav">Menu</button>
    </div>
    <div id="nav-wrap" class="nav-wrap" :class="{'show':show.mobileNav}">

        <ul class="nav">

            <li><a href="http://more.starfall.com/info/parents.php">Parents</a></li>

            <li class="bullet"> &nbsp; • &nbsp; </li>

            <li><a href="http://more.starfall.com/info/educators.php">Educators</a></li>

            <li class="bullet"> &nbsp; • &nbsp; </li>

            <li><a href="http://more.starfall.com/info/homeschool.php">Homeschool</a></li>

            <li class="bullet"> &nbsp; • &nbsp; </li>

            <li><a href="https://store.starfall.com/">Store</a></li>

        </ul>

        <ul class="navr">

            <li><a href="https://more.starfall.com/memb/login1.php">Login/Authorize</a></li>

            <li class="bullet"> &nbsp; • &nbsp; </li>

            <li><a href="http://more.starfall.com/info/ways-to-join.php?ref=NI_MenuBar">How to Join</a></li>

        </ul>

        <div class="ribbon-container">

            <h1 class="ribbon">

                Kindergarten Mathematics curriculum is here! <a href="http://more.starfall.com/info/curriculum/k-math.php" class="btn btn-sm">Learn More</a>

            </h1>

        </div>
      </div>

  </div>

  <!--END HEADER-->



  <!--BEGIN Container-->

  <div class="container">

      <!--BEGIN COL LEFT-->

      <div class="col-sm-6" id="col-left">

          <button v-if="flash && !useHtmlFive" class="btn btn-info" @click.prevent="useHtmlFive = !useHtmlFive">New HTML5 version available! View in HTML5.</button>
          <button v-if="flash && useHtmlFive" class="btn btn-info" @click.prevent="useHtmlFive = !useHtmlFive">Viewing HTML5 version. Return to Flash version.</button>
          <!-- <label for="useHtmlFive" class="useHtmlFive"><input type="checkbox" v-model="useHtmlFive" id="useHtmlFive"> New HTML5 version available! View in HTML5.</label> -->

          <div class="row">
              <a :class="{ 'disabled':!hasFlash && !links.ABCs.html5 }" :href="getHref(links.ABCs)">
                  <div class="classic table ABC"><div class="number table-cell">1</div>
                      <div class="table-cell img-well">
                        <img src="assets/images/app-ABCs-114.png" alt="ABCs">
                      </div><p class="table-cell">ABCs</p></div></a>
          </div>

          <div class="row">
              <a :class="{ 'disabled':!hasFlash && !links.LearnToRead.html5 }" :href="getHref(links.LearnToRead)">
                  <div class="classic table LTR"><div class="number table-cell">2</div>
                      <div class="table-cell img-well">
                        <img src="assets/images/app-LTR-114.png" alt="Learn to Read">
                      </div><p class="table-cell">Learn to Read</p></div></a>

          </div>

          <div class="row">
              <a :class="{ 'disabled':!hasFlash && !links.FunToRead.html5 }" :href="getHref(links.FunToRead)">
                  <div class="classic table FTR"><div class="number table-cell">3</div>
                      <div class="table-cell img-well">
                        <img src="assets/images/app-FunToRead-114.png" alt="Fun to Read">
                      </div><p class="table-cell">It's Fun to Read</p></div></a>
          </div>

          <div class="row">
              <a :class="{ 'disabled':!hasFlash && !links.ImReading.html5 }" :href="getHref(links.ImReading)">
                  <div class="classic table IR"><div class="number table-cell">4</div>
                      <div class="table-cell img-well">
                        <img src="assets/images/app-ImReading-114.png" alt="I&#39;m Reading">
                      </div><p class="table-cell">I'm Reading</p></div></a>
          </div>

          <div class="row holidayicon">

              <div class="col-1-10">
                <img src="assets/images/s.gif" style="width:40px; height:59px; float:left;" alt="">
              </div>

              <div class="col-1-5">
                <span :class="{ 'disabled':!hasFlash && !links.calendar.html5 }"><a :href="getHref(links.calendar)">
                    <img src="assets/images/h-calendar.gif" alt="Let&#39;s Make a Calendar"></a></span>
              </div>

              <div class="col-1-5">
                <span :class="{ 'disabled':!hasFlash && !links.gingerbread.html5 }"><a  :href="getHref(links.gingerbread)">
                    <img src="assets/images/h-gingerbread.gif" alt="Make a Gingerbread Boy or Girl"></a></span>
              </div>

              <div class="col-1-5">
                <span :class="{ 'disabled':!hasFlash && !links.snowman.html5 }"><a  :href="getHref(links.snowman)">
                    <img src="assets/images/h-snowman.gif" alt="Make a Snowman"></a></span>
              </div>

              <div class="col-1-5">
                <span :class="{ 'disabled':!hasFlash && !links.pumpkinPatch.html5 }"><a  :href="getHref(links.pumpkinPatch)">
                    <img src="assets/images/h-pumpkin.gif" alt="Pumpkin Patch"></a></span>
              </div>
          </div>

          <div class="row holidayicon">

              <div class="col-1-5">
                <span :class="{ 'disabled':!hasFlash && !links.turkey.html5 }"><a  :href="getHref(links.turkey)">
                    <img src="assets/images/h-turkey.gif" alt="Silly Turkey"></a></span>
              </div>

              <div class="col-1-5">
                <span :class="{ 'disabled':!hasFlash && !links.grandparents.html5 }"><a  :href="getHref(links.grandparents)">
                    <img src="assets/images/h-gparentsday.gif" alt="Grandparents Day, Let&#39;s write a letter!"></a></span>
              </div>

              <div class="col-1-5">
                <span :class="{ 'disabled':!hasFlash && !links.hundredthDay.html5 }"><a  :href="getHref(links.hundredthDay)">
                    <img src="assets/images/h-hundredth.gif" alt="Hundredth Day of School"></a></span>
              </div>

              <div class="col-1-5">
                <span :class="{ 'disabled':!hasFlash && !links.groundhog.html5 }"><a  :href="getHref(links.groundhog)">
                    <img src="assets/images/h-groundhog.gif" alt="Groundhog&#39;s Day"></a></span>
              </div>

              <div class="col-1-5">
                <span :class="{ 'disabled':!hasFlash && !links.clover.html5 }"><a  :href="getHref(links.clover)">
                    <img src="assets/images/h-clover.gif" alt="Find a Four Leaf Clover"></a></span>
              </div>
          </div>

          <div class="row holidayicon">

              <div class="col-1-10">
                <img src="assets/images/s.gif" style="" alt="">
              </div>

              <div class="col-1-5">
                <span :class="{ 'disabled':!hasFlash && !links.gardenshop.html5 }"><a  :href="getHref(links.gardenshop)">
                    <img src="assets/images/h-garden.gif" alt="Plant a Flower"></a></span>
              </div>

              <div class="col-1-5">
                <span :class="{ 'disabled':!hasFlash && !links.valentine.html5 }"><a  :href="getHref(links.valentine)">
                    <img src="assets/images/h-valentine-15.gif" alt="Make a Valentine"></a></span>
              </div>

              <div class="col-1-5">
                <span :class="{ 'disabled':!hasFlash && !links.spring.html5 }"><a  :href="getHref(links.spring)">
                    <img src="assets/images/h-spring.gif" alt="Go on a Word Hunt"></a></span>
              </div>

              <div class="col-1-5">
                <span :class="{ 'disabled':!hasFlash && !links.earthDay.html5 }"><a  :href="getHref(links.earthDay)">
                    <img src="assets/images/h-earth.gif" alt="Every Day is Earth Day!"></a></span>
              </div>
          </div>

      </div><!--END COL LEFT-->

      <!--BEGIN COL RIGHT-->

      <div class="col-sm-6" id="col-right">
          <div class="more">

              <a href="http://more.starfall.com/info/ways-to-join.php?ref=NI_DemoHeading"><h1>Get more from Starfall—Join today!</h1></a>

              <div class="row">
                  <div :class="{ 'disabled':!hasFlash && !links.firstGrade.html5 }" class="col-xs-4 icon-double"> <a :href="getHref(links.firstGrade)">
                    <img src="assets/images/FirstGrade.png" alt="First Grade Mathematics and Reading"></a></div>

                  <div :class="{ 'disabled':!hasFlash && !links.coinMonkey.html5 }" class="col-xs-4 icon-double"><a :href="getHref(links.coinMonkey)">
                    <img src="assets/images/coin-monkey-school.png" alt="Help Coin Monkey get ready for school!"  border="0"></a></div>

                  <div :class="{ 'disabled':!hasFlash && !links.mathJourney.html5 }" class="col-xs-4 icon-double"><a :href="getHref(links.mathJourney)">
                    <img src="assets/images/mathjourney-sch.png" alt="Journey back to school!" border="0"></a></div>
              </div>

              <div class="row">
                  <h2 class="col-11b more">Mathematics</h2>
              </div>

              <div class="row">
                  <div :class="{ 'disabled':!hasFlash && !links.mathSongs.html5 }" class="col-xs-4 icon-double"> <a :href="getHref(links.mathSongs)">
                    <img src="assets/images/MathSongs_index.png" alt="Math Songs"></a></div>

                  <div :class="{ 'disabled':!hasFlash && !links.mathNumbers.html5 }" class="col-xs-4 icon-double"> <a :href="getHref(links.mathNumbers)">
                    <img src="assets/images/Numbers_index.png" alt="Numbers"></a></div>

                  <div :class="{ 'disabled':!hasFlash && !links.mathGeometry.html5 }" class="col-xs-4 icon-double"> <a :href="getHref(links.mathGeometry)">
                    <img src="assets/images/Geometry_index.png" alt="Geometry"></a></div>
              </div>

              <div class="row">
                  <div :class="{ 'disabled':!hasFlash && !links.mathAddSubtract.html5 }" class="col-xs-4 icon-double"> <a :href="getHref(links.mathAddSubtract)">
                    <img src="assets/images/AddSub_index.png" alt="Addition and Subtraction"></a></div>

                  <div :class="{ 'disabled':!hasFlash && !links.mathMultiplyDivide.html5 }" class="col-xs-4 icon-double"> <a :href="getHref(links.mathMultiplyDivide)">
                    <img src="assets/images/MultDiv_index.png" alt="Multiplication and Division"></a></div>

                  <div :class="{ 'disabled':!hasFlash && !links.mathSecondGrade.html5 }" class="col-xs-4 icon-double"> <a :href="getHref(links.mathSecondGrade)">
                    <img src="assets/images/Selected2nd.png" alt="Selected 2nd Grade Math Skills"></a></div>
              </div>

              <div class="row">
                  <h2 class="col-11b more">Songs</h2>
              </div>

              <div class="row">
                  <div :class="{ 'disabled':!hasFlash && !links.bodyMotion.html5 }" class="col-xs-4 icon-double"> <a :href="getHref(links.bodyMotion)">
                    <img src="assets/images/MotionSongs.png" alt="Motion Songs"></a></div>

                  <div :class="{ 'disabled':!hasFlash && !links.nurseryRhymes.html5 }" class="col-xs-4 icon-double"> <a :href="getHref(links.nurseryRhymes)">
                    <img src="assets/images/SelectedNR.png" alt="Selected Nursery Rhymes"></a></div>

                  <div :class="{ 'disabled':!hasFlash && !links.folkSongs.html5 }" class="col-xs-4 icon-double"> <a :href="getHref(links.folkSongs)">
                    <img src="assets/images/FolkSongs_index.png" alt="Folk Songs"></a></div>
              </div>

              <div class="row">
                  <h2 class="col-11b more">Reading</h2>
              </div>

              <div class="row">
                  <div :class="{ 'disabled':!hasFlash && !links.abcRhymes.html5 }" class="col-xs-4 icon-double"> <a :href="getHref(links.abcRhymes)">
                    <img src="assets/images/ABC-r_index.jpg" alt="ABC Rhymes"></a></div>

                  <div :class="{ 'disabled':!hasFlash && !links.colors.html5 }" class="col-xs-4 icon-double"> <a :href="getHref(links.colors)">
                    <img src="assets/images/Colors_index.png" alt="Colors"></a></div>

                  <div :class="{ 'disabled':!hasFlash && !links.predecodeable.html5 }" class="col-xs-4 icon-double"> <a :href="getHref(links.predecodeable)">
                    <img src="assets/images/BPBbooks_index.png" alt="Backpack Bear&#39;s Books"></a></div>
              </div>

              <div class="row">
                  <div :class="{ 'disabled':!hasFlash && !links.wordMachines.html5 }" class="col-xs-4 icon-double"> <a :href="getHref(links.wordMachines)">
                    <img src="assets/images/WordMachines_index.png" alt="Word Machines"></a></div>

                  <div :class="{ 'disabled':!hasFlash && !links.phonics.html5 }" class="col-xs-4 icon-double noshadow"> <a :href="getHref(links.phonics)">
                    <img src="assets/images/MorePhonics_index.png" alt="More Phonics"></a></div>

                  <div :class="{ 'disabled':!hasFlash && !links.library.html5 }" class="col-xs-4 icon-double"> <a :href="getHref(links.library)">
                    <img src="assets/images/TalkingLibrary.png" alt="Talking Library"></a></div>
              </div>

              <div class="row">
                  <img src="assets/images/s.gif" alt="0" width="2" height="2">
              </div>

          </div><!--END COL RIGHT-->

      </div><!--END OF ROW-->

  </div><!--END OF CONTAINER-->

  <!--BEGIN FOOTER-->

  <div class="footer row">



      <ul class="nav">

          <li><a href="http://more.starfall.com/info/about.php">About</a></li>

          <li> &nbsp; • &nbsp; </li>

          <li><a href="http://more.starfall.com/privacy.php">Privacy</a></li>

          <li> &nbsp; • &nbsp; </li>

          <li><a href="http://more.starfall.com/info/service.php">Help</a></li>

          <li> &nbsp; • &nbsp; </li>

          <li><a href="http://more.starfall.com/info/service.php">Contact</a></li>

      </ul>



      <p class="about">Starfall.com is a program service of Starfall Education Foundation, a 501(c)(3)

          public charity. The website opened in September of 2002 as a free public service and social

          enterprise supported by the Polis-Schutz family. On July 1, 2015, the Polis-Schutz family donated

          their full interest in Starfall to the <a href="http://more.starfall.com/info/about.php">

          Starfall Education Foundation</a>.</p>



      <p class="about">Starfall has been teaching children to read with phonics for well over a decade.

          Our systematic approach, in conjunction with audiovisual interactivity is perfect for preschool,

          kindergarten, first grade, second grade, special education, homeschool, and English language development

          (ELD, ELL, ESL). Starfall is an educational alternative to other entertainment choices for children.</p>



      <p class="about">Our low-cost membership program expands the free content you already enjoy to include

          delightfully animated songs, mathematics, and reading activities spanning pre-k to 2nd grade.

          Your child will have fun learning essential reading and math skills through exploration! Your membership

          fee ensures that we can continue to provide Classic Starfall free of charge and offer low-cost, high-quality,

          educational resources to classrooms.</p>



      <p class="about">In May of 2009, we released the <a href="http://more.starfall.com/info/curriculum/kindergarten.php">

          <b>Starfall Kindergarten English and Language Arts Curriculum</b></a> and in June 2013 the

          <a href="http://more.starfall.com/info/curriculum/pre-k.php"><b>Starfall Pre-K Curriculum</b></a>.

          Our methodology motivates children in an atmosphere of imagination and play. The teacher-guided and

          child-directed nature of our curriculum products ensure English language learners and struggling readers

          learn alongside their peers. Please visit <a href="https://store.starfall.com/"><b>The Starfall Store</b></a>

          for our curriculum products and other low-cost phonics journals and books paralleling this website.</p>



      <p class="copyright">

        The Starfall Website is a program service of Starfall Education Foundation, a 501(c)(3) publicly supported charity.

        <br>Starfall® and Starfall.com® are registered trademarks in the U.S., the European Union, and various other countries.

        <br>Copyright © 2002–2016 by Starfall Education and its licensors. All rights reserved.

      </p>

  </div>

  <!--END FOOTER-->

</template>

<script>
import Modernizr from 'modernizr'
import links from 'assets/links.json'

export default {
  data () {
    return {
      links,
      flash: false,
      useHtmlFive: false,
      show: {
        mobileNav: false
      }
    }
  },
  ready () {
    Modernizr.on('flash', function (result) {
      this.flash = result
      return result
    }.bind(this))
    // if (this.flash === undefined) this.flash = Modernizr.flash
  },
  components: {},
  computed: {
    hasFlash: {
      cache: false,
      get () {
        if (this.flash === undefined) this.flash = Modernizr.flash
        return this.useHtmlFive ? false : this.flash
      }
    },
    screenSize: {
      cache: false,
      get () {
        return this.window.innerWidth || this.document.documentElement.clientWidth || this.document.body.clientWidth
      }
    }
  },
  methods: {
    getHref (link) {
      if (!this.hasFlash) return link.html5
      return link.flash
    }
  }
}
</script>

<style>
  /* START RESET */
  html, body, div, span, applet, object, iframe,h1, h2, h3, h4, h5, h6, p, blockquote, pre,a, abbr, acronym, address, big, cite, code, del, dfn, em, img, ins, kbd, q, s, samp,small, strike, strong, sub, sup, tt, var,b, u, i, center,dl, dt, dd, ol, ul, li,fieldset, form, label, legend,table, caption, tbody, tfoot, thead, tr, th, td,article, aside, canvas, details, embed, figure, figcaption, footer, header, hgroup, menu, nav, output, ruby, section, summary,time, mark, audio, video {
    margin:0;padding:0;border:0;font:inherit;vertical-align:baseline;text-decoration:none;list-style-type:none;
  }
  *{box-sizing: border-box;}
  html{font-size: 62.5%; }
  /* END RESET */

  body {
      background: #77cbff url(assets/images/BG-yellowstripe.gif) repeat;
      font-family: "Trebuchet MS", Arial, Helvetica, sans-serif;
      font-size: 1em;
      /*min-width:1070px;*/
  }

  .row{}
  .row:before,
  .row:after{ display: table; content: " "; }
  .row:after{clear: both;}

  .column{position:relative;float:left;}

  .container{
    /*width:980px;*/
    margin:auto; padding:0 2%;}

  .logo {
      background:#00b000; width:225px; border-radius: 0 0 15px 15px; box-shadow:0 2px 2px rgba(0,0,0,.35); margin:0 0 0 20px; text-align:center; position:absolute;display:block; z-index:4;
      behavior: url(/css/PIE.htc); /* well-tested solution for adding border-radius to IE 6-9 */
  }

  .logo img {position:relative; top:2px; left:2px}

  .ribbon-container{
      position:relative;
      top:0;
      z-index:3;
  }

  .ribbon {
      font: normal 1em "Trebuchet MS"; /*16px*/
      width: 478px;
      height: 25px;
      position: absolute;
      top: 15px;
      left: -30px;
      background: #39f;
      color: #fff;
      padding: 3px 0 0 8px;
      box-shadow:0 1px 1px rgba(0,0,0,.35);
      background: linear-gradient(to right, rgba(255,160,0,1), rgba(255,180,0,1), rgba(255,160,0,1)); /*Standard*/
  }

  .ribbon:after {
      content: "";
      position: absolute;
      display: block;
      top:3px;
      left:475px;
      border: 12px solid #ff8e00;
      border-left-width: 8px;
      border-right-color: transparent;
      z-index:-2;
  }

  .ribbon a {
      background:#ff8e00; color:#FFF; text-decoration:none; padding: 0 4px; border-radius:3px; behavior: url(/css/PIE.htc);
  }

  .ribbon a:hover { background:#FFF; color:#ff8e00;}

  .header, .footer{font-size: 1.6em;}
  .header { background:#97DBFF url(assets/images/BG-cloudsbanner.png) repeat-x; height:46px; border:none; border-collapse:collapse; padding:10px 0 0 265px; margin-bottom:25px; color: #005bc5; position:relative; z-index:2; }

  .nav li, .footer .nav li {float:left; border: none; }

  .navr {margin-right:15px;}

  .navr li {float:right; white-space:nowrap;}

  .nav a, .footernav a, .navr a {color:#005bc5; z-index: <##>;}
  .btn.mobile-nav-toggle { display: none; }

  @media (max-width:928px){
    .btn.mobile-nav-toggle { display: block; float: right; padding: 5px 10px; margin-right: 10px; color: #fff; }
    .header { padding: 20px 0 0 20px; }
    .ribbon:after{display: none;}
    .ribbon{position: static; width: auto; height: auto; background: none; box-shadow: none; font-size: 1em; left:0; top:0; margin: 0; padding: 5px 0; border: 0; text-align: left;}
    .nav, .navr, .nav li, .navr li{float: none; margin: none; }
    .nav li, .navr li{border-bottom: 1px solid #86D2FF; padding: 0;  }
    .nav li a, .navr li a{ display: block; padding: 5px; }
    .nav .bullet, .navr .bullet { display: none; }
    .nav-wrap, .header { transition: all .3s ease; }
    .nav-wrap { display: none; float: left; width: 100%; }
    .nav-wrap.show { display: block; }
    .header{ height: auto; min-height: 46px; background-position: center bottom; padding-bottom: 20px; }
  }

  .table{ display: table; table-layout: fixed; width: 100%; }
  .table-cell{ display: table-cell; vertical-align: middle; }

  /*col-1,.col-2,.col-3,.col-4,.col-5,.col-6,.col-7,.col-8,.col-9,.col-10,.col-11,.col-12,.col-margin,.col-half-container{ width: 100%; position:relative; top:0; float:left; box-sizing: border-box; padding: 0 10px;}*/
  [class*="col-"]{ width: 100%; position:relative; top:0; float:left; box-sizing: border-box; padding: 0 10px; margin-top: 10px;}
  .col-xs-1{width:8.33333%}
  .col-xs-2{width:16.66667%}
  .col-xs-3{width:25%}
  .col-xs-4{width:33.33333%}
  .col-xs-5{width:41.66667%}
  .col-xs-6{width:50%}
  .col-xs-7{width:58.33333%}
  .col-xs-8{width:66.66667%}
  .col-xs-9{width:75%}
  .col-xs-10{width:83.33333%}
  .col-xs-11{width:91.66667%}
  .col-xs-11b{width:98%}
  .col-xs-12{width:100%}
  .col-half-container{width:50%;}
  .col-1-5{width:20%; padding: 0 1%;}
  .col-1-10{width:10%; padding: 0 1%;}

  @media only screen and (min-width:928px) {
    .col-sm-1{width:8.33333%}
    .col-sm-2{width:16.66667%}
    .col-sm-3{width:25%}
    .col-sm-4{width:33.33333%}
    .col-sm-5{width:41.66667%}
    .col-sm-6{width:50%}
    .col-sm-7{width:58.33333%}
    .col-sm-8{width:66.66667%}
    .col-sm-9{width:75%}
    .col-sm-10{width:83.33333%}
    .col-sm-11{width:91.66667%}
    .col-sm-11b{width:98%}
    .col-sm-12{width:100%}
    .col-half-container{width:50%}
  }

  .number {font:normal 2.8em StarfallvBP_bold; width:50px; padding-top:15px; text-align:center;}

  h2.classicsf {font:normal 1.8em StarfallvBP_bold; color:#060; margin:15px 0 0 0;}

.classic { border-radius:4em; text-align:left; box-shadow:0 2px 2px rgba(0,0,0,.50); margin:1em 0px; padding: .5em; behavior: url(/css/PIE.htc); /* well-tested solution for adding border-radius to IE 6-9 */ }

  .classic img { margin:3px 10px 0 0; width:65px; border-radius:5px; box-shadow:0 2px 2px rgba(0,0,0,.50); }
  .classic .img-well { width: 75px; }

  .classic p{white-space:nowrap; height: 71px; width: 315px; margin-top:5px; border-radius:0 35px 35px 0; padding:0 10px; 	behavior: url(/css/PIE.htc); /* well-tested solution for adding border-radius to IE 6-9 */}

  .ABC {background:#C3C;color:#FCF;}

  .LTR {background:#390;color:#9F3;}

  .FTR {background:#30C;color:#69F;}

  .IR {background:#F90;color:#FF9;}

  .ABC p, .LTR p, .FTR p, .IR p {font:normal 3.6em StarfallvBP_bold; padding-top:.5em; width: 100%;}

  .ABC p {background:url(assets/images/BG-ABCs.png) repeat-x; color:#903;}

  .LTR p {background:url(assets/images/BG-LTR.png) repeat-x; color:#C00;}

  .FTR p {background:url(assets/images/BG-FTR.png) repeat-x; color:#30C;}

  .IR p {background:url(assets/images/BG-IR.png) repeat-x; color:#090;}

  .holidayicon { margin:5px 0 0; text-align:center;}

.holidayicon span { display: block; background:#39F url(assets/images/BG-holiday.png); background-size: cover; border-radius:5px; box-shadow:0 2px 2px rgba(0,0,0,.50); padding-top:2px; 	behavior: url(/css/PIE.htc); /* well-tested solution for adding border-radius to IE 6-9 */}

  .holidayicon img {width:90%; height:auto;}

  .more {background:url(assets/images/BG-transparentgreen.png); border-radius:20px; height:100%; padding:5px; text-align:center; 	behavior: url(/css/PIE.htc); /* well-tested solution for adding border-radius to IE 6-9 */}

  h1 {text-align:center; font:normal 3.2em 'DancingScript';color:#060; margin:7px 0 8px 0;}

  h2.more {margin:2px 0; padding:2px 0 0 0; font:normal 1.6em StarfallvBP_bold; color:#060;

      background:url(assets/images/BG-transparentgreen.png); border-radius:5px; 	behavior: url(/css/PIE.htc); /* well-tested solution for adding border-radius to IE 6-9 */}


  .icon{text-align:center;}

  .icon img{width:85%;margin:7.5%;border-radius:0.313em; box-shadow:0 2px 2px rgba(0,0,0,.50)}

  .icon-double img{width:85%;margin:3%;width:92.5%;border-radius:0.313em; box-shadow:0 2px 2px rgba(0,0,0,.50); 	behavior: url(/css/PIE.htc); /* well-tested solution for adding border-radius to IE 6-9 */}

  .noshadow img{box-shadow:none;}

  .footer{background:#97DBFF url(assets/images/BG-bluegradient.png) repeat-x;float:left; margin-top:15px; border-top:2px solid #06C; padding:35px 0;color:#005bc5;}
  .footer ul{
      text-align: center;
      width: 320px;
      padding: 0;
      height: 35px;
      margin: 0 auto;
      display: block;
      float: none;
      clear: both;
      white-space: nowrap;
  }

  .about {font:1em Georgia, "Times New Roman", Times, serif; float:none; clear:both; margin:15px 100px;}

  .about a {color:#005bc5; background:#b8eaff; border-radius:2px; padding: 0 3px; 	behavior: url(/css/PIE.htc); /* well-tested solution for adding border-radius to IE 6-9 */}

  .copyright {text-align:center;float:none; clear:both;font-size: 0.750em; color:#005bc5; opacity:.5;}

  .disabled, .disabled>div, .disabled img { filter: saturate(0%) contrast(.3) brightness(1.5) blur(0px); cursor: normal;}

  .btn {
    display: inline-block;
    padding: 6px 12px;
    margin-bottom: 0;
    font-size: 1.4em;
    font-weight: normal;
    line-height: 1.42857143;
    text-align: center;
    white-space: nowrap;
    vertical-align: middle;
    -ms-touch-action: manipulation;
        touch-action: manipulation;
    cursor: pointer;
    -webkit-user-select: none;
       -moz-user-select: none;
        -ms-user-select: none;
            user-select: none;
    background-image: none;
    border: 1px solid transparent;
    border-radius: 4px;
  }
  .btn:focus,
  .btn:active:focus,
  .btn.active:focus,
  .btn.focus,
  .btn:active.focus,
  .btn.active.focus {
    outline: 5px auto -webkit-focus-ring-color;
    outline-offset: -2px;
  }
  .btn:hover,
  .btn:focus,
  .btn.focus {
    color: #333;
    text-decoration: none;
  }
  .btn:active,
  .btn.active {
    background-image: none;
    outline: 0;
    -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, .125);
            box-shadow: inset 0 3px 5px rgba(0, 0, 0, .125);
  }
  .btn.disabled,
  .btn[disabled],
  fieldset[disabled] .btn {
    cursor: not-allowed;
    filter: alpha(opacity=65);
    -webkit-box-shadow: none;
            box-shadow: none;
    opacity: .65;
  }
  a.btn.disabled,
  fieldset[disabled] a.btn {
    pointer-events: none;
  }
  .btn-sm{ font-size: 1em; }
  .btn-default {
    color: #333;
    background-color: #fff;
    border-color: #ccc;
  }
  .btn-default:focus,
  .btn-default.focus {
    color: #333;
    background-color: #e6e6e6;
    border-color: #8c8c8c;
  }
  .btn-default:hover {
    color: #333;
    background-color: #e6e6e6;
    border-color: #adadad;
  }
  .btn-default:active,
  .btn-default.active,
  .open > .dropdown-toggle.btn-default {
    color: #333;
    background-color: #e6e6e6;
    border-color: #adadad;
  }
  .btn-default:active:hover,
  .btn-default.active:hover,
  .open > .dropdown-toggle.btn-default:hover,
  .btn-default:active:focus,
  .btn-default.active:focus,
  .open > .dropdown-toggle.btn-default:focus,
  .btn-default:active.focus,
  .btn-default.active.focus,
  .open > .dropdown-toggle.btn-default.focus {
    color: #333;
    background-color: #d4d4d4;
    border-color: #8c8c8c;
  }
  .btn-default:active,
  .btn-default.active,
  .open > .dropdown-toggle.btn-default {
    background-image: none;
  }
  .btn-default.disabled:hover,
  .btn-default[disabled]:hover,
  fieldset[disabled] .btn-default:hover,
  .btn-default.disabled:focus,
  .btn-default[disabled]:focus,
  fieldset[disabled] .btn-default:focus,
  .btn-default.disabled.focus,
  .btn-default[disabled].focus,
  fieldset[disabled] .btn-default.focus {
    background-color: #fff;
    border-color: #ccc;
  }
  .btn-default .badge {
    color: #fff;
    background-color: #333;
  }
  .btn-primary {
    color: #fff;
    background-color: #337ab7;
    border-color: #2e6da4;
  }
  .btn-primary:focus,
  .btn-primary.focus {
    color: #fff;
    background-color: #286090;
    border-color: #122b40;
  }
  .btn-primary:hover {
    color: #fff;
    background-color: #286090;
    border-color: #204d74;
  }
  .btn-primary:active,
  .btn-primary.active,
  .open > .dropdown-toggle.btn-primary {
    color: #fff;
    background-color: #286090;
    border-color: #204d74;
  }
  .btn-primary:active:hover,
  .btn-primary.active:hover,
  .open > .dropdown-toggle.btn-primary:hover,
  .btn-primary:active:focus,
  .btn-primary.active:focus,
  .open > .dropdown-toggle.btn-primary:focus,
  .btn-primary:active.focus,
  .btn-primary.active.focus,
  .open > .dropdown-toggle.btn-primary.focus {
    color: #fff;
    background-color: #204d74;
    border-color: #122b40;
  }
  .btn-primary:active,
  .btn-primary.active,
  .open > .dropdown-toggle.btn-primary {
    background-image: none;
  }
  .btn-primary.disabled:hover,
  .btn-primary[disabled]:hover,
  fieldset[disabled] .btn-primary:hover,
  .btn-primary.disabled:focus,
  .btn-primary[disabled]:focus,
  fieldset[disabled] .btn-primary:focus,
  .btn-primary.disabled.focus,
  .btn-primary[disabled].focus,
  fieldset[disabled] .btn-primary.focus {
    background-color: #337ab7;
    border-color: #2e6da4;
  }
  .btn-primary .badge {
    color: #337ab7;
    background-color: #fff;
  }
  .btn-success {
    color: #fff;
    background-color: #5cb85c;
    border-color: #4cae4c;
  }
  .btn-success:focus,
  .btn-success.focus {
    color: #fff;
    background-color: #449d44;
    border-color: #255625;
  }
  .btn-success:hover {
    color: #fff;
    background-color: #449d44;
    border-color: #398439;
  }
  .btn-success:active,
  .btn-success.active,
  .open > .dropdown-toggle.btn-success {
    color: #fff;
    background-color: #449d44;
    border-color: #398439;
  }
  .btn-success:active:hover,
  .btn-success.active:hover,
  .open > .dropdown-toggle.btn-success:hover,
  .btn-success:active:focus,
  .btn-success.active:focus,
  .open > .dropdown-toggle.btn-success:focus,
  .btn-success:active.focus,
  .btn-success.active.focus,
  .open > .dropdown-toggle.btn-success.focus {
    color: #fff;
    background-color: #398439;
    border-color: #255625;
  }
  .btn-success:active,
  .btn-success.active,
  .open > .dropdown-toggle.btn-success {
    background-image: none;
  }
  .btn-success.disabled:hover,
  .btn-success[disabled]:hover,
  fieldset[disabled] .btn-success:hover,
  .btn-success.disabled:focus,
  .btn-success[disabled]:focus,
  fieldset[disabled] .btn-success:focus,
  .btn-success.disabled.focus,
  .btn-success[disabled].focus,
  fieldset[disabled] .btn-success.focus {
    background-color: #5cb85c;
    border-color: #4cae4c;
  }
  .btn-success .badge {
    color: #5cb85c;
    background-color: #fff;
  }
  .btn-info {
    color: #fff;
    background-color: #5bc0de;
    border-color: #46b8da;
  }
  .btn-info:focus,
  .btn-info.focus {
    color: #fff;
    background-color: #31b0d5;
    border-color: #1b6d85;
  }
  .btn-info:hover {
    color: #fff;
    background-color: #31b0d5;
    border-color: #269abc;
  }
  .btn-info:active,
  .btn-info.active,
  .open > .dropdown-toggle.btn-info {
    color: #fff;
    background-color: #31b0d5;
    border-color: #269abc;
  }
  .btn-info:active:hover,
  .btn-info.active:hover,
  .open > .dropdown-toggle.btn-info:hover,
  .btn-info:active:focus,
  .btn-info.active:focus,
  .open > .dropdown-toggle.btn-info:focus,
  .btn-info:active.focus,
  .btn-info.active.focus,
  .open > .dropdown-toggle.btn-info.focus {
    color: #fff;
    background-color: #269abc;
    border-color: #1b6d85;
  }
  .btn-info:active,
  .btn-info.active,
  .open > .dropdown-toggle.btn-info {
    background-image: none;
  }
  .btn-info.disabled:hover,
  .btn-info[disabled]:hover,
  fieldset[disabled] .btn-info:hover,
  .btn-info.disabled:focus,
  .btn-info[disabled]:focus,
  fieldset[disabled] .btn-info:focus,
  .btn-info.disabled.focus,
  .btn-info[disabled].focus,
  fieldset[disabled] .btn-info.focus {
    background-color: #5bc0de;
    border-color: #46b8da;
  }
  .btn-info .badge {
    color: #5bc0de;
    background-color: #fff;
  }
  /* Portrait

  @media screen and (orientation:portrait) {

  .col-half-container{width:96% !important;}

  #col-left{float:none;}

  #col-right{float:none; margin-top:90px}
  .classic{width:100%;}
  .classic p {width:85% !important;}
  .holidayicon {left: 25%;position: relative;}
  } */
</style>

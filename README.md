# DoodiTabs
Tabs with jQuery

1- Create you tabs buttons or links list, --GIVE YOUR "CUSTOM-CLASS-LIST" TO DIV OF LIST--
<!-- START TABS LINK BUTTONS LIST -->
<div class="list-items">
<ul>
    <li><a href="#one">List one</a></li>
    <li><a href="#two">List two</a></li>
    <li><a href="#three">List three</a></li>
    <li><a href="#four">List four</a></li>
</ul>
</div>
<!-- END TABS LINK BUTTONS LIST -->

2- Create you main tabs content divs --GIVE YOUR "CUSTOM-CLASS-DIVS" TO EACH DIV--
<!-- START TABS MAIN CONTENT LIST -->
<div class="Main">
    <div class="main-inner active" id="one"><h1>This is Tab ONE</h1></div>
    <div class="main-inner" id="two"><h1>This is Tab TWO</h1></div>
    <div class="main-inner" id="three"><h1>This is Tab THREE</h1></div>
    <div class="main-inner" id="four"><h1>This is Tab FOUR</h1></div>
</div>
<!-- END TABS MAIN CONTENT LIST -->



3- Add jquery cdn or downloaded file.
4- Add this jquery Code.
<!-- START JQUERY -->


    

    $(document).ready(function(){

        /* TABS ON CLICK FUNCTION */
        $(".CUSTOM-CLASS-LIST ul li a").click(function(){
            var tabLink = $(this).attr("href");    // Getting the --href-- from tabs buttons
            var tabSlider = $(".CUSTOM-CLASS-DIVS").attr("id"); // Getting main content --ID--
            var tabSliderID = "#"+tabSlider;
            var showThisSlider = tabSliderID = tabLink; // Checking main content --ID-- == tab button --href--
            $(".CUSTOM-CLASS-DIVS").hide(); // Hiding all main content
            $(".CUSTOM-CLASS-DIVS"+showThisSlider).show(); // Showing matching main content == tab button clicked
        });

    });



<!-- END JQUERY -->

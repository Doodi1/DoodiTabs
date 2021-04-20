# DoodiTabs
Tabs with jQuery

1- Create you tabs buttons or links list
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

2- Create you main tabs content divs
<!-- START TABS MAIN CONTENT LIST -->
<div class="Main">
    <div class="main-inner active" id="one"><h1>This is Tab ONE</h1></div>
    <div class="main-inner" id="two"><h1>This is Tab TWO</h1></div>
    <div class="main-inner" id="three"><h1>This is Tab THREE</h1></div>
    <div class="main-inner" id="four"><h1>This is Tab FOUR</h1></div>
</div>
<!-- END TABS MAIN CONTENT LIST -->



3- Add jquery
4- Add this jquery Code


<!-- START JQUERY -->
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
<script>
    $(document).ready(function(){

        /* TABS ON CLICK FUNCTION */
        $(".list-items ul li a").click(function(){
            var tabLink = $(this).attr("href");    // Getting the --href-- from tabs buttons
            var tabSlider = $(".main-inner").attr("id"); // Getting main content --ID--
            var tabSliderID = "#"+tabSlider;
            var showThisSlider = tabSliderID = tabLink; // Checking main content --ID-- == tab button --href--
            $(".main-inner").hide(); // Hiding all main content
            $(".main-inner"+showThisSlider).show(); // Showing matching main content == tab button clicked
        });

    });
</script>
<!-- END JQUERY -->

# jquery-ui-droppable-iframe
##Use your droppable zones inside iframe!

[Demo page](http://maxazan.github.io/jquery-ui-droppable-iframe/)

Plugin features:

* Fix droppable position inside iframe
* You can use iframe scroll, while you are dragging
* After scroll droppable position works perfect
* Works even in IE and Edge
* You can use native scrollSensitivity and scrollSpeed params

##Installation
```
npm install jquery-ui-droppable-iframe
```
##Usage
```html
<!--jquery -->
<script type="text/javascript" src="js/jquery-1.11.3.min.js"></script>
<!--jquery UI -->
<script type="text/javascript" src="js/jquery-ui-1.11.4.custom.js"></script>
<!-- jquery-ui-droppable-iframe -->
<script type="text/javascript" src="jquery-ui-droppable-iframe.js"></script>    
<!--Activate drag and drop zones -->
<script type="text/javascript">
$(function() {
    //After frame loaded
    $("#testframe").attr('src','iframe.html').load(function() {
        //Activate droppable zones
        $(this).contents().find('.droppable').droppable({
            drop: function(event, ui) {
                //ACTION ON DROP HERE
            }
        });
    });

    //Activate draggable zones
    $('.draggable').draggable({
        iframeFix: true,    //Core jquery ui params needs for fix iframe bug
        iframeScroll: true  //This param needs for activate iframeScroll
    });

});
</script>
```

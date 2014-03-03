jquery
======

Nothing major just my sample codes

<form class="new" method="post" action="/jobs">
    <div id="dynamicInput">
        
    </div>
    <input type="button" value="+" onclick="addInput('dynamicInput');" />
    <input type="button" value="Save" />
</form>


var choices = ["one","two","three"];
//choices[0] = "one";
//choices[1] = "two";

var choices_a = '{"i_contains":"Contains (case insensitive)","i_not_contains":"Does not contain","contains":"Contains (case sensitive)","not_contains":"Does not contain","eq":"Equal to","neq":"Not Equal to","lt":"Less than","lte":"Less than or equal to","gt":"Greater than","gte":"Greater than or equal to"}';

var choices_b = '{"url":"Full url","domain":"Domain visited","path":"The path of the site visited (not including the domain)","event":"The name of the pixel event"}';

var result = $.parseJSON(choices_b);
var results = $.parseJSON(choices_a);
var inputfield = '<input type="text" name="name" />';


var select = $("<select/>");
$.each(results, function(a, b) {
    select.append($("<option/>").attr("value", a).text(b));
});
$("#dynamicInput").append(select);

var select = $("<select/>");
    $.each(result, function(a, b) {
        select.append($("<option/>").attr("value", a).text(b));
    });

$("#dynamicInput").append(select);
$("#dynamicInput").append(inputfield);

function addInput(divName) {
var select = $("<select/>");
      $.each(results, function(a, b) {
          select.append($("<option/>").attr("value", a).text(b));
      });
      $("#" + divName).append(select);
    $('#dynamicInput select:odd').attr("name", "data[]");

      var select = $("<select/>");
      $.each(result, function(a, b) {
          select.append($("<option/>").attr("value", a).text(b));
      });
      $("#" + divName).append(select);
       $("#" + divName).append(inputfield);

       $('#dynamicInput select').addClass('_uniformed u-input u-length-4  required _uniformed');
       $('#dynamicInput select:even').attr("name", "operators[]");
    
    
}

$('#dynamicInput input').last().attr("value", "Nanyon");



# esp2886_Project
This Code im sure has many errors..
Check for checked states should be initiated on click if clicked element is currently unchecked. Then followed by intended state update. Otherwise inserted code  may
result in inability to uncheck state. 

Basic javascript to check all checkboxes and get states is

for (i = 1; i<3; i++) {
  document.getElementById('lang_'+i).checked = true;

#do stuff here
}

Added to function toggleCheckbox
  <!--  Inserted bits attempting to set all states to off -->	
	if(element.unchecked)
	{
  var xhr = new XMLHttpRequest();
		for (i = 1; i<=NUM_RELAYS; i++) {
		document.getElementById(i).checked = true;
		xhr.open("GET", "/update?relay="+element.id+"&state=0", true); }
		xhr.send();
		}
	}
  <!--------------------------- -->

element id may be incorret as I may be incorrectly reading the id from the custom webcode. 
Assuming it works I may have the update state inverted and should be 1. 


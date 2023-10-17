# wedzardry-journal
Just a Webzardry Journal

📺 Content Rendering 📺

Server Side 
    VS 
Client Side

    Server Side :
        Server Builds Up The Web Page Then Sends To Client
        +   less work on the client side
        -   cant hide data in javascript memory

    Client Side :
        Some Parts of the server gets sent initially then it keeps asking for more
        -   a lot more work on the client side
        -   a lot more work on the server side
        +   can hide data in javascript memory by using anonymous functions


🤏 DOM Manipulation 🤏

document.querySelectorAll()
    vs
JQuery() or $()

    document.querySelectorALL() :
        Returns an array of the selected elements
        + Built in most of the popular modern browsers
        - a whole lot longer to type

    JQuery() or $() :
        Returns an array of selected elements wrapped in a javascript object
        + Needs an additional File
        - a whole lot shorter with shorten functions too

    Additional Info : 
	JQuery Offers a Minimal Version That Does Not Include Things Like Ajax
        There is a library that is much more lighter than Mininal JQuery Called
        Cash JS
	

* Identifying elements *

class and id vs data-*

	> use class and id for css queries only
	> use data-* for javascript queries
	
	> example for js queries :
   		<input data-* type="text"/>
	    document.querySelector("[data-*]");	

🚌 The fetch() API 🚌

    let formData = new FormData();
    formData.append('key', 'value');
    fetch('models/model.php', {
        method: 'POST',
        body: formData
    })
    .then(response => response.json())
    .then(results => {
        console.log('Success:', results);
    })
    .catch(error => {
        console.error('Error:', error);
    });


☢ The fetch() API For LARAVEL - JS Side ☢

    let formData = new FormData();
    formData.append("somekey","somevalue");
    fetch("{{ route('work.store') }}", {
        method: 'POST',
        body: formData,
        headers: { 'X-CSRF-TOKEN': document.querySelector('input[name="_token"]').value}
    })
    .then(response => response.json())
    .then(results => {
        console.log('Success:', results);
    })
    .catch(error => {
        console.error('Error:', error);
    });
    
☢ The fetch() API For LARAVEL - PHP Side ☢

    return response(["data"=>$_POST], 200)->header('Content-Type', 'application/json');

☄ Lambda - Creating and Running a lambda Function ☄

	(()=>{})();

⚠ The event for the option element issue ⚠

    adding event handlers on <option> works on firefox
    but does not work on chromes engine

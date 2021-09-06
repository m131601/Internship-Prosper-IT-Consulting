# Live Project
## Introduction

For the last two weeks of my time at The Tech Academy. I worked with my peers in a team developing a Web Site in HTML, CSS and JavaScript. It was a great learning experience to work in Azure DevOps as a team. I had daily standups with the Project Manager and also a weekly Sprint retrospective. I worked on several front end stories that I am proud of. Everyone on the team had a chance to owrk on front end stories and some also did back end stories. Over the two week sprint I had the opportunity to work with Project Management with my programming skills that I will be able to use again in the future on future projects.

Below are descriptions some of the stories I worked on along with code snippets.

## Modal

I use Bootstrap to create the modal and added a form in the modal that allowed the user to input information. I subscribed to formspree.io so that information that is entered in the form will come to my destinated email.
	

    <style>
    /* set a style for all buttons*/
	button {
		background-color: rgb(128, 0, 79);
		color: white;
		padding: 14px 20px;
		margin: 8px 0;
		cursor: pointer;
		width: 100%;
	}
    /*define the modal’s background*/
	
	.modal {
		display: none;
		position: fixed;
		z-index: 1;
		left: 0;
		top: 0;
		width: 100%;
		height: 100%;
		overflow: auto;
		background-color: rgb(0, 0, 0);
		background-color: rgba(0, 0, 0, 0.4);
		padding-top: 60px;
	}
	/*define the modal-content background*/
	
	.modal-content {
		background-color: #fefefe;
		margin: 5% auto 15% auto;
		border: 1px solid #888;
		width: 80%;
	}
	/*define the close button*/
	
  	</style>    
      	<!-- Modal with formspree.io-->
          <script src="https://formspree.io/js/formbutton-v1.min.js" defer></script>
          <script>
            window.formbutton=window.formbutton||function(){(formbutton.q=formbutton.q||[]).push(arguments)};
            formbutton("create", {action: "https://formspree.io/f/xleaabvz"})
          </script>


## Top to Bottom Button

I created a button that when the user reaches the bottom of the page when clicked on it will take them to the top of the page. 

     <div id="bottom-button" class="d-none">
        <button class="btn btn-secondary btn-lg" onclick="toTop()">Back To Top</button>
    </div>

    <div id="bottom-button-mobile" class="d-none d-sm-none">
        <button class="btn btn-secondary btn" onclick="toTop()">Back To Top</button>
    </div>


//Back to Top

	window.onscroll = function() {
  	var myButton = document.getElementById("bottom-button");
  	var myButtonMoblie = document.getElementById("bottom-button-mobile");
  	if ((window.innerHeight + window.pageYOffset) >= document.body.offsetHeight - 100) {                            
      	myButton.classList.add('d-md-block');
      	myButton.classList.add('fade-in');
      	myButtonMoblie.classList.add('fade-in');
      	myButtonMoblie.classList.add('d-block');
     	myButtonMoblie.classList.remove('d-none');
  	} else {
      	myButton.classList.remove('fade-in');
      	myButton.classList.remove('d-md-block');
      	myButtonMoblie.classList.remove('fade-in');
      	myButtonMoblie.classList.remove('d-block');
      	myButtonMoblie.classList.add('d-none');
  	}
	}

	function toTop(){
  	window.scrollTo(0,0);
	}


	#bottom-button{
    	position: fixed;
    	bottom: 2vh;
	right: 2vw;
	}

	#bottom-button-mobile{
    	position: fixed;
    	bottom: 2vh;
    	left: 2vw;
	}

	.fade-in{
    	animation: fadeIn 3s;
    	-webkit-animation: fadeIn 3s;
    	-moz-animation: fadeIn 3s;
    	-o-animation: fadeIn 3s;
    	-ms-animation: fadeIn 3s;
	}

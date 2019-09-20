# Katsiaryna Zhdanovich

### Contacts:
* +375 29 88 98 621
* [Mail](mailto:zhdanovichkat@gmail.com)
* [Linkedin](https://www.linkedin.com/in/katsiaryna-zhdanovich/)

### Summary:
I can identify myself as being capable of *studying quickly*, *highly-motivated* and *responsible*. I like being challenged and engaged in projects that require me to work outside my comfort and knowledge set, as continuing to learn new development techniques are important to me.
My goal is to learn as much as possible in the sphere of front-end development and to become a _specialist_ in the chosen field.
And I do my best to achieve my goal.

### Skills:
* HTML;
* CSS;
* JS;
* Bootstrap;
* jQuery;
* AJAX;
* English, B2.

### Quiz - the last project, I've made:
```HTML
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Quiz</title>
        <style type="text/css">
			.quiz-window {
				width: 400px;
				min-height: 70px;
				border: dotted black 5px;
				border-radius: 15px;
				text-align: center;
				font-size: 20px;
				margin: 0 auto;
			}
			button {
				width: auto;
				margin: 0 auto;
			}
			.quiz-window div {
				margin: 20px;
			}
			#option1,#option2,#option3,#option4 {
				display:none;
				margin-bottom: 10px;
			}

			@media only all and (max-width: 550px) {
				.quiz-window {
					width: 200px;
					font-size: 10px;
					height: auto;
				}
				button {
					font-size: 10px;
				}
				.quiz-window div {
					margin: 10px;
				}
			}
		</style>
	</head>
	<body>
		<div class="quiz-window">			
			<div><p id="result"></p></div>
			<div><p id="question"></p></div>
			<button onclick="prove(1)" class="text" id="option1"></button>
			<button onclick="prove(2)" class="text" id="option2"></button>
			<button onclick="prove(3)" class="text" id="option3"></button>
			<button onclick="prove(4)" class="text" id="option4"></button>
			<button id="start" class="text" onclick="prove(0)">Start the quiz</button>
		</div>

		<script type="text/javascript">

			var quiz_arr = [
				["How many continents are there on th Earth?","6","3","7","10",3],
				["133-2*12 =","220","209","199","100",2],
				["How many oceans are there on the Earth?  ","4","5","6","7",1],
			];

			var score = 0;
			var cur_answer = 0;
			var number_of_questions = quiz_arr.length;

			function prove(answer){

				if(answer == 0){ 

					document.getElementById('option1').style.display='block';
					document.getElementById('option2').style.display='block';
					document.getElementById('option3').style.display='block';
					document.getElementById('option4').style.display='block';
					document.getElementById('question').style.display='block';

					document.getElementById('option1').innerHTML=quiz_arr[cur_answer][1];
					document.getElementById('option2').innerHTML=quiz_arr[cur_answer][2];
					document.getElementById('option3').innerHTML=quiz_arr[cur_answer][3];
					document.getElementById('option4').innerHTML=quiz_arr[cur_answer][4];
					document.getElementById('question').innerHTML=quiz_arr[cur_answer][0];

					document.getElementById('start').style.display='none';

				}else{

					if( answer ==  quiz_arr[cur_answer][5]){
						score++;
						document.getElementById('result').innerHTML='Correct!';

					}else{

						document.getElementById('result').innerHTML="Incorrect! Right answer: " + quiz_arr[cur_answer][quiz_arr[cur_answer][5]];
						}

					cur_answer++;
					if(cur_answer < number_of_questions){

						document.getElementById('option1').innerHTML=quiz_arr[cur_answer][1];
						document.getElementById('option2').innerHTML=quiz_arr[cur_answer][2];
						document.getElementById('option3').innerHTML=quiz_arr[cur_answer][3];
						document.getElementById('option4').innerHTML=quiz_arr[cur_answer][4];
						document.getElementById('question').innerHTML=quiz_arr[cur_answer][0];

					}else{

						document.getElementById('option1').style.display='none';
						document.getElementById('option2').style.display='none';
						document.getElementById('option3').style.display='none';
						document.getElementById('option4').style.display='none';
						document.getElementById('question').style.display='none';
						
						var percent =  Math.round(score/number_of_questions*100);				
						var res = 'Bad!';
						if(percent>65) res = 'Good!';
						if(percent==100) res = 'Excellent!';

						document.getElementById('result').innerHTML='Right answers: ' + score + ' out of ' + number_of_questions + ' (' + percent + '%)<br>' + res;
					}
				}
			}
		</script>
	</body>
</html>
```

### Experience:
* Course Project - BOOM;
* University Labs' Tasks;
* Quiz Project;

### Education
* Belarusian State University of Informatics and Radioelectronics, 2015-2019, Faculty of Engineering and Economics;
* IT-Academy, 2019, "Websites development using HTML, CSS and JavaScript";
* Codecademy, 2019, "Introduction to HTML";
* Codecademy, 2019, "Learn CSS";
* Skyeng, 2019, "General Upper-Intermediate";
* Goethe-Istitut, 2015-2019, "A1-B2 German Language".

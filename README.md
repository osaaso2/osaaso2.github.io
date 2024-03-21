# osaaso2.github.io
<html>
<head>
<script type="text/javascript">
window.onload = function () {
    var chart = new CanvasJS.Chart("chartContainer");

    chart.options.axisY = { prefix: "$", suffix: "K" };
    chart.options.title = { text: "CelSci Views $ Duration" };

    var series1 = { //dataSeries - first quarter
        type: "column",
        name: "Views",
        showInLegend: true
    };

    var series2 = { //dataSeries - second quarter
        type: "column",
        name: "Duration",
        showInLegend: true
    };

    chart.options.data = [];
    chart.options.data.push(series1);
    chart.options.data.push(series2);


    series1.dataPoints = [
            { label: "Video 1", y: 58 },
            { label: "Video 2", y: 69 },
            { label: "Video 3", y: 80 },
            { label: "Video 4", y: 74 },
            { label: "Video 5", y: 64 }
    ];

    series2.dataPoints = [
        { label: "Video 1", y: 63 },
        { label: "Video 2", y: 73 },
        { label: "Video 3", y: 88 },
        { label: "Video 4", y: 77 },
        { label: "Video 5", y: 60 }
    ];

    chart.render();
}
</script>
<script type="text/javascript" src="https://cdn.canvasjs.com/canvasjs.min.js"></script>
</head>

<body>
    <div id="chartContainer" style="height: 300px; width: 100%;">
    </div>
</body>
</html>
<html>
	<head>
      <script type="module">
  import { pipeline } from 'https://cdn.jsdelivr.net/npm/@xenova/transformers@2.7.0';

</script>
		<button id="run">Gen</button>
    <h3>Output:</h3>
    
    <div id="output2">None</div>
	</head>
	<body> 
    
      <script type="module">
   import { pipeline, env } from 'https://cdn.jsdelivr.net/npm/@xenova/transformers@2.7.0'; 
        
    const generate = document.getElementById("run");   
    generate.addEventListener("click", async () =>{
        try {
         
env.useBrowserCache=false;
env.allowLocalModels=false;

let pipe = await pipeline('text-classification');

let output = await pipe('When life gives us difficult situations, how do we deal with them? This is the question that Nathaniel Drew attempts to tackle with this video, and through his journey to Vienna he uncovers some key concepts that work toward an answer to this question. The uncertainty that exists in the world, especially now, is something that can make us indecisive and unsure of our role in it all. Yet by keeping some key ideas in mind, it is possible to navigate this landscape. Firstly, the challenges we encounter are there to teach us. There are times when we must change,and the problems are there to guide us along the way. It is equally important to know your friends, and who you can rely on. When things get serious, it becomes clear who you can trust. In addition, everyone goes through certain phases of life that are always shifting. It is critical to find goals that align with where you are in the present moment. Another element to consider is the objective lack of control that we have on events external to us. By focusing on what we can control, we make the largest impact. Lastly, approaching each situation and experience with openness and curiosity allows for a better outlook, and inspires us to look forward instead of backward.');
output2.textContent = JSON.stringify(output);            
            } catch (error){
                 console.log("Error:",error.message);       
            }   
        }       
)

    </script>
    </body>
</html>
<iframe src="https://sohrabia.github.io"></iframe>
<head>
<html>
   <title>Your Name</title>
	<h3>Your CelSci</h3>
	<head>
		<script type="module" crossorigin src="https://cdn.jsdelivr.net/npm/@gradio/lite/dist/lite.js"></script>
	</head>
	<body>
		<gradio-lite>
			import gradio as gr
			import pandas as pd
			def show_df(as1,as2,as3):
				 df = pd.DataFrame({
					  "Videos" : ["Video 1", "Video 2", "Video 3", "Video 4", "Video 5"], 
					  "Views" : [500, 2000, 540, 300, 200], 
					  "Duration" : [30, 20, 70, 35, 22]})
				 print(as1)
				 df = df.style.highlight_max(color = 'lightgreen', axis = 0)
				 return df
			with gr.Blocks() as demo:
				with gr.Row():
					with gr.Column():
						data = gr.Dataframe()
						demo.load(show_df, None, [data])
			demo.launch()
		</gradio-lite>
	</body>
</html>
<html>
	<head>
		<script type="module" src="https://cdn.jsdelivr.net/npm/@gradio/lite/dist/lite.js"></script>
	</head>
	<body>
		<gradio-lite>
		import gradio as gr
		def fn1(txt1):
			return txt1+"hey"
		gr.Interface(fn1,"text","text").launch()
		</gradio-lite>
	</body>
</html>


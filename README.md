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

<iframe src="https://sohrabia.github.io"></iframe>


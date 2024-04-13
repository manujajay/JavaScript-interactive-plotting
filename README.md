# Interactive and Advanced Charting with JavaScript Libraries

This README provides detailed instructions and code samples for creating interactive and advanced charts using popular JavaScript libraries such as Chart.js, D3.js, and Highcharts.

## 1. Chart.js

Chart.js is a simple yet flexible charting library for designers and developers. It is easy to use and includes a variety of chart types.

### Sample: Line Chart

```html
<!DOCTYPE html>
<html>
<head>
    <title>Chart.js Sample</title>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
</head>
<body>
    <canvas id="myChart" width="400" height="400"></canvas>
    <script>
        var ctx = document.getElementById('myChart').getContext('2d');
        var myChart = new Chart(ctx, {
            type: 'line',
            data: {
                labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
                datasets: [{
                    label: '# of Votes',
                    data: [12, 19, 3, 5, 2, 3],
                    backgroundColor: 'rgba(255, 99, 132, 0.2)',
                    borderColor: 'rgba(255, 99, 132, 1)',
                    borderWidth: 1
                }]
            },
            options: {
                scales: {
                    y: {
                        beginAtZero: true
                    }
                }
            }
        });
    </script>
</body>
</html>
```

## 2. D3.js

D3.js is a powerful library for producing dynamic, interactive data visualizations in web browsers. It supports complex visualizations and large datasets.

### Sample: Dynamic Bar Chart

```html
<!DOCTYPE html>
<html>
<head>
    <title>D3.js Sample</title>
    <script src="https://d3js.org/d3.v6.min.js"></script>
</head>
<body>
    <svg width="500" height="500"></svg>
    <script>
        const data = [30, 86, 168, 281, 303, 365];
        const svg = d3.select("svg");
        svg.selectAll("rect")
            .data(data)
            .enter().append("rect")
            .attr("width", (d) => d)
            .attr("height", 50)
            .attr("y", (d, i) => i * 60)
            .attr("fill", "steelblue");
    </script>
</body>
</html>
```

## 3. Highcharts

Highcharts is a charting library written in pure JavaScript, offering an easy way of adding interactive charts to your web site or web application.

### Sample: 3D Chart

```html
<!DOCTYPE html>
<html>
<head>
    <title>Highcharts Sample</title>
    <script src="https://code.highcharts.com/highcharts.js"></script>
    <script src="https://code.highcharts.com/highcharts-3d.js"></script>
</head>
<body>
    <div id="container" style="height: 400px"></div>
    <script>
        Highcharts.chart('container', {
            chart: {
                type: 'column',
                options3d: {
                    enabled: true,
                    alpha: 15,
                    beta: 15,
                    depth: 50
                }
            },
            series: [{
                data: [29.9, 71.5, 106.4, 129.2, 144.0, 176.0]
            }]
        });
    </script>
</body>
</html>
```

## Conclusion

These examples demonstrate how to use JavaScript libraries for creating a variety of interactive and advanced charts. Each library offers unique features and customization options to cater to different visualization needs.

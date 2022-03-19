<?php

?>

<head>

<title>Calendar</title>

<link rel="stylesheet" href="calendar.css" type="text/css">

</head>

<body>

<div class="container">

<h1>Bruin Family Schedule for Wed, September 18, 2019, 10:50 pm </h1>

<table id="event_table">
       <tr>
         
        <th class='table_header'>Cynthia</th> 
        <th class='table_header'>Sandra</th>
        <th class='table_header'>Meggy</th>
       </tr> <br>

<?php

function get_hour_string($time){
$hour_string = "";
$hour = date("h",$time);
$ampm = date("a",$time);
$hour_string = "$hour:00$ampm";
return $hour_string;
}
$hours_to_show = 12;
$timestamp = time();
for($row = 0; $row <= $hours_to_show; $row++)
{
echo "<tr class=";
if ($row % 2 == 0)
echo '"even_row">';
else echo '"odd_row">';
echo '<td class="hr_td">'. get_hour_string($timestamp) . "</td>";
echo "<td></td>";
echo "<td></td>";
echo "<td></td>";
echo "</tr>";
$timestamp += 60 * 60;
}
?>

</table>

</div>

</body>
</html>
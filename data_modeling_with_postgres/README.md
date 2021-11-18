## Discuss the purpose of this database in the context of the startup, Sparkify, and their analytical goals.

Sparkify is a startup that wants to analyze song and user activity data collected from their new music streaming app. Their analytics team is especially interested in understanding the songs users are listening to. The desired data is stored in JSON log files within the app.

## State and justify your database schema design and ETL pipeline.

The database uses a star schema design optimized for queries on song play analysis. The ETL pipeline reads data from the two app directories and efficiently and accurately processes the data into the database tables.

## [Optional] Provide example queries and results for song play analysis.

	SELECT * FROM songplays LIMIT 5;

<table>
<tbody><tr>
	<th>songplay_id</th>
	<th>start_time</th>
	<th>user_id</th>
	<th>level</th>
	<th>song_id</th>
	<th>artist_id</th>
	<th>session_id</th>
	<th>location</th>
	<th>user_agent</th>
</tr>
<tr>
	<td>1</td>
	<td>2018-11-30 00:22:07.796000</td>
	<td>91</td>
	<td>free</td>
	<td>None</td>
	<td>None</td>
	<td>829</td>
	<td>Dallas-Fort Worth-Arlington, TX</td>
	<td>Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.2; WOW64; Trident/6.0)</td>
</tr>
<tr>
	<td>2</td>
	<td>2018-11-30 01:08:41.796000</td>
	<td>73</td>
	<td>paid</td>
	<td>None</td>
	<td>None</td>
	<td>1049</td>
	<td>Tampa-St. Petersburg-Clearwater, FL</td>
	<td>"Mozilla/5.0 (Macintosh; Intel Mac OS X 10_9_4) AppleWebKit/537.78.2 (KHTML, like Gecko) Version/7.0.6 Safari/537.78.2"</td>
</tr>
<tr>
	<td>3</td>
	<td>2018-11-30 01:12:48.796000</td>
	<td>73</td>
	<td>paid</td>
	<td>None</td>
	<td>None</td>
	<td>1049</td>
	<td>Tampa-St. Petersburg-Clearwater, FL</td>
	<td>"Mozilla/5.0 (Macintosh; Intel Mac OS X 10_9_4) AppleWebKit/537.78.2 (KHTML, like Gecko) Version/7.0.6 Safari/537.78.2"</td>
</tr>
<tr>
	<td>4</td>
	<td>2018-11-30 01:17:05.796000</td>
	<td>73</td>
	<td>paid</td>
	<td>None</td>
	<td>None</td>
	<td>1049</td>
	<td>Tampa-St. Petersburg-Clearwater, FL</td>
	<td>"Mozilla/5.0 (Macintosh; Intel Mac OS X 10_9_4) AppleWebKit/537.78.2 (KHTML, like Gecko) Version/7.0.6 Safari/537.78.2"</td>
</tr>
<tr>
	<td>5</td>
	<td>2018-11-30 01:20:56.796000</td>
	<td>73</td>
	<td>paid</td>
	<td>None</td>
	<td>None</td>
	<td>1049</td>
	<td>Tampa-St. Petersburg-Clearwater, FL</td>
	<td>"Mozilla/5.0 (Macintosh; Intel Mac OS X 10_9_4) AppleWebKit/537.78.2 (KHTML, like Gecko) Version/7.0.6 Safari/537.78.2"</td>
</tr>
</tbody></table>
	
	SELECT * FROM users LIMIT 5;
	
<table>
<tbody><tr>
	<th>user_id</th>
	<th>first_name</th>
	<th>last_name</th>
	<th>gender</th>
	<th>level</th>
</tr>
<tr>
	<td>92</td>
	<td>Ryann</td>
	<td>Smith</td>
	<td>F</td>
	<td>free</td>
</tr>
<tr>
	<td>78</td>
	<td>Chloe</td>
	<td>Roth</td>
	<td>F</td>
	<td>free</td>
</tr>
<tr>
	<td>73</td>
	<td>Jacob</td>
	<td>Klein</td>
	<td>M</td>
	<td>paid</td>
</tr>
<tr>
	<td>12</td>
	<td>Austin</td>
	<td>Rosales</td>
	<td>M</td>
	<td>free</td>
</tr>
<tr>
	<td>86</td>
	<td>Aiden</td>
	<td>Hess</td>
	<td>M</td>
	<td>free</td>
</tr>
</tbody></table>
	
	SELECT * FROM songs LIMIT 5;
	
<table>
<tbody><tr>
	<th>user_id</th>
	<th>first_name</th>
	<th>last_name</th>
	<th>gender</th>
	<th>level</th>
</tr>
<tr>
	<td>92</td>
	<td>Ryann</td>
	<td>Smith</td>
	<td>F</td>
	<td>free</td>
</tr>
<tr>
	<td>78</td>
	<td>Chloe</td>
	<td>Roth</td>
	<td>F</td>
	<td>free</td>
</tr>
<tr>
	<td>73</td>
	<td>Jacob</td>
	<td>Klein</td>
	<td>M</td>
	<td>paid</td>
</tr>
<tr>
	<td>12</td>
	<td>Austin</td>
	<td>Rosales</td>
	<td>M</td>
	<td>free</td>
</tr>
<tr>
	<td>86</td>
	<td>Aiden</td>
	<td>Hess</td>
	<td>M</td>
	<td>free</td>
</tr>
</tbody></table>

	
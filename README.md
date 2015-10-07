#Tunisia jQuery Vector MAP
![JQVMap](http://jqvmap.com/img/logo.png "JQVMap")

This project is based on [JQVMap](https://github.com/manifestinteractive/jqvmap). So you can have a full documentation at their git repository.

This project is only for the Tunisia Regions MAP

Preview
======
<img src="http://medhossam.github.io/Tunisia-jQuery-Vector-MAP/preview.jpg"/>

Feel free to try the map [HERE](http://medhossam.github.io/Tunisia-jQuery-Vector-MAP/).

How To Use
======

To get started, all you need to do is include the JavaScript and CSS files for the map you want to load.  Here is a sample HTML page for loading the World Map with default settings:

	<html lang="en">
		<head>
			<title>Tunisia jQuery Vector MAP</title>
			<link href="css/jqvmap.css" media="screen" rel="stylesheet" type="text/css" />
			<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.7.2/jquery.min.js" type="text/javascript"></script>
			<script src="js/jquery.vmap.min.js" type="text/javascript"></script>
			<script src="js/maps/jquery.vmap.tunisia.min.js" type="text/javascript" charset="utf-8"></script>

			<script type="text/javascript">
				jQuery(document).ready(function() {
					jQuery('#jqvmap').vectorMap({ map: 'tn_regions_fr' });
				});
			</script>
		</head>
		
		<body>
			<div id="jqvmap" style="width:600px;height:400px;"></div>
		</body>
	</html>


Making it Pretty
======

While initializing a map you can provide parameters to change its look and feel.

	jQuery('#vmap').vectorMap({
		map: 'tn_regions_fr',
		backgroundColor: '#7EA4D0',
		borderColor: '#818181',
		borderOpacity: 0.75,
		borderWidth: 1,
		color: '#f4f3f0',
		enableZoom: true,
		hoverColor: '#C9DFAF',
		hoverOpacity: null,
		normalizeFunction: 'linear',
		scaleColors: ['#b6d6ff', '#005ace'],
		selectedColor: '#C9DFAF',
		selectedRegion: null,
		showTooltip: true,
		onRegionClick: function(element, code, region) {
			var msg = 'You clicked "'
				+ region 
				+ '" which has the code: '
				+ code.toUpperCase();

			alert(msg);
		}
	});

Configuration Settings
------

**map** *'tn_regions_fr'*

The Map you want to load. Must include the javascript file with the name of the map you want. 
There are many maps available with this library, but in this project the only map available is 'tn_regions_fr', 
it will be other libraries available in other languages. (e.g. tn_regions_ar, tn_regions_en, etc.)

**backgroundColor** *'#7EA4D0'*

Background color of map container in any CSS compatible format.

**borderColor** *'#818181'*

Border Color to use to outline map objects

**borderOpacity** *0.75*

Border Opacity to use to outline map objects ( use anything from 0-1, e.g. 0.5, defaults is 0.25 )

**borderWidth** *3*

Border Width to use to outline map objects ( defaults to 1 )

**color** *'#f4f3f0'*

Color of map regions.

**colors**

Colors of individual map regions. Keys of the colors objects are country codes according to ISO 3166-1 alpha-2 standard. Keys of colors must be in lower case.

**enableZoom** *boolean*

Whether to Enable Map Zoom ( true or false, defaults is true)

**hoverColor** *'#C9DFAF'*

Color of the region when mouse pointer is over it.

**hoverOpacity** *0.5*

Opacity of the region when mouse pointer is over it.

**normalizeFunction** *'linear'*

This function can be used to improve results of visualizations for data with non-linear nature. Function gets raw value as the first parameter and should return value which will be used in calculations of color, with which particular region will be painted.

**scaleColors** *['#b6d6ff', '#005ace']*

This option defines colors, with which regions will be painted when you set option values. Array scaleColors can have more then two elements. Elements should be strings representing colors in RGB hex format.

**selectedRegion** *'TN-TN'*

This is the Region that you are looking to have preselected ( 'TN-' suffixed with two letters ISO code, defaults is null )

	TUNISIA
	------------------------------
	TN-AR = Ariana
	TN-BE = Béja
	TN-BA = Ben Arous
	TN-BI = Bizerte
	TN-GB = Gabès
	TN-GF = Gafsa
	TN-JN = Jendouba
	TN-KR = Kairouan
	TN-KS = Kasserine
	TN-KE = Kébili
	TN-KF = El Kéf
	TN-MH = Mahdia
	TN-MN = La Manouba
	TN-MD = Médenine
	TN-MS = Monastir
	TN-NA = Nabeul
	TN-SF = Sfax
	TN-SB = Sidi Bouzid
	TN-SI = Siliana
	TN-SO = Sousse
	TN-TT = Tataouine
	TN-TZ = Tozeur
	TN-TN = Tunis
	TN-ZG = Zaghouan
	
**showTooltip** *boolean*

Whether to show Tooltips on Mouseover ( true or false, defaults is true)

**onLabelShow** *function(event, label, code)*

Callback function which will be called before label is shown. Label DOM object and country code will be passed to the callback as arguments.

**onRegionOver** *function(event, code, region)*

Callback function which will be called when the mouse cursor enters the region path. Country code will be passed to the callback as argument.

**onRegionOut** *function(event, code, region)*

Callback function which will be called when the mouse cursor leaves the region path. Country code will be passed to the callback as argument.

**onRegionClick** *function(event, code, region)*

Callback function which will be called when the user clicks the region path. Country code will be passed to the callback as argument. This callback may be called while the user is moving the map. If you need to distinguish between a "real" click and a click resulting from moving the map, you can inspect **$(event.currentTarget).data('mapObject').isMoving**.

#Copyright

All code in this Github Repository are available under both the MIT and GPL license

Copyright © 2015 CreaGen (Creative Generation)

See [Tunisia Map LICENSE](https://github.com/MedHossam/Tunisia-jQuery-Vector-MAP/blob/gh-pages/LICENSE.md) for details.

See [jQVMap LICENSE](https://github.com/manifestinteractive/jqvmap/blob/stable/LICENSE) for details.
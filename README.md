# jquery-input-switch
jQuery toggle switch input component

## Installation

```bash 
npm install @netliva/jquery-input-switch 
```

or

```bash 
yarn add @netliva/jquery-input-switch
```

## Add to project
 
if you are use yarn import package your project

```javascript
// add your script file
import '@netliva/jquery-input-switch'
```

or add inline 

```html
<!-- add base html file -->
<script src="/node_modules/@netliva/jquery-input-switch/src/js/netliva_switch.js"></script>
<link rel="stylesheet" href="/node_modules/@netliva/jquery-input-switch/src/css/netliva_switch.css">
```

## Usage

#### Basic Usage
![Basic Usage](https://github.com/netliva/jquery-input-switch/blob/master/readme_assets/01.png?raw=true)
```html
<input type="checkbox" netliva-switch />
<input type="checkbox" netliva-switch checked />
```

#### Mini Usage
![Mini Usage](https://github.com/netliva/jquery-input-switch/blob/master/readme_assets/02.png?raw=true)
```html
<input type="checkbox" netliva-switch data-size="mini" />
<input type="checkbox" netliva-switch data-size="mini" checked />
```

#### Change Text And Color
![Change Text And Color](https://github.com/netliva/jquery-input-switch/blob/master/readme_assets/03.png?raw=true)
![Change Text And Color Mini Usage](https://github.com/netliva/jquery-input-switch/blob/master/readme_assets/04.png?raw=true)
```html
<input type="checkbox"
       netliva-switch
       data-active-text="Yes "
       data-passive-text="No"
       data-active-color="#0A0"
       data-passive-color="#C00"
/>
<input type="checkbox"
       netliva-switch
       data-size="mini"
       data-active-text="On"
       data-passive-text="Off"
       data-active-color="#0A0"
       data-passive-color="#C00"
       checked
/>
```

If you use bootstrapp or color css variable, you can use variable name for color

![Change Color With Variable](https://github.com/netliva/jquery-input-switch/blob/master/readme_assets/06.png?raw=true)
```html
<input type="checkbox"
       netliva-switch
       data-active-color="info"
       data-passive-color="danger"
/>
```

#### Disabled Usage
![Mini Usage](https://github.com/netliva/jquery-input-switch/blob/master/readme_assets/05.png?raw=true)
```html
<input type="checkbox"
       netliva-switch
       data-active-color="#0A0"
       data-passive-color="#C00"
       disabled
/>
```

#### Javascript Usage
```html
<input id="example-input" type="checkbox" />
<script type="text/javascript">
	jQuery(function ($){
		$("#example-input").netlivaSwitch({
			'size': 'mini',
			'active-text': 'On',
			'passive-text': 'Off',
			'active-color': '#0f9983',
			'passive-color': '#ba1c00',
			'width' : '100px'
		});
	});
</script>
```

## Options
### Get State and Set State 
```html
<input id="example-input" type="checkbox" netliva-switch />
<script type="text/javascript">
	jQuery(function ($){
		$("#example-input").netlivaSwitch('state'); // return false
		$("#example-input").netlivaSwitch('state', true); // switch to active
		$("#example-input").netlivaSwitch('state'); // return true
	});
</script>
```
### On Change
if switch the input, triggered the function named *netlivaSwitch.change*
```html
<input id="example-input" type="checkbox" netliva-switch />
<script type="text/javascript">
	jQuery(function ($){
		$("#example-input").on('netlivaSwitch.change', function(event, state, element) {
			console.log(state);
	    });
	});
</script>
```

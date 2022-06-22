# Mortgage Brokers Component Installation


Add this to `functions.php` on your custom theme

```php
add_action('wp_enqueue_scripts', 'propulsoft_custom_scripts');

function propulsoft_custom_scripts() {
  $url = 'https://components.propulsoft.dev/hypothecaire';
  wp_enqueue_script('custom', $url.'/js/Autoload.js', array(), false, true);
  wp_enqueue_script('full-calculator', $url.'/js/FullCalculator.js', array(), false, true);
  wp_enqueue_script('calculator', $url.'/js/Calculator.js', array(), false, true);
  wp_enqueue_script('form-ajax', $url.'/js/FormAjax.js', array(), false, true);
  wp_enqueue_script('sweet-alert', $url.'/plugins/sweetalert2/sweetalert2.bundle.js', array(), false, true);
  wp_enqueue_style('sweet-alert', $url.'/plugins/sweetalert2/sweetalert2.bundle.css');
}
```

# Render components on page 

## Full calculator
```html
<div id="full_calculator"></div>
<script>
jQuery().ready(function() {
	jQuery("#full_calculator").calculator(lang);
});
</script>
```
## Simple Calculator
```html
<div id="simple_calculator"></div>
<script>
jQuery().ready(function() {
	jQuery("#simple_calculator").simple_calculator(lang);
});
</script>
```

## Call Form
```html
<div id="call_form"></div>
<script>
jQuery().ready(function() {
	jQuery("#call_form").call_form(lang, open, optional);
});
</script>
```

## Service Form
```html
<div id="service_form"></div>
<script>
jQuery().ready(function() {
	jQuery("#service_form").service_form(lang, open);
});
</script>

```

# Variables
> `lang` Variable set like `en` or `fr`: default: `fr` - defined the lang for the form


> `open` Varuable set like `true` or `false` - show the form as open or close


> `optional` Variable set like `true` or `false` - shows the optional label in the view

# dropdown-change-price

$('select:eq(0)').change(function() {
    var valueSelected = this.value;
if (valueSelected !== '' && valueSelected !== 'None') {
console.log('yes');
var selected_value =  $('#calculated_option_total').text();	
$('span.price-item.price-item--regular').html('<span class="price-item price-item--regular">$'+selected_value+' USD</span>');
console.log('sdsdsd',selected_value);
    $(this).parents('.form').find('.disable_button').hide();
    $(this).parents('.form').find('.custom-add').show();
    $(this).parents('.form').find('.shopify-payment-button__more-options').removeAttr("disabled");
}
else{
console.log('no');
    $(this).parents('.form').find('.disable_button').show();
    $(this).parents('.form').find('.custom-add').hide();
    $(this).parents('.form').find('.shopify-payment-button__more-options').attr('disabled', 'disabled');
}
//console.log('selected_value',valueSelected);
});
$('select:eq(1)').change(function() {

 var valueSelected2 = this.value;
if (valueSelected2 !== '' && valueSelected2 !== 'None') {
console.log('yes');
var selected_value =  $('#calculated_option_total').text();	
$('span.price-item.price-item--regular').html('<span class="price-item price-item--regular">$'+selected_value+' USD</span>');
 $(this).parents('.form').find('.disable_button').hide();
 $(this).parents('.form').find('.custom-add').show();
 $(this).parents('.form').find('.shopify-payment-button__more-options').removeAttr("disabled");
}
else{
console.log('no');
 $(this).parents('.form').find('.disable_button').show();
 $(this).parents('.form').find('.custom-add').hide();
 $(this).parents('.form').find('.shopify-payment-button__more-options').attr('disabled', 'disabled');
}
});


jQuery(document).on('change', 'select.hulkapps_option_child', function(){
   setTimeout(function(){
       var selected_price_app = jQuery('span#calculated_option_total').text();
console.log('selected_price_app',selected_price_app);
  jQuery('span.price-item.price-item--regular').html('<span class="price-item price-item--regular">$'+selected_price_app+' USD</span>')
   }, 2000); 
});
   

# currency switcher
CradleCMS (eCommerce) currency switcher web component

## Installation
Put the `acurrency.js` component in your themes `components` folder.

## How to use
Include the component and render the currency switcher however you like inside a `<a-currency></a-currency>` tag. 
It listens on a `change` event, uses the ISO-4217 currency code from the target value and does a page reload. 

### Example
```
{% if shop.currencies.size > 1 %}
{% component 'acurrency.js' %}
<a-currency>
  <select name="currency" class="select" value="{{cart.currency}}">
    {% for code in shop.currencies | keys | sort %}
    <option value="{{ code }}" {% if code == cart.currency %}selected{% endif %}>{{code}}</option>
    {% endfor %}
  </select>
</a-currency>
{% endif %}
```

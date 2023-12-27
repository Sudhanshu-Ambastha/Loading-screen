# Loading Screen

A minimalistic loading screen with a dynamic progress bar, built using HTML, CSS, and jQuery.

## Preview

![Loading Screen Preview](https://github.com/Sudhanshu-Ambastha/loding-screen/assets/135802131/3e2ce7a0-9c4d-4ceb-8d25-5c57e57d1f68)

## Usage

1. Clone the repository:

    ```bash
    git clone https://github.com/Sudhanshu-Ambastha/loding-screen.git
    ```

2. Open the `index.html` file in your web browser.

## Customization

Feel free to customize the loading screen to fit your needs. You can modify the text, colors, and styles in the `index.html` and `style.css` files.

### CSS Styles

Adjust the styles in the `<style>` section of the `head` in `index.html`:

```css
/* Customize styles here */
body {
    background: #0d0d0d;
    /* Add your custom styles */
}

/* ... */

.counter {
    /* Customize counter styles */
}

/* ... */
```

## Loading animation

The loading animation is controlled by jQuery in the `<script>` section at the end of `index.html`. You can customize the loading duration, text, and colors:

```javascript
$(document).ready(function(){
    var counter = 0;
    var c = 0;
    var i = setInterval(function(){
        $(".loading-page .counter h1").html(c + "%");
        $(".loading-page .counter hr").css("width", c + "%");
        counter++;
        c++;
        if(counter == 101) {
            clearInterval(i);
        }  
    }, 50);
});
```

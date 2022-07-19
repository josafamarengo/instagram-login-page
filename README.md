# Instagram Login Page

## Stacks:
- **HTML**
- **CSS**
- **JavaScript**

## Slider:
>O Mockup e as imagens de Screenshot, foram copiadas do site original.

Para fazer o efeito da troca de imagens, inseri o código abaixo:

```javascript
let time = 4500,
    currentImageIndex = 0,
    images = document
         .querySelectorAll("#slider img")
    max = images.length;

function nextImage() {
    
    images[currentImageIndex]
        .classList.remove("selected")

    currentImageIndex++

    if(currentImageIndex >= max)
        currentImageIndex = 0

    images[currentImageIndex]
        .classList.add("selected")
}

function start() {
    setInterval(() => {
        nextImage()
    }, time)
}

window.addEventListener("load", start)
```


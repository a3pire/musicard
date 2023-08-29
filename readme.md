![enter image description here](https://raw.githubusercontent.com/A3PIRE/musicard/main/assets/musicard.jpg)
# About
**Musicard** is a lightweight and futuristic music card library designed for Discord bots.

- Fully Customizable
- Lightweight
- High Quality Assets
- Auto Color Detection (from thumbnail)
- Brightness Control

# Installation
```
npm install musicard
```

# Example
This example code will generate a music card image and save it.
```js
(async () => {
const { musicCard } = require("musicard");
    const fs = require("fs");

    // Create a new music card
    const card = new musicCard()
        .setName("Makeba (Ian Asher Remix)")
        .setAuthor("By Ian Asher")
        .setColor("auto") // or hex color without # (default: auto) (auto: dominant color from thumbnail)
        .setBrightness(50)
        .setThumbnail("https://th.bing.com/th/id/OIP.TReQbbMLSu6fwHvqxIUS0gHaHa?pid=ImgDet&rs=1")
        .setProgress(0)
        .setStartTime("0:00")
        .setEndTime("3:00")
        .setOutput("png")

    // Build the card
    const cardBuffer = await card.build();

    // Write the card to a file
    fs.writeFileSync(`musicCard.${card.output}`, cardBuffer);
    console.log("Done!");
})()
```
**Output** : musicCard.png
![output](https://raw.githubusercontent.com/A3PIRE/musicard/main/assets/example.png)

# Projects
We will create projects soon, but if you want your project here using **Musicard**, join our [Discord](https://discord.gg/TvjrWtEuyP) server and contact us.
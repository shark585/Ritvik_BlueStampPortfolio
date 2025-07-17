# Lunar Lander Simulation
Replace this text with a brief description (2-3 sentences) of your project. This description should draw the reader in and make them interested in what you've built. You can include what the biggest challenges, takeaways, and triumphs from completing the project were. As you complete your portfolio, remember your audience is less familiar than you are with all that your project entails!

You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:
```HTML 
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->
```

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Ritvik U | Dougherty Valley High | Computer Science + Astronomy | Incoming Senior 

**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](logo.svg)
  
# Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- I was able to finish building the Raspberry Pi and installed a fan on it to prevent overheating. I also put it in its box to keep the components organized and make it look neater.
- What your biggest challenges and triumphs were at BSE
- The biggest obstacle I faced while completing this milestone was the SD card failing
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE




# Second Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your second milestone, explain what you've worked on since your previous milestone. You can highlight:
- Technical details of what you've accomplished and how they contribute to the final goal
- What has been surprising about the project so far
- Previous challenges you faced that you overcame
- What needs to be completed before your final milestone 

For my second milestone, I mostly focused on optimizing the program's speed by utilizing various methods such as overclocking the Raspberry Pi and tweaking the learning model. The first thing I did was test the base model to see how long it takes to run. However, the base model is a little different from the intented base model already, as I mentioned I had to use an external SSD drive for the Pi's OS instead of the provided SD card since the card stopped working. One important thing to note before I dive in is that the model always ran 100,000 episodes in all of these tests. Albeit, this resulted in a real time of 24 minutes and 39 seconds, which is quite a bit of time for just one program. Furthermore, the graph of the learning model didn't quite show significant improvement for the time given. My next test was to overclock the Pi itself to support voltage of 6V, as well has having a max CPU frequency of 1800 MHz. I also made sure to test it for any overheating before going through and executing the program. This new and improved Pi was able to execute in 24 minutes and 12 seconds, which wasn't much of an increase in efficiency. For reference, the un-modified version of the Pi runs at 1500 MHz CPU and 500 MHz GPU, with a 5V power. When looking at the difference, there isn't really much, and some features can get bottlenecked. Therefore, this didn't really have much of an impact. The next thing I did was tweak the hyperparameters for the learning model in an attempt to improve efficiency.  Specifically, I focused upon the batch size, buffer size, when learning would start, and how often the model would train itself. I made use of the batch size and set it to 32, which meant that it would focus on 32 individual episodes when training instead of 1. I also set the buffer size to 1000 instead of 1, which would let the model sample the 32 episodes from the 1000 while learning. Additionally, I also made the learning to start at 1000 episodes, since that was the first buffer. Lastly, I told the model to train itself every 4 steps instead of 1 for more stability. 


# First Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/CaCazFBhYKs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your first milestone, describe what your project is and how you plan to build it. You can include:
- An explanation about the different components of your project and how they will all integrate together
- Technical progress you've made so far
- Challenges you're facing and solving in your future milestones
- What your plan is to complete your project

My project is a self-landing lunar lander simulation, where it trains itself on landing between two flags in an uneven terrain. This required a Raspberry Pi kit, a USB drive (for Pi OS), and a display screen to view the simulation. For my first milestone, I was able to get the Raspberry Pi working with the mouse and keyboard and I was also able to SSH into the Pi from my laptop. I was also able to get the full base model working and could display the post-training simulation on the screen provided just by running the python script. One major issue I faced while getting this done was the SD card failing (possibly due to overheating). Luckily, I was able to use a USB drive to load the Pi OS on and was able to connect that to the Pi. This allowed it to work normally without overheating issues. However, to be safe, I put the Pi in a case with a fan. Installing the fan was a bit difficult, however, since it was hard to find consistent instructions online. After that, I had to figure out how to establish an SSH with the Pi through my computer's terminal. Using the localhost name wasn't working so I searched it up and found it to work with the Pi's IP. I was then able to similarly establish a remote SSH through Visual Studio Code. After that, I was able to get the code working after installing required packages and fixing minor issues. Furthermore, I added a line that showed the learned video on the display screen at the end of the program. My next step is to optimize the PI and possibly also the program to run faster and more efficiently.

# Schematics 
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. 

# Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

<a href = "https://github.com/shark585/Lunar_Lander/blob/main/base_model.py"> Base Model Code </a>

# Bill of Materials
Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. 

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| RasTech Raspberry Pi 4 Starter Kit | Used for running the simulation (providing CPU) | $92.09 | <a href="https://www.amazon.com/RasTech-Raspberry-Starter-Heatsink-Screwdriver/dp/B0C8LV6VNZ/ref=sr_1_4?crid=3506HY00MCGVM&dib=eyJ2IjoiMSJ9._zkM62vSQ8p7tNr88715LdMv_qHh72Je-tkF9PXEa3chDE53QT4aZu4AGAb4ihE61QY4ZD55nKF6Fp2Kfs8t7AbafM_JrlJFfHo9OB4eAVGqa0EB-7aoBQHPmhKHZ2MW8ny-Kd44bMVlVxPlTWVk5YHIN5P3uKVqrE5Dcal0rKkHny-O6Xyb5ux2AOU6OwVbkag_bqBX66RQNRrgBuz-0pS43mcx93IZTQA9R8NaJJypYU2HAycp-XicTFmyU60a01Nfm9iuyo6B9yA8ppN3OQQyJ-NQ9xyNPxfTLwkqtng.yAYpU6outhQcZmOZhN9Wb6yTw7A85CNUbXZguGInZNg&dib_tag=se&keywords=raspberry%2Bpi%2Bkit&qid=1718848547&s=electronics&sprefix=rasbperry%2Bpi%2Bkit%2Celectronics%2C83&sr=1-4&th=1"> Link </a> |
| 7 Inch Touch Screen Display Panel | Used for displaying the simulation | $36.79 | <a href="https://www.amazon.com/Hosyond-Display-1024%C3%97600-Capacitive-Raspberry/dp/B09XKC53NH/ref=sr_1_3?crid=1KKB9WC62OIAD&keywords=raspberry%2Bpi%2Bips&qid=1685911698&s=electronics&sprefix=raspberry%2Bpi%2Bips%2B%2Celectronics%2C87&sr=1-3&th=1"> Link </a> |
| Wireless Mouse and Keyboard | Used for navigating through the display | $21.99 | <a href="https://www.amazon.com/gp/product/B07XDWCLYF/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&th=1"> Link </a> |

# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.

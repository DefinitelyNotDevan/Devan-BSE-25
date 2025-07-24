# Pose Estimation
Have you ever wondered how bad your posture truly is? Well, wait no longer, as the pose estimator is here to shame you into correcting your posture (as well as many other capabilities)! 

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Devan G | Marin Academy | Electrical Engineering | Incoming Junior

**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](logo.svg)
  
# Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For my final milestone, I got two new robotic arms and stuck them onto a wooden box. It now mirrors both of my arms, tracking them and sending the angles to the ESP32, which has them write to the servos. Because these arms had the largest capacities for movement than my last arm, I had to create a mapping angle function which would turn the possible -180 to +180 degrees into 0-180, adjusting for the servo's  limited movement. I overcomplicated this mapping function a bit because in the end all I needed to do was just add 90* to the arm angle, and it would be adjusted. While installing all of the electronics inside the box, my Raspberry Pi got twisted up, and the Picam broke, meaning I had to make a last-minute adjustment to the code for it to work with a USB webcam. However, in the end, this ended up helping me as the USB webcam was way better at tracking my joints than the Picam and could provide a smoother, faster flask output.

For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE



# Second Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/5flAucnnV8M" title="Devan G. Milestone 2" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

For my second milestone, I added a physical robotic arm from one of my past projects to mirror my left arm. First, I had to set up a math function which using code inspired by <a href="https://stackoverflow.com/questions/72601765/calculate-angle-between-two-coordinates-python"> this StackOverflow forum. </a> With these angles, I then send them over to an ESP32 from another one of my past projects, and the ESP32 controls the servos and has them mimic my arm. It is a bit delayed, but it still does a good job of copying my movements. Sometimes it struggles with tracking my wrist because of the lighting, so in the future, for my next milestone, I'll try to improve the live movement for both arms. I didn't have any major obstacles for this milestone; some little problems I had were errors with the virtual environment or powering issues, but those were solved by creating a new virtual environment and adding a battery pack, respectively.

# First Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/0AwXptokzxw" title="Devan G. Milestone 1" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

For my first milestone, I set up pose estimation using this <a href="https://github.com/ecd1012/rpi_pose_estimation"> code from this Github. </a> The pose estimation uses the TensorFlow PoseNet model to place keypoints on the different joints it tracks, like elbows and knees, and then draws a line through them, giving you the full pose estimation. When implementing it, I  struggled with downloading OpenCV and other libraries as they often wouldn't compile correctly or not even compile at all. In the end, however, like most things, I simply reflashed my Pi and started from a clean slate, where it immediately worked perfectly. It was quite frustrating, as whatever I tried just wasn't working, and I was stuck on the same errors for multiple days until I wiped my Pi and reuploaded the code.


# Schematics 
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. 

# Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

```c++
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  Serial.println("Hello World!");
}

void loop() {
  // put your main code here, to run repeatedly:

}
```

# Bill of Materials
Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. 

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |

# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.

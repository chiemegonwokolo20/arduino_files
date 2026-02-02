
#Reflection

For this assignment, I used an AI assistant(ChatGPT) to help me diagnose and complete a Neo Pixel sequence on the Adafruit Circuit Playground Express. The goal was straightforward on paper-create a red >green> blue chase across the 10 onboard LEDs, pausing between colors-but my original sketch had obvious and hidden problems. The AI’s role was to accelerate the “unblocking” work: it unpacked my uploaded project, inspected the .ino file, pointed out concrete syntax issues(missing semicolons and incomplete function calls), and then produced two clean, runnable sketches: one using Adafruit_NeoPixel directly and another using the higher-level Adafruit_CircuitPlayground library. Having those side-by-side options was particularly helpful because it made the trade-offs visible: more control with the Neo Pixel object vs. a slightly simpler API with the Circuit Playground helper.

 

That said, the AI didn’t “do the project for me”. I still had to define the behavior precisely (100ms per pixel, 1-second holds, repeats indefinitely), understand the pin and pixel count for the CPX (pin 8, 10 pixels), choose which library, load the code into the Arduino IDE, and test on real hardware. I also had the opportunity of playing with the code with my little knowledge of coding, like changing the figures(chasing patterns) made it more interesting than accepting the generated answer from ChatGPT.

 

In terms of whether I contributed meaningfully: yes, I did. My contribution centered on requirements, validation, and learning. I provided the functional spec and the broken code, and then I curated the solution by picking the version that matched my goals, testing it, and confirming behaviour. Importantly, I used this process to deepen my understanding of the control flow and the library calls: why strip.show() is necessary after setting pixel colors, how delays values affect perceived motion, and why defining constants like NUMPIXELS and PIXEL_PIN makes the sketch clearer and more maintainable. I also learned from the AI’s structure-breaking the animation into small, reusable functions like chaseFill() and doStep()- which is a clean pattern I can reuse.

 

Was the assignment easier or more difficult with AI in the loop? It was easier in the sense that I didn’t get stuck for long on trivial syntax problems. AI effectively acted like a very fast programmer that could propose a clean, idiomatic refactor instantly. However, there’s a subtle way in which AI can make things harder if I'm not careful: it can tempt me to skip the “why”. I intentionally addressed this by reading the generated code line by line, running it, and making a couple of small adjustments so I could connect the behavior to the code. AI significantly reduced the friction, but I still had to do some more digging and put in the work to do more cognitive work on the project.

 

Compared with traditional coding forums (like Stack Overflow, Adafruit guides), AI has very different strengths and weaknesses. Forums are great for vetted, community-revised answers, and those posts often include multiple perspectives, edge cases, and discussion about trade-offs. They also teach you to search, skim, and synthesize-valuable skills on your own. The downside is latency: it can take time to find the exact scenario that matches your hardware, your library versions, and your constraints. AI, by contrast, adapts instantly to the exact context I provide (e.g., my specific sketch, my timing requirements). That immediacy is enormous for momentum and motivation. The trade-off is that AI answers aren’t peer-reviewed in the same way, so I must be the reviewer: compile, run, test, and sanity-check claims against documentation.

 

On the question of ethics: I believe that using AI in this capacity is ethical when it's transparent and aligned with the assignment’s learning outcomes. I treated the AI as a tool-like a textbook, a forum, or an IDE feature-not as a ghostwriter. I supplied the requirements, learned from the generated structure, and verified everything on the hardware. I also retained ownership of the design decisions (library choice, timing, and animation style). I also made sure to cite the credible resources used, as it is the right thing to do and required by this class.

 

Finally, did AI ease my concerns about coding-especially as a first-time or early-stage coder on this platform? Absolutely. Seeing a working pattern with clear, named helper functions reduced the intimidation factor. It also made the next steps feel within reach. I now feel confident in how to insert a brightness control, add colour, or smooth cross-fade between colors. The experience shifted my mindset from “Will I get this to compile?” to “What creative effect do I want?” That’s a big jump in confidence.

 

In summary, AI accelerated the tedious parts (syntax fixes, boilerplate structure) and freed me to focus on behaviour and understanding. I contributed meaningfully by setting the requirements, selecting the approach, and validating it on real hardware. The assignment became easier in terms of execution, but it still required me to think and learn to meet the spirit of the course. Compared to forums, AI offered immediacy and context-awareness at the cost of requiring me to self-validate; that’s a trade-off I’m comfortable with. Used transparently and thoughtfully, AI is an ethical learning aid-one that, in my case, helped turn anxiety into curiosity and progress.

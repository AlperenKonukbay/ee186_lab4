# ee186_lab4

**Q1: What are the different bit resolutions can you set the ADC? What is the maximum sampling
rate at each of these resolutions? Where did you find this information in the datasheet?**

**Answer: ** ADC supports 12 10 8 and 6 bit resolution. Max sampling rates are as follows respectively: 5.33,6.15, 7.27, 8.88 Msps. I found this information on page 214 of the DS which is table 81, ADC characteristics. 

**Q2: Why do you need a voltage divider circuit? What would happen if the photodiode is directly
connected to the board?**

**Answer: ** You need a voltage divider in the circuit because the ADC alone only measures voltage, but photoresistors can only chjange resistance. Putting in serioes with the resistor makes it become a voltage divider that converts resistance change into a voltage change, which the ADC can measure. If instead it was directly connected to the board, nearly 0 current would flow the into high-imped ADC input and there would be no voltage diffeence. Pin would sit around 3.3V. 

**Q3: Submit circuit diagrams for both configurations used in this part of the lab. The first should
illustrate the potentiometer connected as a variable voltage divider, and the second should show the
voltage divider circuit using a photodiode and a 10 kΩ resistor. Both diagrams should clearly indicate
the supply voltage Vin, the output voltage Vout, and the ground reference.**

**Answer:** https://drive.google.com/file/d/1pscDfHvFGin02AlFVBJ14pBDnI5bEiGZ/view?usp=sharing

**Q4: Submit a video demonstrating how the output of the ADC changes in the terminal when the
light changes. Submit the code.**
**Answer:** https://drive.google.com/file/d/1BFSuvu25V5OvJVMUllUJ3-kY0b-p6MNm/view?usp=sharing 

**Q5:If B = 9, what is Vout? Express your answer in terms of Vref . Use the DAC mode that
provides the best resolution available on your MCU (refer to the data sheet).**

**Answer:** The DAC mode that provides the best res is 12 bit as per page 46 of the DS where it says DAC has 8 or 12 bit output modes. With 12 bit pluggef nn to the formula we get : 

B / (2^12) = (9 / 4096 ) * Vref 

**Q6: Submit a screenshot of your serial terminal printing DAC, ADC, and their difference as
voltage values as you increment and decrement the DAC output.**

**Answer:** https://drive.google.com/file/d/1EF9nj240FPn_307vU3llrVyTPu9RvOaW/view?usp=sharing
https://drive.google.com/file/d/1acWOIDm8ZmC6ifpJ6TBF2EDJ6YIVxPAw/view?usp=sharing

**Q7: How does the sampling rate of the DAC affect the quality of the output waveform? What
are the differences in sound perception between sine, square, and sawtooth waves? Why do we need a
capacitor in the signal path when sending an audio signal to a speaker or earphones?**

**Answer:** Sampling rate effects the shape of the waveform directly. The DAC holds each value until the next update so if sampling rate is low its more staircase shaped.  A higher one gives more steps per cycle so its more continous and closer to a real sine wave. 

Sine vs Square vs Sawtooth: they are all the same pitch at a different tone. The sine wave is the smoothest, the square is like buzzing and the sawtooth is the brightest and harshest. 

We need a capacitor to block the 1.65 DC offset that the DAC sits at so we ca control and only pass the changing audio signal, and the earphones get a wave centered around 0V. Without it you waste power and mighr damage the device. 

**Q8: Submit a picture of that sine wave on the oscilloscope**
**Answer:** https://drive.google.com/file/d/1_Jpb3H-Tm2Sl0qNnQjvoYpu2wC5IZP3U/view?usp=sharing

**Q9:Submit a short video demonstration of your working Theremin along with your source code.**
**Answer:** https://drive.google.com/file/d/1il8D8SFqs0Eznw0B41mAXpqwGKZJxDfa/view?usp=sharing

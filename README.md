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

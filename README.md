# OFDM_Transceiver_using_Vitis_Model_Composer
This transceiver of OFDM system is implemented using the latest version of Vitis Model Composer 2022.2 and MATLAB version 2022a.

First of all open the file named as Block-Diagram_of_OFDM.png. This will be the transceiver that I will implement.

After that open the file named Serial_2_Parallel.slx in which I will convert the serially coming data into parallel and then again I will convert that parallel data into serial. This you can observed on the scope i.e., initial and final waveform will be same.

After that open the file named QAM_16_Point.slx in which I will implement the QAM_16 modulation. Since we are using QAM-16 so we have to use the serial to paraller converter to collect 4-bit and release that 4-bit parallerly. You will be able to see the In-Phase and Q_Phase output for each point. To check wheather output is correct or not you can match with the table named Actual_Output_QAM-16.

After that open the file named QAM_Mod_with_Dmod.slx in which QAM-16 modulation and demodulation is connected in sequence to verify that the input of QAM_16_Mod is same as the output of the QAM_16_Dmod. 

After that open the file named FFT_64_Point.slx in which FFT of 64 point will be get calculated. NOTE:- FFT block will take some time to calculate the FFT. Hence, we need to apply some dealy to the input side to match the input and output points. Another things that shoudl be get noted is that this FFT block will take 64 point at a time sequentially starting after 4th clock cycle. To observe this behaviour I have collected the input and output in the workspace.

After that open the file named IFFT_64_Point.slx in which IFFT of 64 point will be get calculated. NOTE:- IFFT block will take some time to calculate the IFFT. Hence, we need to apply some dealy to the input side to match the input and output points. Another things that shoudl be get noted is that this IFFT block will take 64 point at a time sequentially starting after 4th clock cycle. To observe this behaviour I have collected the input and output in the workspace. NOTE:- Output of IFFT block gives the output without divided by the number of points. So for that I have added user defined function in M-code block.

After that open the file named IFFT_then_FFT_8_Point.slx in which I have connected the IFFT first and then FFT block to check that input of IFFT block is getting matched with the output of FFT block. If you will run this file then you will be able to see that real and imaginary input of IFFT block is same as the real and imaginary output of FFT blocl. Simillarly you can check for the 64 point. Although I will show the complete OFDM transceiver for 8 point as well 64 point.

After that open the file named cyclic_prefix_of_4_symbol.slx and cyclic_refix_of_16_symbol.slx in which I implemented the addition of cyclic prefix addition and removal. I have made for adding 4 symbol in case of 8 symbol message sequence and adding of 16 symbol in case of 64 symbol message sequence. We can observe the output either on the scope or on the workspace. For better understandings I also have stored the value of Cyclic Prefix in seperate workspace.

Now we have all the block that is getting use in the Block-Diagram_of_OFDM.png.

Now open the file named OFDM_8_Point.slx or OFDM_with_64_Point_FFT_and_IFFT.slx in which you will find the complete OFDM system transceiver.

For any help you can contact me on: -
Email: - ujjwalkrpas@gmail.com

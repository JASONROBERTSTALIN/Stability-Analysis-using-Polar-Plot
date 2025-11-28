# Stability-Analysis-using-Polar-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=10/(S(1+0.5S)(1+0.2S)) using polar plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:
![WhatsApp Image 2025-11-27 at 21 53 33_620dad6d](https://github.com/user-attachments/assets/2995bd4e-5c55-4054-8a43-654dc8d0b0b2)
![WhatsApp Image 2025-11-27 at 21 54 46_8f4a2904](https://github.com/user-attachments/assets/0a3d0f66-fa46-4cd6-a8e8-bc92e0ae1eba)
![WhatsApp Image 2025-11-27 at 21 55 37_f3c95300](https://github.com/user-attachments/assets/7f9c44b8-f8e9-4d07-9772-40d06957b970)
![WhatsApp Image 2025-11-27 at 21 58 42_12330fc9](https://github.com/user-attachments/assets/ef230325-ed5c-4a26-b66a-3b4181f3f456)




## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
num=[10] <br>
den=[0.1 0.7 1 0] <br>
sys=tf(num,den) <br>
[mag,phase,W]=bode(sys) <br>
mag=squeeze(mag) <br>
phase=squeeze(phase) <br>
phase1=deg2rad(phase) <br>
polarplot(phase1,mag,'linewidth',1.5) <br>
grid on <br>
[Gm Pm Wpc Wgc]=margin(sys) <br>
if(Wpc>Wgc) <br>
    disp('stable') <br>
elseif(Wpc == Wgc) <br>
    disp('marginally stable') <br>
else <br>
    disp('unstable') <br>
end <br>

## Output:
![6th exp](https://github.com/user-attachments/assets/d0f23533-fa12-4ddf-bead-fbf91f206f10)


## Result:
Thus the polar plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin = 0.7 <br>
Phase Margin = -8.88<br>
Gain crossover frequency = 3.75<br>
Phase crossover frequency = 3.16<br>
The system is  unstable

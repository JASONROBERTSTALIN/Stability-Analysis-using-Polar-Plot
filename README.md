# Stability-Analysis-using-Polar-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=10/(S(1+0.5S)(1+0.2S)) using polar plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:

![WhatsApp Image 2025-11-23 at 17 25 15_29f72fb9](https://github.com/user-attachments/assets/380409d0-da82-4b4f-b087-a95b5fb590f5)

![WhatsApp Image 2025-11-23 at 17 25 16_135e2cd1](https://github.com/user-attachments/assets/a3c22ff6-e572-4881-8c9b-d9eaa4ebb842)

![WhatsApp Image 2025-11-23 at 17 25 16_938e9b1f](https://github.com/user-attachments/assets/e3f20b32-c417-48ed-8365-36a1a65ad33d)

## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
```
num=[10]
den=[0.1 0.7 1 0]
sys=tf(num,den)
[mag,phase,W]=bode(sys)
mag=squeeze(mag)
phase=squeeze(phase)
phase1=deg2rad(phase)
polarplot(phase1,mag,'linewidth',1.5)
grid on
[Gm Pm Wpc Wgc]=margin(sys)
if(Wpc>Wgc)
    disp('stable')
elseif(Wpc == Wgc)
    disp('marginally stable')
else
    disp('unstable')
end
```

## Output:

<img width="1053" height="985" alt="image" src="https://github.com/user-attachments/assets/24191fc3-ac73-4201-96dd-624d62738f40" />

## Result:
Thus the polar plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin = 0.7692 dB <br>
Phase Margin = -15 degrees <br>
Gain crossover frequency = 3.7565 rad/sec <br>
Phase crossover frequency = 3.1623 rad/sec <br>
The system is stable.

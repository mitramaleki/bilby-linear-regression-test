# bilby-linear-regression-test
just me trying out bilby's parameter estimation on some fake linear data. The whole idea comes from their example code; I just wanted to see how it works.
My bilby sine wave test

Original linear example I modified:
https://git.ligo.org/lscsoft/bilby/blob/master/examples/core_examples/linear_regression_unknown_noise.py

What I changed:
- replaced their line model with my sine wave:
def sine_model(time, amplitude, frequency, phase, offset):
    return amplitude * np.sin(2*np.pi*frequency*time + phase) + offset
- changed params to wave stuff (amplitude=1.5, frequency=0.2, phase=0.3, offset=0.5)
- reduced noise to sigma=0.2
- made time longer (20s) to see more waves

Results image:
<img width="1163" height="1178" alt="a51238d1-0299-4262-815f-beb9e0796390" src="https://github.com/user-attachments/assets/2d07abc1-c24e-4b03-8567-929e8eb1dbce" />


What it found:
- amplitude ≈ 1.5 ± small
- frequency ≈ 0.2 ± tiny
- phase ≈ 0.3 ± bit
- offset ≈ 0.5 ± small
- noise ≈ 0.2 ± tiny


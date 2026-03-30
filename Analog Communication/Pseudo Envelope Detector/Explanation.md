# 📡 Envelope Detector (AM Demodulation)

> Turning a buzzing high-frequency signal into something meaningful 🎧

This project demonstrates a simple yet powerful **envelope detector** built in **LTspice**—a classic circuit used to recover information from an **AM (Amplitude Modulated) signal**.

At its core, this circuit answers a beautiful question:  
👉 *How do you extract a low-frequency message hidden inside a high-frequency carrier?*

---

## 🧠 Concept

An AM signal can be expressed as:

$$
v(t) = A(t)\sin(\omega_c t)
$$

- \( A(t) \) → the **information (message signal)**  
- \( \omega_c \) → the **high-frequency carrier**

The goal?  
👉 Strip away the carrier and recover **just the envelope \( A(t) \)**.

---

## ⚙️ How It Works

The envelope detector is a beautifully minimal circuit made of just:

### 🔹 Diode — *The Gatekeeper*
- Allows only **positive peaks** of the signal  
- Blocks the negative half cycles  
- Performs **half-wave rectification**

---

### 🔹 Capacitor — *The Memory Unit*
- Charges up to the **peak voltage**  
- Holds that value briefly  
- Smooths the rapidly changing carrier  

Think of it like:  
> “Wait… don’t drop yet, I’ll hold this peak for a moment!”

---

### 🔹 Resistor — *The Release Valve*
- Slowly discharges the capacitor  
- Ensures the output can **follow the envelope**  
- Prevents the signal from getting “stuck” at peak  

---

## ⏱️ The Golden Rule (RC Time Constant)

$$
\frac{1}{\omega_c} \ll RC \ll \frac{1}{\omega_m}
$$

### Meaning:

✅ **RC should be large enough**  
→ to remove high-frequency carrier ripple  

✅ **RC should be small enough**  
→ to track the modulation (message signal)

If you mess this up:
- Too small → noisy output 😵  
- Too large → distorted / flat output 🫠  

---

## 🔬 Simulation Overview

The LTspice setup includes:

- 📶 A **modulated signal source** (carrier + message)  
- 🔌 A **1N914 diode**  
- ⚡ An **RC network** (envelope filter)  

---

## 📊 Waveform Breakdown

| Color | Signal |
|------|--------|
| 🟢 Green | AM signal (carrier + modulation) |
| 🔵 Blue | Extracted envelope (demodulated output) |

✨ The magic:  
The blue waveform **smoothly traces the outer shape** of the green signal.

---

## 🧩 Key Components

| Component | Role |
|----------|------|
| 1N914 Diode | Peak rectification |
| Capacitor (C1) | Peak storage |
| Resistor (R5) | Controlled discharge |
| RC Network | Envelope extraction |

---

## 🚀 Applications

This tiny circuit powers some big ideas:

- 📻 AM Radio Receivers  
- 📡 RF Demodulation  
- 🎚️ Analog Peak Detection  
- 🔬 Signal Measurement Systems  
- 🎧 Audio Recovery from RF signals  

---

## 🧾 Why This Matters

The envelope detector is one of the **simplest yet most elegant circuits** in electronics.

With just:
- a diode ⚡  
- a capacitor 🪫  
- a resistor 🔧  

…it decodes information hidden in high-frequency waves.

> Sometimes, the simplest circuits do the smartest work 😉

---

## 🏁 Final Takeaway

This project shows how **rectification + filtering = demodulation**.

A perfect example of:  
📌 *Signal processing without complexity*

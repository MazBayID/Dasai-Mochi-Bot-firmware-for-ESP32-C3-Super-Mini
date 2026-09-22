## 🧩 Hardware

<table>
<tr><th>Part</th><th>Role</th><th>Interface</th></tr>
<tr><td>Waveshare <b>ESP32-C3-Zero</b></td><td>brain + WiFi</td><td>—</td></tr>
<tr><td><b>SSD1306</b> 0.96" OLED</td><td>the face & status</td><td><code>I2C</code></td></tr>
<tr><td><b>INMP441</b> mic</td><td>hears you</td><td><code>I2S in</code></td></tr>
<tr><td><b>MAX98357A</b> + 2W speaker</td><td>talks back</td><td><code>I2S out</code></td></tr>
<tr><td>3× <b>TTP223</b> touch buttons</td><td>talk / next-face / mode</td><td><code>digital</code></td></tr>
<tr><td><b>LiPo + TP4056</b></td><td>portable power</td><td><code>3.7V</code></td></tr>
<tr><td>slide switch</td><td>on / off</td><td>—</td></tr>
</table>

---

## 🔌 Wiring

Everything runs at **3.3V**. Default pins live in [`config.h`](firmware/dasai_mochi_bot/config.h) — easy to change.

<table>
<tr>
<td valign="top">

**OLED (I2C)**
| signal | GPIO |
|---|---|
| SDA | `21` |
| SCL | `20` |

**Mic — INMP441 (I2S)**
| signal | GPIO |
|---|---|
| SCK | `1` |
| WS | `2` |
| SD | `8` |
| L/R | `GND` |

</td>
<td valign="top">

**Speaker — MAX98357A (I2S)**
| signal | GPIO |
|---|---|
| BCLK | `1` |
| LRC | `2` |
| DIN | `5` |
| SD | `3V3` |

**Touch buttons (TTP223)**
| button | GPIO | job |
|---|---|---|
| TALK | `3` | push-to-talk |
| NEXT | `6` | next face |
| MODE | `7` | mode toggle |

</td>
</tr>
</table>

Full step-by-step: **[`hardware/WIRING.md`](hardware/WIRING.md)**

---

## 🚀 Getting started

<table>
<tr>
<td width="90%" valign="top">

### 🙂 For users — no coding

1. Open the **[flash page](https://web.esphome.io/)** in **Chrome / Edge / Opera**.
2. **Hold BOOT** while plugging in USB-C (flash mode).
3. Click **Connect**, pick the port, upload file **DasaiMochi-SuperMini-merged.bin** from Zip, and **Flash**.
4. The bot makes a WiFi network: **`DasaiMochi-Setup`**.
5. Join it → a setup page opens → enter WiFi + your AI key. 🍡

</td>
<td width="90%" valign="top">

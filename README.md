# ESP-IDF Terminal & Commands Quick Reference

## 1. Open ESP-IDF Terminal

In **VS Code**:

1. Press **`Ctrl + Shift + P`**
2. Type:

   ```text
   ESP-IDF: Open ESP-IDF Terminal
   ```
3. Press **Enter**

You can then run ESP-IDF commands such as:

```bash
idf.py build
```

---

## 2. Build the Project

To build the current ESP-IDF project:

```bash
idf.py build
```

---

## 3. Open Serial Monitor

To open the serial monitor on **COM3**:

```bash
idf.py -p COM3 monitor
```

> Replace `COM3` with the COM port of your ESP32 device if it is different.

To build and flash, then open the monitor:

```bash
idf.py -p COM3 flash monitor
```

---

## 4. Open Menu Configuration

To configure the ESP-IDF project:

```bash
idf.py menuconfig
```

This opens the **ESP-IDF configuration menu**, where you can modify project settings, component options, Wi-Fi settings, flash configuration, etc.

---

## 5. Check ESP-IDF Target Environment Variable

In the **PowerShell** terminal, run:

```powershell
echo $env:IDF_TARGET
```

This displays the currently configured ESP-IDF target.

For example:

```text
esp32
```

Other possible targets include:

```text
esp32s2
esp32s3
esp32c3
esp32c6
esp32h2
```

---

## 6. Go to Function Definition

To jump to the definition of a function in **VS Code**:

* Hold **`Ctrl`** and click the function name, or
* Place the cursor on the function and press **`F12`**

### Keyboard Shortcut

```text
F12 → Go to Definition
```

> On some laptops, you may need to press **`Fn + F12`** if the function keys are configured as special hardware keys.

---

## 7. Useful ESP-IDF Commands

| Command                        | Purpose                           |
| ------------------------------ | --------------------------------- |
| `idf.py build`                 | Build the project                 |
| `idf.py flash`                 | Flash firmware to the ESP32       |
| `idf.py -p COM3 monitor`       | Open serial monitor               |
| `idf.py -p COM3 flash monitor` | Flash and open serial monitor     |
| `idf.py menuconfig`            | Open project configuration        |
| `idf.py clean`                 | Clean build files                 |
| `idf.py fullclean`             | Remove the entire build directory |
| `idf.py app`                   | Build the application             |
| `idf.py size`                  | Show firmware size information    |

## Quick Workflow

A typical ESP-IDF development workflow is:

```text
Open ESP-IDF Terminal
        ↓
idf.py menuconfig
        ↓
idf.py build
        ↓
idf.py -p COM3 flash monitor
```

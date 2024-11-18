
# PATLITE Tower Control Interface

This project is a **dynamic web interface** for controlling PATLITE towers through their API. It allows users to:
- Connect to multiple towers by their IP addresses.
- Configure tower settings, including colors, flashing patterns, and buzzer levels.
- Send commands to towers to apply the configurations.
- Remove or clear tower configurations dynamically.

---

## Features

### 1. **Connect to Towers**
- Enter an IP address to connect to a new tower.
- Towers are displayed in a scrollable container for easy access.

### 2. **Dynamic Tower Configuration**
Each tower card includes:
- **Color Selection**: Assign up to 5 tiers with individual colors from a predefined palette.
- **Flashing Control**: Enable or disable flashing for each tier.
- **Buzzer Settings**: Choose from multiple buzzer patterns.

### 3. **Command Buttons**
- **Send Command**: Applies the current configuration to the tower.
- **Clear Command**: Resets the tower's configuration.
- **Remove Tower**: Removes the tower from the interface.

---

## Prerequisites

- A web browser (Google Chrome, Firefox, or similar).
- PATLITE towers accessible via their API.

---

## Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/ivlub/patlite-control.git
   cd patlite-control
   ```

2. Open the `index.html` file in your browser:
   ```bash
   open index.html
   ```

3. Enter the IP address of a PATLITE tower in the input field and click **Verbinden**.

4. Configure the tower:
   - Select colors for up to 5 tiers.
   - Enable flashing for individual tiers.
   - Choose a buzzer pattern.

5. Use the buttons to:
   - Apply the configuration (**Befehl Senden**).
   - Reset the configuration (**Befehl Löschen**).
   - Remove the tower from the interface (**Säule entfernen**).

---

## File Structure

- `index.html`: The main HTML file containing the interface and logic.
- Embedded CSS and JavaScript for styling and functionality.

---

## Technical Details

### 1. **Validation**
- IP addresses are validated using a regular expression before connecting to towers.

### 2. **Dynamic API Request Construction**
- The configuration is sent as an API request to the tower's control endpoint:
  ```
  http://<IP_ADDRESS>/api/control?color=<COLOR>&flash=<FLASH>&buzzer=<BUZZER>
  ```

### 3. **User Feedback**
- Towers are displayed dynamically in a scrollable view.
- Alerts notify the user of invalid IP addresses.


## License

This project is released under the MIT License. See the [LICENSE](LICENSE) file for more details.

---

## Acknowledgements

- **Font Awesome**: Used for icons.
- **PATLITE API**: The interface communicates with PATLITE towers via their API.

---

# Programming Projects Portfolio

**Author:** Daniel  
**Programming Language:** C  
**Repository:** programmingproject2

## About this repository

This repository contains three C programming projects completed as part of programming coursework. Each project uses a menu-driven program and demonstrates different C programming concepts, including structures, unions, arrays, pointers, dynamic memory allocation, modular functions, and function pointers.

This README describes the student-style versions of the projects. The code is written in a straightforward style, with simple prompts and explanations.

---

## Project 1: Dynamic Academic Performance and Risk Analysis

GitHub: https://github.com/mog-ttw/risk-assessment-

This project is a student record management system. It stores student details and helps review academic performance.

### Main features
- Stores student ID, name, course, and grade using a structure.
- Starts with sample student records.
- Adds new student records and expands the array when needed.
- Displays all student records.
- Sorts students by grade, name, or ID.
- Calculates the average grade.
- Finds the top-performing student.
- Searches for students by ID or name.
- Removes a student using their ID.
- Runs a custom academic analysis and creates a summary report.
- Uses function pointers to connect menu options to functions.

### C concepts used
Structures, arrays of structures, dynamic memory allocation, pointers, pointer traversal, strings, `strcmp()`, sorting, searching, modular functions, and function pointers.

---

## Project 2: Dynamic Text Mining and Linguistic Pattern Analyzer

GitHub: https://github.com/mog-ttw/Text-Mining-and-Linguistic-Pattern-Analyzer

This project reads a paragraph and analyses the words in it. It provides information about word frequency and the structure of the text.

### Main features
- Accepts a paragraph of at least 150 words.
- Records the source title and author or publication.
- Stores the paragraph dynamically.
- Counts the total number of words and distinct words.
- Creates a dynamically allocated list of words and their frequencies.
- Finds the longest word and the most frequent word.
- Displays word statistics.
- Sorts words alphabetically or by frequency.
- Searches for a word entered by the user.
- Creates a text summary and calculates lexical diversity.
- Displays memory addresses for selected allocated data.
- Uses function pointers for menu operations.

### Text processing
Words are converted to lowercase before counting. Punctuation, apostrophes, and hyphens are treated as separators. The word storage field has a maximum size, so very long words are limited to fit the structure.

### C concepts used
Dynamic strings, structures, `malloc()`, `realloc()`, `free()`, pointers, pointer traversal, `strlen()`, `strcpy()`, `strcmp()`, sorting, and function pointers.

---

## Project 3: Dynamic IoT Event Monitoring and Callback Engine

GitHub: https://github.com/mog-ttw/iot-monitioring--system

This project simulates IoT devices that produce readings. The system checks the readings and uses callback functions to decide whether a reading is normal or should raise an alert.

### Supported device types
- Temperature sensor
- Pressure sensor
- Battery voltage monitor

### Main features
- Registers devices with unique IDs.
- Prevents duplicate device IDs.
- Stores devices in a dynamically allocated array.
- Expands the array when devices are added and reduces it after removals.
- Displays registered devices and removes devices by ID.
- Generates at least 10 simulated readings in a monitoring run.
- Sends readings to separate callback functions depending on device type.
- Updates device status when a reading is outside its normal range.
- Displays alerts and a monitoring summary.
- Uses a custom sensor drift detector.

### Monitoring limits

| Device | Normal operating range |
|---|---|
| Temperature | 0 to 40 degrees C |
| Pressure | 90 to 110 kPa |
| Battery voltage | 3.30 to 4.20 V |

The simulation uses wider reading ranges so that both normal and abnormal readings can occur.

### Custom callback: Sensor Drift Detector

The `sensor_drift_detector()` function compares the current reading with the previous reading from the same device. It reports a warning if the change is greater than the limit for that device:

- Temperature: more than 8 degrees C
- Pressure: more than 15 kPa
- Battery voltage: more than 0.35 V

The first reading is saved as the starting value. Each later reading is compared with the saved value, and then the current value becomes the new previous value.

### C concepts used
Structures, unions, arrays of structures, dynamic memory allocation, pointers, pointer traversal, `rand()`, `srand()`, callback functions, and function pointers.

---

## How to compile and run

Open the folder containing the relevant C source file in VS Code. Use the matching command below.

### Project 1

If the source file is named `main.c`:

```bash
gcc -std=c11 -Wall -Wextra -pedantic main.c -o academic
./academic
```

If it is named `academic_risk_engine.c`:

```bash
gcc -std=c11 -Wall -Wextra -pedantic academic_risk_engine.c -o academic
./academic
```

### Project 2

```bash
gcc -std=c11 -Wall -Wextra -pedantic main.c -o text_analyzer
./text_analyzer
```

Enter a paragraph of at least 150 words when the program asks for it.

### Project 3

```bash
gcc -std=c11 -Wall -Wextra -pedantic main.c -o iot_monitor
./iot_monitor
```

Register devices of the supported types before generating readings.

**Note:** Run each compile command from the folder where that project's source file is saved. The source filename may differ between project versions.

---

## What I learned

By completing these projects, I practised how to:
- Divide a larger program into smaller functions.
- Create and use structures and unions.
- Store and manage data using dynamic memory.
- Resize arrays using `realloc()`.
- Traverse arrays using pointers.
- Process and compare strings.
- Use function pointers for menu operations and callbacks.
- Generate and analyse simulated data.
- Check program results and handle invalid input.
- Release allocated memory before a program ends.

---

## Author

**Daniel**

C Programming Coursework Projects
# RISC-V Talent Development Program Powered by SAMSUNG and VSD
This is a RISC-V Internship using VSDSquadron Mini based  on RISC-V architecture and uses open-source tools to teach students about VLSI SoC design and RISC-V. The instructor and guide for this internship program is Mr. Kunal Ghosh, Co-Founder of VSD.

# ABOUT ME🚀
Name: NAGARAJ PRAKASH SHETTY
-
College: Sahyadri College of Engineering and Management, Adyar, Mangaluru.
-
Email ID: sharatshetty2510@gmail.com / nagaraj.ec22@sahyadri.edu.in
-
LinkedIn: https://www.linkedin.com/in/nagaraj-prakash-shetty-3264b4247/
-
<details>
<summary>TASK1:Development of C Based LAB</summary>
<img 
src="https://github.com/user-attachments/assets/dea48677-2dc9-480e-a22c-50e92683ba22" alt="Task Icon"/>
  <img
src="https://github.com/user-attachments/assets/96216554-d5e8-486f-a3db-1f23befaa070" alt="Task Icon"/>
<img
src="https://github.com/user-attachments/assets/d771f6dd-07e0-4f3a-bb16-5980613bccaa" alt="Task Icon"/>
<img
src="https://github.com/user-attachments/assets/fef6562c-a3a0-4055-948d-2adb860c053e" alt="Task Icon"/>
  <img
src="https://github.com/user-attachments/assets/2355abed-78e1-44e9-ba6d-f14899c60142" alt="Task Icon"/>
  <img
src="https://github.com/user-attachments/assets/0b18ba5d-c4c7-4be9-97a9-cc67e913bcab" alt="Task Icon"/>
</details>
<details>
<summary>TASK2:Simulation with Spike</summary>
<img width="959" alt="Image" src="https://github.com/user-attachments/assets/674b87c3-8b8f-496c-9503-153806811360" alt="Task Icon"/>
<img width="959" alt="Image" src="https://github.com/user-attachments/assets/b276fe30-0f9b-4d93-b41f-aa8207b0adfe" alt="Task Icon"/>
</details>

<details>
<summary>TASK3:Identification of RISCV instructions</summary>
<img width="959" alt="Image" src="https://github.com/user-attachments/assets/c5fd70c3-389d-49f2-834d-a5a0b0ea567d" />
<img width="959" alt="Image" src="https://github.com/user-attachments/assets/f1525077-2f06-452c-ab06-1092f773109a" />
<img width="959" alt="Image" src="https://github.com/user-attachments/assets/ce7c349d-6ccb-4fa3-80be-6aff3ae78c5e" />
<summary>1. addi sp, sp, -32</summary>

Opcode(ADDI): 0010011  
Immediate: -32 = 11111111111111100000 (12 bits)  
Registers: sp(rd) = 00010, sp(rs1) = 00010  

| imm[11:0]       | rs1    | funct3 | rd    | opcode  |
|------------------|--------|--------|-------|---------|
| 111111100000     | 00010  | 000    | 00010 | 0010011 |

---
<summary>2. sd ra, 24(sp)</summary>

Opcode(SD): 0100111  
Immediate: 24 (split into two parts: imm[11:5] and imm[4:0])  
Registers: rs1 = sp = 00010, rs2 = ra = 00001  

| imm[11:5] | rs2   | rs1   | funct3 | imm[4:0] | opcode  |
|-----------|-------|-------|--------|----------|---------|
| 0000000   | 00001 | 00010  | 011    | 11000    | 0100111 |

---

<summary>3. jal ra, 10448</summary>

Opcode(JAL): 1101111  
Immediate: 10448  
Register (rd): ra = 00001  

| imm[20] | imm[10:1] | imm[11] | imm[19:12] | rd    | opcode  |
|---------|-----------|---------|------------|-------|---------|
|   0    | 0010100000 |    0    | 10100000   | 00001 | 1101111 |

---

<summary>4. ld ra, 24(sp)</summary>

Opcode(LD): 0000011  
Immediate: 24  
Registers: rd = ra = 00001, rs1 = sp = 00010  

| imm[11:0]      | rs1   | funct3 | rd    | opcode  |
|-----------------|-------|--------|-------|---------|
| 000000011000    | 00010 | 011    | 00001 | 0000011 |

---

<summary>5. lw a1, 8(sp)</summary>

Opcode(LW): 0000011  
Immediate: 8  
Registers: rd = a1 = 01011, rs1 = sp = 00010  

| imm[11:0]      | rs1   | funct3 | rd    | opcode  |
|-----------------|-------|--------|-------|---------|
| 000000001000    | 00010 | 010    | 01011 | 0000011 |

---

<summary>6. li a0, 0</summary>

Opcode(ADDI): 0010011  
Immediate: 0  
Registers: rd = a0 = 01010, rs1 = x0 = 00000  

| imm[11:0]     | rs1   | funct3 | rd    | opcode  |
|---------------|-------|--------|-------|---------|
| 000000000000  | 00000 | 000    | 01010 | 0010011 |

---

<summary>7. jalr x0, 0(ra)</summary>

| imm[11:0]     | rs1   | funct3 | rd    | opcode  |
|---------------|-------|--------|-------|---------|
| 000000000000  | 00001 | 000    | 00000 | 1100111 |

---

<summary>8. addi a0, a0, -920</summary>

Opcode(ADDI): 0010011  
Registers: rd = a0 = 01010, rs1 = a0 = 01010  
Immediate: -920 = 110001101000 (sign-extended 12-bit value)  

| imm[11:0]     | rs1   | funct3 | rd    | opcode  |
|---------------|-------|--------|-------|---------|
| 110001101000  | 01010 | 000    | 01010 | 0010011 |

---

<summary>9. sd s0, 16(sp)</summary>

Opcode(SD): 0100111  
Registers: rs1 = sp = 00010, rs2 = s0 = 01000  
Immediate: 16 (split into imm[11:5] and imm[4:0])  
imm[11:5] = 0000000, imm[4:0] = 10000  

| imm[11:5]     | rs2   | rs1   | funct3 | imm[4:0] | opcode  |
|---------------|-------|-------|--------|----------|---------|
| 0000001       | 01000 | 00010 | 011    | 10000    | 0100111 |

---

<summary>10. lw a5, 12(sp)</summary>

Opcode(LW): 0000011  
Registers: rd = a5 = 01000, rs1 = sp = 00010  
Immediate: 12 = 000000001100  

| imm[11:0]     | rs1   | funct3 | rd    | opcode  |
|---------------|-------|--------|-------|---------|
| 000000001100  | 00010 | 010    | 01000 | 0000011 |

---

<summary>11. add a1, a1, a5</summary>
Opcode: 0110011

| funct7   | rs2   | rs1   | funct3 | rd    | opcode  |
|----------|-------|-------|--------|-------|---------|
| 0000000  | 01000 | 01011 | 000    | 01010 | 0110011 |

---

<summary>12. add a0, a1, a5</summary>

Opcode(ADD): 0110011  
Registers: rd = a0 = 01010, rs1 = a1 = 01011, rs2 = a5 = 01000  
Funct3: 000  
Funct7: 0000000  

| funct7   | rs2   | rs1   | funct3 | rd    | opcode  |
|----------|-------|-------|--------|-------|---------|
| 0000000  | 01000 | 01011 | 000    | 01010 | 0110011 |

---

<summary>13. addw a1, a1, a5</summary>

Opcode(ADDW): 0111011  
Registers: rd = a1 = 01011, rs1 = a1 = 01011, rs2 = a5 = 01000  
Funct3: 000  
Funct7: 0000000  

| funct7   | rs2   | rs1   | funct3 | rd    | opcode  |
|----------|-------|-------|--------|-------|---------|
| 0000000  | 01000 | 01011 | 000    | 01011 | 0111011 |

---
<summary>14. lui a0, 0x2b</summary>

Opcode(LUI): 0110111  
Immediate (0x2b << 12): 0000000000101011  
Register (rd): a0 = 01010  

| imm[31:12]      | rd      | opcode  |
|------------------|---------|---------|
| 0000000000101011 | 01010   | 0110111 |

 ---                   
<summary> 15. li a0,0</summary>

|imm[11:0] | 	rs1 	|funct3 |	 rd   	|opcode |
|----------|-------|-------|--------|-------|
|000000000000|	00000	|000	|01010	|0010011|
---
</details>
<details>
<summary>TASK4:Functional Simulation of RISC-V Core</summary>
</summary>
<img width="959" alt="Image" src="https://github.com/user-attachments/assets/679df146-7745-4ddc-bc5c-e1e737075164" />
<img width="959" alt="Image" src="https://github.com/user-attachments/assets/bc06334a-cdec-4442-8114-ee6838431ac0" />
<img width="959" alt="Image" src="https://github.com/user-attachments/assets/b7ff8b2d-7a42-4519-a6ca-78b2be14b2f8" />
<img width="959" alt="Image" src="https://github.com/user-attachments/assets/0317a1c4-f6a3-4f00-88d1-537735299021" />
<img width="959" alt="Image" src="https://github.com/user-attachments/assets/32aa419f-2c48-4269-adea-19b571c65322" />
<br>


</details>
<details>
<summary>TASK5:Project overview-circuit diagram</summary>
</summary>
# TASK-5
# PROJECT :- OBJECT DISTANCE DETECTOR & DISPLAY IT ON I2C LCD





# OVERVIEW

The Object Detector project integrates an ultrasonic sensor with the CH32V003 RISC-V processor to detect nearby objects. 
 An ultrasonic sensor measures the distance to an object by emitting ultrasonic waves and calculating the time it takes for the waves to return after bouncing off the object. This time is then converted into a distance measurement.The I2C LCD display allows for efficient communication between the microcontroller and the display, enabling the system to present the measured distance or object detection status.

![Screenshot 2025-02-16 165033](https://github.com/user-attachments/assets/e1e6dfbd-3ea4-4152-bbd3-586de31eb6fe)

# Components Required:

Microcontroller: CH32V003F4U6


Ultrasonic Sensor: HC-SR04

I2C LCD Display: 16x2

Jumper Wires

Breadboard


# HARDWARE CONNECTION

# Pin Connections:

# Ultrasonic Sensor (HC-SR04) Connections:

VCC: Connect to 5V power supply on VSDSquadron Mini


GND: Connect to ground on VSDSquadron Mini


TRIG PIN to PA1 on VSDSquadron Mini


ECHO PIN to PA2 on VSDSquadron Mini



# I2C LCD Display Connections:

VCC: Connect to 5V power supply


GND: Connect to ground


SDA: Connect to GPIO pin to PC1


SCL: Connect to GPIO pin to PC2

# Connected Circuit
![WhatsApp Image 2025-02-17 at 9 23 47 PM](https://github.com/user-attachments/assets/2b392dbe-5ae1-4cc0-8948-a8c1445bfa22)

# CODE

#include <ch32v00x.h>

#include <debug.h>

#include <stdio.h>

#define I2CLCD_H

#include "i2clcd.h"


#define LCD_ADDRESS 0x27

#define TRIG_PIN  GPIO_Pin_1  // PA1 - Trigger

#define ECHO_PIN  GPIO_Pin_2  // PA2 - Echo

#define GPIO_Pin_9  (1 << 9)

#define GPIO_Pin_10 (1 << 10)



// Function prototypes
void Ultrasonic_Init(void);

uint32_t Measure_Distance();

void DelayUs(uint32_t us);

void DelayMs(uint32_t ms);

void Ultrasonic_Init(void) {

    GPIO_InitTypeDef GPIO_InitStruct;

    RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOA, ENABLE);

    // Configure TRIG pin as Output
    
    GPIO_InitStruct.GPIO_Pin = TRIG_PIN;
    
    GPIO_InitStruct.GPIO_Mode = GPIO_Mode_Out_PP;
    
    GPIO_InitStruct.GPIO_Speed = GPIO_Speed_50MHz;
    
    GPIO_Init(GPIOA, &GPIO_InitStruct);

    // Configure ECHO pin as Input
    
    GPIO_InitStruct.GPIO_Pin = ECHO_PIN;
    
    GPIO_InitStruct.GPIO_Mode = GPIO_Mode_IN_FLOATING;
    
    GPIO_Init(GPIOA, &GPIO_InitStruct);
}

uint32_t Measure_Distance() {
    uint32_t time, distance;

    // Send Trigger Pulse
    GPIO_ResetBits(GPIOA, TRIG_PIN);
    DelayUs(2);
    GPIO_SetBits(GPIOA, TRIG_PIN);
    DelayUs(10);
    GPIO_ResetBits(GPIOA, TRIG_PIN);

    // Wait for Echo to go HIGH
    while (GPIO_ReadInputDataBit(GPIOA, ECHO_PIN) == 0);
    
    // Measure pulse duration
    time = 0;
    while (GPIO_ReadInputDataBit(GPIOA, ECHO_PIN) == 1) {
        time++;
        DelayUs(1);
    }

    // Convert to distance (cm)
    distance = (time * 0.0343) / 2;
    return distance;
}

void USART1_Init(void) {

    GPIO_InitTypeDef GPIO_InitStruct;
    
    USART_InitTypeDef USART_InitStruct;
    
    RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOA | RCC_APB2Periph_USART1, ENABLE);

    // Configure PA9 (TX) as alternate function push-pull
    GPIO_InitStruct.GPIO_Pin = GPIO_Pin_9;
    GPIO_InitStruct.GPIO_Mode = GPIO_Mode_AF_PP;
    GPIO_InitStruct.GPIO_Speed = GPIO_Speed_50MHz;
    GPIO_Init(GPIOA, &GPIO_InitStruct);

    // Configure PA10 (RX) as input floating
    GPIO_InitStruct.GPIO_Pin = GPIO_Pin_10;
    GPIO_InitStruct.GPIO_Mode = GPIO_Mode_IN_FLOATING;
    GPIO_Init(GPIOA, &GPIO_InitStruct);

    USART_InitStruct.USART_BaudRate = 115200;
    USART_InitStruct.USART_WordLength = USART_WordLength_8b;
    USART_InitStruct.USART_StopBits = USART_StopBits_1;
    USART_InitStruct.USART_Parity = USART_Parity_No;
    USART_InitStruct.USART_Mode = USART_Mode_Rx | USART_Mode_Tx;
    USART_InitStruct.USART_HardwareFlowControl = USART_HardwareFlowControl_None;
    USART_Init(USART1, &USART_InitStruct);
    
    USART_Cmd(USART1, ENABLE);
}

void USART1_SendString(char *str) {

    while (*str) {
    
        USART_SendData(USART1, *str++);
        
        while (USART_GetFlagStatus(USART1, USART_FLAG_TXE) == RESET);
    }
}

int main(void) {
    SystemInit();
    Ultrasonic_Init();
    USART1_Init();
    I2C_LCD_Init();

    LCD_Clear();
    LCD_SetCursor(0, 0);
    LCD_Print("Ultrasonic Sensor");

    while (1) {
        uint32_t distance = Measure_Distance();
        
        char buffer[20];
        sprintf(buffer, "Distance: %d cm", distance);

        // Print to LCD
        LCD_Clear();
        LCD_SetCursor(0, 0);
        LCD_Print("Distance:");
        LCD_SetCursor(0, 1);
        LCD_Print(buffer);

        // Print to Serial (for debugging)
        USART1_SendString(buffer);
        USART1_SendString("\n");

        DelayMs(500);
    }
}

// Microsecond delay function

void DelayUs(uint32_t us) {

    for (volatile uint32_t i = 0; i < us * 10; i++);
}

// Millisecond delay function

void DelayMs(uint32_t ms) {

    for (volatile uint32_t i = 0; i < ms * 10000; i++);
}


// Function Declarations

void lcdInit();

void setCursor(uint8_t col, uint8_t row);

void printLCD(const char* str);

void clear(); // Add this line for clear function

// Internal Functions

void lcdCommand(uint8_t cmd);

void sendI2C(uint8_t data, uint8_t mode);

void writeNibble(uint8_t nibble);

</details>
<details>
<summary>TASK6: WORKING Principle of the Object Detection System Using Ultrasonic Sensor with I2C LCD Display</summary>




# WORKING Principle of the Object Detection System Using Ultrasonic Sensor with I2C LCD Display

This project utilizes an ultrasonic sensor to detect objects and measures the distance to them. The measured distance is then displayed on an I2C LCD screen.

# 1. Ultrasonic Sensor Operation:

The ultrasonic sensor operates by emitting high-frequency sound waves and measuring the time it takes for the sound waves to reflect back from an object.

Trigger Pulse: The sensor emits a short ultrasonic pulse through its transmitter.

Echo Pulse: The pulse travels through the air, reflects off an object, and returns to the sensor's receiver.

Time Measurement: The sensor measures the time interval between sending the trigger pulse and receiving the echo pulse.



# 2. I2C LCD Display:

The I2C LCD display is used to show the measured distance. It communicates with the microcontroller via the I2C protocol, which requires only two data lines: SDA (Serial Data) and SCL (Serial Clock).

Initialization: The microcontroller initializes the I2C communication and the LCD display.

Data Display: The calculated distance is converted to a string and sent to the LCD to be displayed.

# 3. System Workflow:

Initialization:

The microcontroller initializes the ultrasonic sensor and the I2C LCD display.
The LCD displays a welcome message or prompts the user.
Distance Measurement:

The microcontroller triggers the ultrasonic sensor to emit a pulse.
It waits for the echo pulse and measures the time taken for the round trip.
The distance to the object is calculated based on the measured time.
Display Update:

The LCD is cleared, and the new distance measurement is displayed.
Repeat:

The system repeats the measurement and display update at regular intervals.


# 4. Practical Applications:

This system can be used in various applications, such as:

Obstacle Detection: Detecting objects in the path of a robot or vehicle.

Level Measurement: Measuring the level of liquids or solids in a container.

Distance Sensing: Providing distance measurements for various automation tasks.







# VIDEO OF THE PROJECT



https://github.com/sharaxtns/samsung-riscv/issues/1#issue-2873261340
</details>

<table>
   <tr>
    <td colspan="2" align="center">
      <h1> STM32 Reversible Counter Project</h1>
    </td>
  </tr>
  <tr>
    <td width="10%">
      <img src="assets/preview.gif" alt="Project preview" style="width:100%;">
    </td>
    <td width="50%" valign="middle">
      
   <p> A hardware implementation of a reversible 2-bit binary counter based on the STM32F446RE MCU.</p>
      <ul>
        <li>Red LEDs: Show the current counter value (Binary representation).</li>
        <li>Green LED: Indicates counting direction (ON = Up, OFF = Down).</li>
        <li>Button: Changes the counting direction using HAL interrupts function.</li>
      </ul>
  </tr>
</table>

## Project Overview 
This project implements a hardware counter on an STM microcontroller family using HAL libraries.  
The core functionality relies on GPIO pins and the EXTI (External Interrupt) module to manage counter operations efficiently via hardware interrupts.  
## Key Features 
* Interrupt-Driven Counting:  
Utilizes the EXTI module and GPIOs to handle inputs and counting logic. 
* PC Communication: Planned implementation of a communication system to exchange data between the MCU and a computer,  
allowing the user to monitor which number is currently displayed on the LEDs. 
* Circular Buffer: Implements a circular buffer data structure to manage transmission queues.  
The MCU processes instructions and updates the counter much faster than the serial interface can transmit the bits to the PC. 
Since the transmission is serial, attempting to send data immediately upon generation results in bits being overwritten and information loss.  

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

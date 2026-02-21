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
* PC Communication: ~~Planned implementation of a communication system to exchange data between the MCU and a computer,  
allowing the user to monitor which number is currently displayed on the LEDs.~~ 18/02/26 Implemented UART interrupts communication to monitor correctness of the displayed number. 
* Circular Buffer: ~~Planned implementation of a circular buffer which manages transmission queues. In this project it is not really necessary to implement such a buffer because UART has plenty of time to transmit data between the cycle of switching the LEDs but I'm planning to do it for educational purposes.~~ 20/02/26 With the help from Mastering STM32 book I implemented an early version of circular buffer.
* KiCAD Scheme: Here I'm planning to add a KiCAD scheme of this project.
## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

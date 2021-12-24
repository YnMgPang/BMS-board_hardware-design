# BMS Board: Hardware Design
Circuit and PCB design of a Battery Management System(BMS) STM32 Shield

<img src="https://user-images.githubusercontent.com/94412167/147296119-54904b56-30dc-4177-b94f-220ccb6bafe9.png" width=30% height=30%> <img src="https://user-images.githubusercontent.com/94412167/147296252-eb5ad155-0f2b-4168-9a8c-487e168005a0.png" width=30% height=30%> <img src="https://user-images.githubusercontent.com/94412167/147296205-c51b9fb6-99c5-42cd-b34c-9b28c3c602f9.png" width=30% height=30%>

# Content
- File Structure
- About This Project
- Circuit Design Principle
- PCB Design Principle
- Further Work/Potential Improvements

# File Structure
- Readme
- Complete project package, Altium Designer

# About This Project
- A "piggyback" PCB board(shield) is developed to be mounted on a Nucleo F429ZI board.
- The shield + Nucleo setup serves as a BMS system, with the following functions:
  - Shield:    
    - Voltage monitoring(5-12 cells)
    - Temperature monitoring
    - Passive battery balancing(5-12 cells)
    - Inter-chip SPI connection(daisy chain, basic config. only, not implemented here)
  - Nucleo:    
    - CAN connection(functional but not used here)
    - Future added functions

# Circuit Design Principle
- Adopted design from Niklas Hörnschemeyer's work
  - "Development of a battery management system for racing cars", ISEA, March 2021
- Added filters, fuses, and a relay at critical connection points
  - Battery connector, temperature sensor connector, power input
- Added thermal pads for balancing resistors

# PCB Design Principle
- Board shape conforms to Nucleo board's form factor.
  - Slightly oversized shield with double-layer design
- "Modular" placement 
  - Different regions on the board clearly identifiable 
- Shared ground plates
- Double-layer placement
  - Greatly reduces board area requirement

# Further Work/Potential Improvements
- Write the embedded code for testing
- Manufacture and test the board for intended functionalities
- Add additional functions(daisy chain, more computations on Nucleo board, CAN comm.)
- Improve board space utilization

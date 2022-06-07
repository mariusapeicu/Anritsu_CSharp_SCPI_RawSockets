# Anritsu SCPI RawSockets C++ SCPI Commands example  

## 1.Overview
Anritsu SCPI RawSockets C++ Commands are SCPI based solutions which run with Anritsu Instruments.
The present example are C++ based programs to command Anritsu devices.  
It exemplifies how to perform the following actions in software communication:
* Connect 
* Write 
* Query 
* Disconnect (Close Connection)

**Programming language and dependency**: C++, Microsoft Visual Studio 2015 Platform Toolset - v140, Target Platform Version - 8.1, Visa32 Library  
**Supported Model(s)**: All Anritsu Instrumnets  
**Interface(s)**: Ethernet  
**Software version Tested**: MVS2019 V16.11.11 ; MVS2015 V14.0.23107.0, Visual Studio - SDK 10.0.10586; visa32.lib
**Solution Revision**: 1.0  
**Original Release Date**: 6/7/2022  
**Current Revision Date**: 6/7/2022


## 2.Required Software
Some software components need to be installed before using these solutions. The current versions of these components are listed below, and can be downloaded from their respective website.

[Visual Studio](https://visualstudio.microsoft.com/downloads/) 

Refer to the relevant Software Developers resources for more information about software requirements.

## 3.Installation
Refer to the above-mentioned relevant Software Developer resources for more information on required Software installation.  
The C# Commands example solutions require no installation, and can be open in Microsoft Visual Studio as is, to be run and/or edited.

## 4.Running

>  **Keep in mind that the Anritsu Instrument has to be running during the execution of this example solution.**

The example covers the method of sending SCPI commands via VXI-11 protocol - VISA library


### 4.0. Instrument connection

The instrument connection is instantiated as a class object depending on the connection type.  
Example addresses for instrument connection:

    * TCPIP0::127.0.0.1::inst0::INSTR

> **Important Note:**
>> The script examples use the localhost address 127.0.0.1 for a device connected directly to the computer running the script; to work with devices connected to another computer in the network **don't forget to change the instrument address (and *timeout* value) in the first few lines of the *Main()* function**, before the "/Object instantiation" code.


If the connection fails for any reason, the error message is displayed in the terminal, and the script stops running completely.

### 4.1. Read Instrument type - *IDN? Query
Simple example of a query command; *IDN?
Returns information about the device manufacturer, model, serial, and firmware revision number.

### 4.2. System preset - *RST
Simple example of a write command;
The instrument is returned to its factory as-shipped configuration.

### 4.3. Instrument connection closing
The connection object will end the relevant connection method depending on the type it instantiated at step 0.

## 5.Revision History
The latest version of this C++ example, and examples for other programming languages, can be downloaded at [this location (to be determined)].

REV 1.0, 06/07/2022  
Modified by: Voicu Bogdan, Bucharest, Romania  
Original Release. 

# Test Plan Site

<table>
<colgroup>
<col style="width: 31%" />
<col style="width: 68%" />
</colgroup>
<tbody>
<tr class="odd">
<td><blockquote>
<p>Requested by:</p>
</blockquote></td>
<td><blockquote>
<p><strong>LSST</strong></p>
</blockquote></td>
</tr>
<tr class="even">
<td><blockquote>
<p>Code / Version:</p>
</blockquote></td>
<td><blockquote>
<p>7186_GIS_0009 / 2.0</p>
</blockquote></td>
</tr>
<tr class="odd">
<td><blockquote>
<p>Editor:</p>
</blockquote></td>
<td><blockquote>
<p>F. Javier López</p>
</blockquote></td>
</tr>
<tr class="even">
<td><blockquote>
<p>Approved by:</p>
</blockquote></td>
<td><blockquote>
<p>Franco Colleoni</p>
</blockquote></td>
</tr>
<tr class="odd">
<td><blockquote>
<p>Date:</p>
</blockquote></td>
<td><blockquote>
<p>02/09/2022</p>
</blockquote></td>
</tr>
</tbody>
</table>

## Index

1\. Introduction [5](#introduction)

2\. Reference document list [5](#reference-document-list)

3\. Technical description [5](#technical-description)

4\. Testing procedure [6](#testing-procedure)

5\. Detections testing [8](#detections-testing)

5.1 D-1 GIS Fire Interlock [8](#d-1-gis-fire-interlock)

5.2 D-2 Catastrophic Earthquake Interlock [9](#d-2-catastrophic-earthquake-interlock)

5.3 D-3 GIS Internal Failure [11](#_Toc112939374)

5.4 D-4 GIS ETPBs [12](#d-4-gis-etpbs)

5.5 D-5 Unauthorized Pier access [14](#d-5-unauthorized-pier-access)

5.6 D-6 Unauthorized Dome access [15](#d-6-unauthorized-dome-access)

5.7 D-7 TMA Brakes NOT engaged [16](#d-7-tma-brakes-not-engaged)

5.8 D-8 Camera Cable Wrap Safety Device Actuated [17](#d-8-camera-cable-wrap-safety-device-actuated)

5.9 D-9 TMA ETPBs [18](#d-9-tma-etpbs)

5.10 D-10 Dome Locking pin retracted or Dome Rear Door Louvers NOT closed
[20](#d-10-dome-locking-pin-retracted-or-dome-rear-door-louvers-not-closed)

5.11 D-11 Dome Rear doors are NOT closed [21](#d-11-dome-rear-doors-are-not-closed)

5.12 D-12 Dome ETPBs [22](#d-12-dome-etpbs)

5.13 D-13 Dome Crane not parked [23](#d-13-dome-crane-not-parked)

5.14 D-14 Camera Rotator Pin Inserted [24](#d-14-camera-rotator-pin-inserted)

5.15 D-15 Platform Lift above Enclosure Lower Level [25](#d-15-platform-lift-above-enclosure-lower-level)

5.16 D-16 Platform Lift NOT parked at the Telescope Level [26](#d-16-platform-lift-not-parked-at-the-telescope-level)

5.17 D-17 Failed MCS Watchdog or MCS Loss of Communication [27](#d-17-failed-mcs-watchdog-or-mcs-loss-of-communication)

5.18 D-18 M1M3 Interlock [28](#d-18-m1m3-interlock)

5.19 D-19 Man-Lift not parked [29](#d-19-man-lift-not-parked)

6\. Relay interlocks testing [30](#relay-interlocks-testing)

6.1 GIS [30](#gis)

6.1.1 Wireless 1 [30](#wireless-1)

6.1.2 Wireless 2 [31](#wireless-2)

6.2 LASER [31](#laser)

6.2.1 Laser controller [32](#laser-controller)

6.3 PFLOW [32](#pflow)

6.3.1 PFlow [32](#pflow-1)

6.4 M2 CAMERA [33](#m2-camera)

6.4.1 M2 Actuator [33](#m2-actuator)

6.4.2 M2 Hexapod [34](#m2-hexapod)

6.4.3 Camera Rotator [34](#camera-rotator)

6.4.4 Camera Hexapod [35](#camera-hexapod)

6.5 ACCESS / FIRE / EARTHQUAKE [36](#access-fire-earthquake)

6.5.1 Access [36](#access)

6.5.2 Fire [36](#fire)

6.5.3 Earthquake [37](#_Toc112939407)

7\. Delays testing [38](#delays-testing)

7.1 Earthquake delay [38](#earthquake-delay)

8\. User permissions check [39](#_Toc112939410)

8.1 Level 3 permissions check [39](#level-3-permissions-check)

8.2 Level 2 permissions check [40](#level-2-permissions-check)

9\. User Interface [40](#user-interface)

## Document history

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 18%" />
<col style="width: 53%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>VERSION</strong></td>
<td><strong>DATE</strong></td>
<td><strong>EDITOR</strong></td>
<td><strong>COMMENTS</strong></td>
</tr>
<tr class="even">
<td>1.0</td>
<td>2022/05/02</td>
<td>F. Javier López</td>
<td><blockquote>
<p><em>Initial release</em></p>
</blockquote></td>
</tr>
<tr class="odd">
<td>2.0</td>
<td>2022/05/10</td>
<td>F. Javier López</td>
<td><blockquote>
<p><em>Added Franco Colleoni’s comments</em></p>
</blockquote></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 15%" />
<col style="width: 84%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Acronyms</strong></th>
<th><strong>Definition</strong></th>
</tr>
<tr class="odd">
<th><p>AFE / AcFiEa</p>
<p>ETPB</p></th>
<th><p>Access Fire Earthquake</p>
<p>Emergency trip pushbutton</p></th>
</tr>
<tr class="header">
<th>GIS</th>
<th>Global Interlock System</th>
</tr>
<tr class="odd">
<th>HMI</th>
<th>Human Machine Interface</th>
</tr>
<tr class="header">
<th><p>IS</p>
<p>LAS</p></th>
<th><p>Interlock System</p>
<p>LASER</p></th>
</tr>
<tr class="odd">
<th><p>LSST</p>
<p>UI</p></th>
<th><p>Large Synoptic Survey Telescope</p>
<p>User Interface</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

## Introduction

This document collects the procedures performed to verify the correct function of the Global Interlock System (GIS),
which ensures the protection of the different systems of the telescope.

It includes the steps followed to complete GIS tests. Passing the tests confirms the correct communication, reception
and emission of signals, between the different safety systems and, summarizing, the correct actuation of the system.

## Reference document list

<table>
<colgroup>
<col style="width: 5%" />
<col style="width: 57%" />
<col style="width: 18%" />
<col style="width: 18%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>No.</strong></td>
<td><strong>DOCUMENT</strong></td>
<td><strong>CODE</strong></td>
<td><strong>VERSION</strong></td>
</tr>
<tr class="even">
<td><strong>1</strong></td>
<td><blockquote>
<p>GLOBAL INTERLOCK SYSTEM (GIS) ANALYSIS</p>
</blockquote></td>
<td>092-308-E-Z-00004</td>
<td>04</td>
</tr>
<tr class="odd">
<td><strong>2</strong></td>
<td><blockquote>
<p>Updated LTS-99</p>
</blockquote></td>
<td>092-308-F-I-00003</td>
<td>01</td>
</tr>
<tr class="even">
<td><strong>3</strong></td>
<td><blockquote>
<p>Electric schemes – 7186 Test System for GISS_LSST Cabinets</p>
</blockquote></td>
<td><em>7186_GIS_0003</em></td>
<td>1.0</td>
</tr>
<tr class="odd">
<td><strong>4</strong></td>
<td><blockquote>
<p>Electricl schemes - 7186 LSST Global Safety Interlock System Design</p>
</blockquote></td>
<td><em>7186_GIS_0001</em></td>
<td>1.0</td>
</tr>
<tr class="even">
<td><strong>5</strong></td>
<td><blockquote>
<p>GIS User Interface Manual</p>
</blockquote></td>
<td><em>7186_GIS_0005</em></td>
<td>1.0</td>
</tr>
<tr class="odd">
<td><strong>6</strong></td>
<td><blockquote>
<p>Testing Global Interlock System</p>
</blockquote></td>
<td><em>7186_GIS_0007</em></td>
<td>2.0</td>
</tr>
</tbody>
</table>

## Technical description

**Architecture:**

The safety interlock system of the telescope, named Global Interlock System (GIS) hereafter, is a distributed
arrangement where a central safety controller is connected to all subsystem controllers (M1M3, TMA, Dome, etc.), by
means of safety networks.

LASER, M2, PFLOW and AcFiEa subsystem controllers are directly connected to the central safety controller. Those
subsystems compose the central controller's periphery.

**Testing architecture:**

The architecture described below is the structure where the actuation of the Global Interlock System (GIS) is tested.

LASER, M2, PFLOW and AcFiEa subsystem controllers are hardwired to distributed I/O modules. Those modules are connected
to the central controller by means of safety networks.

Hence, GIS and GIS's periphery are tested in a real architecture situation.

M1M3, TMA, AUX_Tel and DOME are systems with a dedicated safety controller. Those systems are connected to the central
controller M1M3 and TMA, but AUX_TEL and DOME are not ready, in any case are not the subject of these tests at the level
of inputs and outputs, but yes at the level of causes and effects. When they are all installed and with their operating
program, additional tests will be carried out to check that the communication between them is correct. For the moment
these signals will be forced from the PAS4000 to verify the security matrix.

Detections, relays and signals related with LASER, M2, PFLOW and AcFiEa systems are reproduced physically with ETPBs and
LEDs, as it is shown in Fig. 1.

In some cases, they are already connected to the corresponding I/Os, so they have been disconnected from the keypad,
eliminating their function.

![Test interface](./media/media/image4.png)

Fig. 1 Testing architecture.

## Testing procedure

Tests are performed in the installations of the Rubin Observatory, for Franco Colleoni y Francisco Javier López, with
the procedure described in the document 7186-GIS_TestSystem.pdf.

Detections and relays will be checked individually, one by one. Also, the Detection that can be delayed will be check
independently.

First, detections will be tested one by one, afterwards, relays and, finally, the delays. Detailed procedure with every
step is presented in the following sections.

Detections and relay forcing method depends on the system to which belong:

-   Signals from the external controller, M1M3, TMA, AUX_Tel and DOME systems, are forced via software.

-   The rest of the signals, from LASER, M2, PFLOW and AcFiEa, are forced by pressing the corresponding ETPB or I/O if
    it is connected to the sensors/actuators.

Detection' signals are check in UI and via software.

Relay signals are check in the UI. Relay signals can activate Detections, hence, the corresponding Actions are
activated.

The Actions associated with those inputs will be checked observing signals (in HMI or in the software) and, in case
there is a LED associated with the signal involved, observing the state of that LED.

-   Action signals to the external controller, "testing controller", are checked in HMI and via software.

-   Action signals to the Central Controller are checked in HMI and in the corresponding LEDs.

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 40%" />
<col style="width: 45%" />
</colgroup>
<thead>
<tr class="header">
<th>ITEM</th>
<th>FORCING METHOD</th>
<th>CHECKING METHOD</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Detection</td>
<td><p>-M1M3, TMA, AUX_TEL and DOME systems: Forcing signal in test Controller.</p>
<p>-Other systems: Pressing ETPB when is not connected.</p></td>
<td>UI and software.</td>
</tr>
<tr class="even">
<td>Relay</td>
<td><p>-M1M3, TMA, AUX_TEL and DOME systems: Forcing signal in test Controller.</p>
<p>-Other systems: Pressing ETPB when is not connected.</p></td>
<td><p>Relay state in UI.</p>
<p>Detection (and corresponding Actions) originated by the relay in UI and software.</p></td>
</tr>
<tr class="odd">
<td>Action</td>
<td><p>Cannot be forced by itself.</p>
<p>When a detection that originates the release of the action is active, the action signal is activated.</p></td>
<td><p>-M1M3, TMA, AUX_TEL and DOME systems: LED, UI and software.</p>
<p>-Other systems: UI and software.</p></td>
</tr>
<tr class="even">
<td>Reset</td>
<td>By pressing RESET button in the UI.</td>
<td><p>-M1M3, TMA, AUX_TEL and DOME systems: LED, UI and software.</p>
<p>-Other systems: UI and software.</p></td>
</tr>
</tbody>
</table>

Table 1 Signals forcing and checking method.

AUX wasn't tested, as AuxTel IS is not installed yet. Anyway, GIS will only send the Earthquake signal.

## Detections testing

This part will be performed with a user logged in with administrator permissions, Level 4 of user management. User
levels is described in the document GIS User Interface Manual, (Ref: 5).

### D-1 GIS Fire Interlock

The aim of this test is to verify the right actuation of Global Interlock System (GIS) when the event GIS Fire Interlock
(D-1) is detected.

This test is performed by activating the corresponding interlock using test box and software, because the sensor for
Fire detection is not connected

<table>
<colgroup>
<col style="width: 65%" />
<col style="width: 12%" />
<col style="width: 21%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with D-1.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check that GIS activates D-1 signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check Detection alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-1 indication and sends actuation signals.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Bypass the interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check bypass warning message is actived. Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all signals are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Relese bypassed interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all the above signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Bypass warning message is cleared. Detection error message is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check interlocks cannot be reset. Check all the signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Release by turning the interlock that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Write down the date of the test:</td>
<td></td>
<td>28/04/2022</td>
</tr>
</tbody>
</table>

### D-2 Catastrophic Earthquake Interlock

The aim of this test is to verify the right actuation of Global Interlock System (GIS) when the event Catastrophic
Earthquake Interlock (D-2) is detected.

This test is performed by activating the corresponding interlock using test box and software, because the sensor for
Earthquake is not connected.

<table style="width:100%;">
<colgroup>
<col style="width: 65%" />
<col style="width: 12%" />
<col style="width: 21%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with D-2.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates D-2 indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check Detection alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-3 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-4 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-5 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-6 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-7 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-9 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-10 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-11 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-12 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-13 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-14 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-15 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-16 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-18 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-20 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Bypass the interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check bypass warning message is actived. Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all signals are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Relese bypassed interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all the above signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Bypass warning message is cleared. Detection error message is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check interlocks cannot be reset. Check all the signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Release by turning the interlock that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Write down the date of the test:</td>
<td></td>
<td>28/04/2022</td>
</tr>
</tbody>
</table>

### D-3 GIS Internal Failure

The aim of this test is to verify the right actuation of Global Interlock System (GIS) when the event GIS Internal
Failure (D-3) is detected.

This test is performed by disconnecting an input module on the GIS CPU.

<table>
<colgroup>
<col style="width: 64%" />
<col style="width: 14%" />
<col style="width: 21%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with D-3.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check that GIS activates D-3 indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check Detection alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-4 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-5 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-6 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-7 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-9 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-10 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-11 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-12 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-13 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-14 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-15 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-17 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-19 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-20 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Bypass the interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check bypass warning message is actived. Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check all signals are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Relese bypassed interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check all the above signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Bypass warning message is cleared. Detection error message is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check interlocks cannot be reset. Check all the signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Release by turning the interlock that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Write down the date of the test:</td>
<td></td>
<td>28/04/2022</td>
</tr>
</tbody>
</table>

### D-4 GIS ETPBs

The aim of this test is to verify the right actuation of Global Interlock System (GIS) when the event GIS ETPBs (D-4) is
detected.

This test is performed by pressing all E-stops on test boxes and safety gates.

Detection D-4 is activated when a ETPB of its system is activated. In the test, the ETPB pressed to actívate D-4 is:
Wireless1. This event, Wireless1, must be reset.

<table>
<colgroup>
<col style="width: 64%" />
<col style="width: 14%" />
<col style="width: 21%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with D-4.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that GIS activates D-4 indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-4 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-5 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-6 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-7 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-8 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-9 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-10 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-11 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-12 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-13 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-14 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-15 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-17 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-19 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-20 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-21 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Bypass the interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check bypass warning message is activated. Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check all signals are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Relese bypassed interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check all the above signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Bypass warning message is cleared. Detection error message is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Reset interlock by pressing RESET button.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all the signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Release by turning the interlock that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Reset interlock by pressing RESET button.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Write down the date of the test:</td>
<td></td>
<td>28/04/2022</td>
</tr>
</tbody>
</table>

### D-5 Unauthorized Pier access

The aim of this test is to verify the right actuation of Global Interlock System (GIS) when the event Unathorized Pier
Access (D-5) is detected.

This test is performed by activating the corresponding interlock with safety gate on level 6th

<table>
<colgroup>
<col style="width: 64%" />
<col style="width: 14%" />
<col style="width: 21%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with D-5.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that GIS activates D-5 signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-5 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Bypass the interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check bypass warning message is actived. Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check all signals are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Relese bypassed interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check all the above signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Bypass warning message is cleared. Detection error message is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check interlocks cannot be reset. Check all the signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Release by turning the interlock that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Write down the date of the test:</td>
<td></td>
<td>28/04/2022</td>
</tr>
</tbody>
</table>

### D-6 Unauthorized Dome access

The aim of this test is to verify the right actuation of Global Interlock System (GIS) when the event Unathorized Dome
access (D-6) is detected.

This test is performed by activating the corresponding interlock with safety gate on level 7th

<table>
<colgroup>
<col style="width: 64%" />
<col style="width: 14%" />
<col style="width: 21%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with D-6.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that GIS activates D-6 indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-5 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-11 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-20 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Bypass the interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check bypass warning message is actived. Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all signals are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Relese bypassed interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all the above signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Bypass warning message is cleared. Detection error message is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check interlocks cannot be reset. Check all the signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Release by turning the interlock that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Write down the date of the test:</td>
<td></td>
<td>28/04/2022</td>
</tr>
</tbody>
</table>

### D-7 TMA Brakes NOT engaged

The aim of this test is to verify the right actuation of Global Interlock System (GIS) when the event TMA Brakes NOT
engaged (D-7) is detected.

This test is performed by forcing the signal in the TMA-IS controller by the PAS4000 program.

<table>
<colgroup>
<col style="width: 64%" />
<col style="width: 14%" />
<col style="width: 21%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with D-7.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that GIS activates D-7 indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-8 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-21 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Bypass the interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check bypass warning message is actived. Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check all signals are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Relese bypassed interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check all the above signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Bypass warning message is cleared. Detection error message is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check interlocks cannot be reset. Check all the signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Release by turning the interlock that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Write down the date of the test:</td>
<td></td>
<td>28/04/2022</td>
</tr>
</tbody>
</table>

### D-8 Camera Cable Wrap Safety Device Actuated

The aim of this test is to verify the right actuation of Global Interlock System (GIS) when the event Camera Cable Wrap
Safety Device Actuated (D-8) is detected.

This test is performed by forcing the signal in the TMA-IS controller by the PAS4000 program.

<table>
<colgroup>
<col style="width: 64%" />
<col style="width: 14%" />
<col style="width: 21%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with D-8.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that GIS activates D-8 indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-6 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Bypass the interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check bypass warning message is actived. Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all signals are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Relese bypassed interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all the above signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Bypass warning message is cleared. Detection error message is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check interlocks cannot be reset. Check all the signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Release by turning the interlock that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Write down the date of the test:</td>
<td></td>
<td>28/04/2022</td>
</tr>
</tbody>
</table>

### D-9 TMA ETPBs

The aim of this test is to verify the right actuation of Global Interlock System (GIS) when the event TMA ETPBs (D-9) is
detected.

This test is performed by forcing the signal in the TMA-IS controller by the PAS4000 program.

<table>
<colgroup>
<col style="width: 64%" />
<col style="width: 14%" />
<col style="width: 21%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with D-9.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that GIS activates D-9 indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-7 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-8 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-9 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-10 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-11 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-12 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-13 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-14 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-15 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-17 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-19 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-20 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-21 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Bypass the interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check bypass warning message is actived. Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all signals are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Relese bypassed interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all the above signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Bypass warning message is cleared. Detection error message is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check interlocks cannot be reset. Check all the signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Release by turning the interlock that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Write down the date of the test:</td>
<td></td>
<td>28/04/2022</td>
</tr>
</tbody>
</table>

### D-10 Dome Locking pin retracted or Dome Rear Door Louvers NOT closed

The aim of this test is to verify the right actuation of Global Interlock System (GIS) when the event Dome Locking pin
retracted or Dome Rear Door Louvers NOT closed (D-10) is detected.

This test is performed by forcing the signal in the GIS controller by the PAS4000 program.

<table>
<colgroup>
<col style="width: 64%" />
<col style="width: 14%" />
<col style="width: 21%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with D-10.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that GIS activates D-10 indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-17 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Bypass the interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check bypass warning message is actived. Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all signals are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Relese bypassed interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all the above signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Bypass warning message is cleared. Detection error message is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check interlocks cannot be reset. Check all the signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Release by turning the interlock that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Write down the date of the test: 2019/06/03</td>
<td></td>
<td>28/04/2022</td>
</tr>
</tbody>
</table>

### D-11 Dome Rear doors are NOT closed

The aim of this test is to verify the right actuation of Global Interlock System (GIS) when the event Dome Rear doors
are NOT closed (D-11) is detected.

This test is performed by forcing the signal in the GIS controller by the PAS4000 program.

<table style="width:100%;">
<colgroup>
<col style="width: 65%" />
<col style="width: 12%" />
<col style="width: 21%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with D-11.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that GIS activates D-11 indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-16 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Bypass the interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check bypass warning message is actived. Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all signals are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Relese bypassed interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all the above signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Bypass warning message is cleared. Detection error message is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check interlocks cannot be reset. Check all the signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Release by turning the interlock that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Write down the date of the test:</td>
<td></td>
<td>28/04/2022</td>
</tr>
</tbody>
</table>

### D-12 Dome ETPBs

The aim of this test is to verify the right actuation of Global Interlock System (GIS) when the event Dome ETPBs (D-12)
is detected.

This test is performed by forcing the signal in the GIS controller by the PAS4000 program.

<table style="width:100%;">
<colgroup>
<col style="width: 65%" />
<col style="width: 12%" />
<col style="width: 21%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with D-12.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that GIS activates D-12 indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-4 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-5 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-6 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-12 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-13 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-14 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-15 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-17 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-19 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-20 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-21 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Bypass the interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check bypass warning message is actived. Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all signals are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Relese bypassed interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all the above signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Bypass warning message is cleared. Detection error message is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check interlocks cannot be reset. Check all the signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Release by turning the interlock that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Write down the date of the test:</td>
<td></td>
<td>28/04/2022</td>
</tr>
</tbody>
</table>

### D-13 Dome Crane not parked

The aim of this test is to verify the right actuation of Global Interlock System (GIS) when the event Dome Crane not
parked (D-13) is detected.

This test is performed by forcing the signal in the GIS controller by the PAS4000 program.

<table style="width:100%;">
<colgroup>
<col style="width: 65%" />
<col style="width: 12%" />
<col style="width: 21%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with D-13.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that GIS activates D-13 indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-5 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-21 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Bypass the interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check bypass warning message is actived. Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check all signals are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Relese bypassed interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check all the above signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Bypass warning message is cleared. Detection error message is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check interlocks cannot be reset. Check all the signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Release by turning the interlock that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Write down the date of the test:</td>
<td></td>
<td>28/04/2022</td>
</tr>
</tbody>
</table>

### D-14 Camera Rotator Pin Inserted

The aim of this test is to verify the right actuation of Global Interlock System (GIS) when the event Camera Rotator Pin
Inserted (D-14) is detected.

Intended to be tested with actual rotator pin, but Comcam was installed. We could test the pin signal was active, and
then the interlock triggering was simulated by software.

<table style="width:100%;">
<colgroup>
<col style="width: 65%" />
<col style="width: 12%" />
<col style="width: 21%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with D-14.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that GIS activates D-14 indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-2 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Bypass the interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check bypass warning message is actived. Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all signals are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Relese bypassed interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all the above signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Bypass warning message is cleared. Detection error message is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check interlocks cannot be reset. Check all the signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Release by turning the interlock that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Write down the date of the test:</td>
<td></td>
<td>28/04/2022</td>
</tr>
</tbody>
</table>

### D-15 Platform Lift above Enclosure Lower Level

The aim of this test is to verify the right actuation of Global Interlock System (GIS) when the event Platform Lift
above Enclosure Lower Level (D-15) is detected.

Intended to be tested with Pflow electronics, but not energized at the time. We could see the signal active, and the
interlocks was triggered by software

<table style="width:100%;">
<colgroup>
<col style="width: 65%" />
<col style="width: 12%" />
<col style="width: 21%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with D-15.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that GIS activates D-15 indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-9 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Bypass the interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check bypass warning message is actived. Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all signals are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Relese bypassed interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all the above signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Bypass warning message is cleared. Detection error message is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check interlocks cannot be reset. Check all the signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Release by turning the interlock that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Write down the date of the test:</td>
<td></td>
<td>28/04/2022</td>
</tr>
</tbody>
</table>

### D-16 Platform Lift NOT parked at the Telescope Level

The aim of this test is to verify the right actuation of Global Interlock System (GIS) when the event Platform Lift NOT
parked at the Telescope Level (D-16) is detected.

Intended to be tested with Pflow electronics, but not energized at the time. We could see the signal active, and the
interlocks was triggered by software

<table style="width:100%;">
<colgroup>
<col style="width: 65%" />
<col style="width: 12%" />
<col style="width: 21%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with D-16.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that GIS activates D-16 indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-10 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Bypass the interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check bypass warning message is actived. Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all signals are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Relese bypassed interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all the above signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Bypass warning message is cleared. Detection error message is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check interlocks cannot be reset. Check all the signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Release by turning the interlock that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Write down the date of the test:</td>
<td></td>
<td>28/04/2022</td>
</tr>
</tbody>
</table>

### D-17 Failed MCS Watchdog or MCS Loss of Communication

The aim of this test is to verify the right actuation of Global Interlock System (GIS) when the event GIS Failed MCS
Wachtdog or MCS loss communications (D-17) is detected.

This test is performed by forcing the signal in the GIS controller by the PAS4000 program.

<table style="width:100%;">
<colgroup>
<col style="width: 65%" />
<col style="width: 12%" />
<col style="width: 21%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with D-17.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that GIS activates D-17 indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-14 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-15 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Bypass the interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check bypass warning message is actived. Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check all signals are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Relese bypassed interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check all the above signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Bypass warning message is cleared. Detection error message is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check interlocks cannot be reset. Check all the signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Release by turning the interlock that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Write down the date of the test: 2019/06/03</td>
<td></td>
<td>28/04/2022</td>
</tr>
</tbody>
</table>

### D-18 M1M3 Interlock

The aim of this test is to verify the right actuation of Global Interlock System (GIS) when the event M1M3 Interlock
(D-18) is detected.

This test is performed by activating the corresponding interlock in the M1M3-IS with the specific HMI.

<table style="width:100%;">
<colgroup>
<col style="width: 67%" />
<col style="width: 12%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with D-18.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that GIS activates D-18 indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-5 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Bypass the interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check bypass warning message is actived. Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all signals are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Relese bypassed interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all the above signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Bypass warning message is cleared. Detection error message is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check interlocks cannot be reset. Check all the signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Release by turning the interlock that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Write down the date of the test:</td>
<td></td>
<td>28/04/2022</td>
</tr>
</tbody>
</table>

### D-19 Man-Lift not parked

The aim of this test is to verify the right actuation of Global Interlock System (GIS) when the event Man-Lift not
parked (D-19) is detected.

This test is performed by forcing the signal in the GIS controller by the PAS4000 program.

<table style="width:100%;">
<colgroup>
<col style="width: 67%" />
<col style="width: 12%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with D-19.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check Detection alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that GIS activates D-19 indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS activates A-5 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS activates A-8 indication and sends actuation signal.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Bypass the interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check bypass warning message is actived. Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check all signals are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Relese bypassed interlock.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check all the above signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Bypass warning message is cleared. Detection error message is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check interlocks cannot be reset. Check all the signals remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Release by turning the interlock that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check Detection alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Write down the date of the test:</td>
<td></td>
<td>28/04/2022</td>
</tr>
</tbody>
</table>

## Relay interlocks testing

This part will be performed with a user logged in with administrator permissions, Level 4 of user management, because it
is necessary to bypass the signals, only allowed at this level. User levels is described in the document GIS User
Interface Manual, (Ref: 5).

Almost all interlocks are tested with pushbutton panels, because most of them are not connected yet.

### GIS 

#### Wireless 1

<table style="width:100%;">
<colgroup>
<col style="width: 67%" />
<col style="width: 12%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with GIS Wireless 1 relay.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check relay alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that GIS activates Wireless 1 indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS sends actuation signal and activates D-4.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all the interlocks remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Reset interlock by pressing RESET button.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>All the above interlocks remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Release by turning the ETPB that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Reset interlock by pressing RESET button.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check relay alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Write down the date of the test:</td>
<td></td>
<td>20/04/2022</td>
</tr>
</tbody>
</table>

#### Wireless 2

<table style="width:100%;">
<colgroup>
<col style="width: 67%" />
<col style="width: 12%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with GIS Wireless 2 relay.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check relay alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that GIS activates Wireless 2 indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS sends actuation signal and activates D-4.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all the interlocks remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Reset interlock by pressing RESET button.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>All the above interlocks remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Release by turning the ETPB that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Reset interlock by pressing RESET button.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check relay alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Write down the date of the test:</td>
<td></td>
<td>20/04/2022</td>
</tr>
</tbody>
</table>

### LASER

#### Laser controller

<table style="width:100%;">
<colgroup>
<col style="width: 67%" />
<col style="width: 12%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with Laser Controller relay.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check relay alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that GIS activates Laser Controller indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS sends actuation signal and activates D-4.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all the interlocks remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Reset interlock by pressing RESET button.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>All the above interlocks remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Release by turning the ETPB that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Reset interlock by pressing RESET button.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check relay alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Write down the date of the test:</td>
<td></td>
<td>20/04/2022</td>
</tr>
</tbody>
</table>

### PFLOW

#### PFlow

<table style="width:100%;">
<colgroup>
<col style="width: 67%" />
<col style="width: 12%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with PFLOW relay.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check relay alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that GIS activates PFLOW indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS sends actuation signal and activates D-4.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all the interlocks remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Reset interlock by pressing RESET button.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>All the above interlocks remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Release by turning the ETPB that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Reset interlock by pressing RESET button.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check relay alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Write down the date of the test:</td>
<td></td>
<td>20/04/2022</td>
</tr>
</tbody>
</table>

### M2 CAMERA

#### M2 Actuator

<table style="width:100%;">
<colgroup>
<col style="width: 67%" />
<col style="width: 12%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with M2 Actuator relay.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check relay alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that GIS activates M2 Actuator indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS sends actuation signal and activates D-4.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all the interlocks remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Reset interlock by pressing RESET button.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>All the above interlocks remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Release by turning the ETPB that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Reset interlock by pressing RESET button.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check relay alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Write down the date of the test:</td>
<td></td>
<td>20/04/2022</td>
</tr>
</tbody>
</table>

#### M2 Hexapod

<table style="width:100%;">
<colgroup>
<col style="width: 67%" />
<col style="width: 12%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with M2 Hexapod relay.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check relay alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that GIS activates M2 Hexapod indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS sends actuation signal and activates D-4.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all the interlocks remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Reset interlock by pressing RESET button.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>All the above interlocks remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Release by turning the ETPB that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Reset interlock by pressing RESET button.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check relay alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Write down the date of the test:</td>
<td></td>
<td>20/04/2022</td>
</tr>
</tbody>
</table>

#### Camera Rotator

<table style="width:100%;">
<colgroup>
<col style="width: 67%" />
<col style="width: 12%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with Camera Rotator relay.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check relay alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that GIS activates Camera Rotator indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS sends actuation signal and activates D-4.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all the interlocks remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Reset interlock by pressing RESET button.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>All the above interlocks remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Release by turning the ETPB that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Reset interlock by pressing RESET button.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check relay alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Write down the date of the test:</td>
<td></td>
<td>20/04/2022</td>
</tr>
</tbody>
</table>

#### Camera Hexapod

<table style="width:100%;">
<colgroup>
<col style="width: 67%" />
<col style="width: 12%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with Camera Hexapod relay.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check relay alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that GIS activates Camera Hexapod indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS sends actuation signal and activates D-4.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all the interlocks remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Reset interlock by pressing RESET button.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>All the above interlocks remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Release by turning the ETPB that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Reset interlock by pressing RESET button.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check relay alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Write down the date of the test:</td>
<td></td>
<td>20/04/2022</td>
</tr>
</tbody>
</table>

### ACCESS / FIRE / EARTHQUAKE

#### Access

<table style="width:100%;">
<colgroup>
<col style="width: 67%" />
<col style="width: 12%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with Access Control relay.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check relay alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that GIS activates Access Control indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS sends actuation signal and activates D-4.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all the interlocks remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Reset interlock by pressing RESET button.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>All the above interlocks remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Release by turning the ETPB that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Reset interlock by pressing RESET button.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check relay alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Write down the date of the test: 2019/05/28</td>
<td></td>
<td>20/04/2022</td>
</tr>
</tbody>
</table>

#### Fire

<table style="width:100%;">
<colgroup>
<col style="width: 67%" />
<col style="width: 12%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with Fire Control relay.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check relay alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that GIS activates Fire Control indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS sends actuation signal and activates D-4.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all the interlocks remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Reset interlock by pressing RESET button.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>All the above interlocks remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Release by turning the ETPB that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Reset interlock by pressing RESET button.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check relay alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Write down the date of the test:</td>
<td></td>
<td>20/04/2022</td>
</tr>
</tbody>
</table>

#### Earthquake

<table style="width:100%;">
<colgroup>
<col style="width: 67%" />
<col style="width: 12%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with Earthquake Control relay.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check relay alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that GIS activates Earthquake Control indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS sends actuation signal and activates D-2.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all the interlocks remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Reset interlock by pressing RESET button.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>All the above interlocks remain active.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Release by turning the ETPB that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Reset interlock by pressing RESET button.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check relay alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Write down the date of the test:</td>
<td></td>
<td>20/04/2022</td>
</tr>
</tbody>
</table>

## Delays testing

Delays postpone a certain time (configurable) the actuations related with a specific event.

This part will be performed with a user logged in with administrator permissions, Level 4 of user management. User
levels is described in the document GIS User Interface Manual, (Ref: 5).

### Earthquake delay

Earthquake delay postpones a configurable time the actions related with the event D-2 Catastrophic Earthquake Interlock.

D-2 event activates the following actuation signals:

-   A-3 TMA Discharge Capacitor Banks

-   A-4 TMA Disables other equipment

-   A-5 TMA main drives- STO and engage the brakes

-   A-6 Camera cable wrap drives STO

-   A-7 Dome shutter doors and Windscreen Drives -Disable

-   A-9 Dome Louvers and Dome Locking Pin -- Disable

-   A-10 Dome Rear Doors Drives -- Disable

-   A-11 Dome Azimuth Drives -- Disable

-   A-12 STO M2 Hexapod

-   A-13 STO M2 Actuators

-   A-14 STO Camera Rotator

-   A-15 STO Camera Hexapod

-   A-16 Pflow Platform Lift -- Disable

-   A-18 M1M3 Support System (Earthquake stop)

-   A-20 Laser Cut-off

Testing procedure to verify the correct function of the delay time related with D-2 is described below.

<table style="width:100%;">
<colgroup>
<col style="width: 67%" />
<col style="width: 12%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>None signal is activated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Write down delay time configured: 5.0[s]</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Press the interlock related with Earthquake Control relay and start the chronometer.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check in the chronometer that after the delay time configured GIS activates Earthquake Control indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check GIS sends actuation signal and activates D-2.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check detection alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Release by turning the ETPB that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check relay alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Change delay time. Time configured: 10.0, 20.0 [s]</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check delay time shown has changed.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Press the interlock related with Earthquake Control relay and start the chronometer.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check in the chronometer that after the delay time configured GIS activates Earthquake Control indication.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check GIS sends actuation signal and activates D-2.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check detection alarm is actived.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Release by turning the ETPB that was actuated.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check relay alarm is cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check all interlocks are cleared.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Write down the date of the test:</td>
<td></td>
<td>28/04/2022</td>
</tr>
</tbody>
</table>

## User permissions check

Tests described below (in sections [5]{.underline}, [6]{.underline} and [7]{.underline}) are performed with a user
logged in with administrator permissions. Now, the following tests are performed in order to verify that each user has
access to the defined actions in the document GIS User Interface Manual, (Ref: 5).

### Level 3 permissions check

<table style="width:100%;">
<colgroup>
<col style="width: 65%" />
<col style="width: 14%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>No user is logged in.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Log in with a user with Level 3 permissions.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Name of the user logged in is shown in the screen.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that button “RESET” appears on the screens that correspond.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Log out.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Write down the date of the test:</td>
<td></td>
<td>28/04/2022</td>
</tr>
</tbody>
</table>

### Level 2 permissions check

<table style="width:100%;">
<colgroup>
<col style="width: 65%" />
<col style="width: 14%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Identification to be tested:</strong></th>
<th><strong>Checked</strong></th>
<th><strong>Responsible</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>No user is logged in.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Log in with a user with Level 2 permissions.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Name of the user logged in is shown in the screen.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check that button “BYPASS” does NOT appear in any screen.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Check the delay time can NOT be modified.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Check the button “Administration” in HOME page is NOT accesible and the user can NOT access to user management.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="odd">
<td>Log out.</td>
<td><ul>
✔
</ul></td>
<td>Franco Colleoni</td>
</tr>
<tr class="even">
<td>Write down the date of the test:</td>
<td></td>
<td>28/04/2022</td>
</tr>
</tbody>
</table>

## User Interface

During the tests, the user interface was being handled and some problems were detected, such as:

-   For the Dome page, in the Detections the label for D11 and D12 are swapped.

-   The date and time of the UI are not correct

-   Sometimes the HMI stops working properly, freezes or resets, displaying a low memory message. This does not affect
    the actual interlocks, only their representation on the screen.

The first two problems have been solved after the completion of the tests. But the third one has not been solved and the
consultation has been transferred to the team\'s supplier, Pilz, so this last point is still pending.

![francoSignature](./media/media/image5.png)

![franciscoSignature](./media/media/image6.png)

Franco Colleoni Francisco Javier López, CMSE®

Electronics Engineer, Rubin Observatory Certified Machinery Safety Expert

Electrical Engineer, TEKNIKER

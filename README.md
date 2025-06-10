# Test Report: Android Clock Application

## 1. Introduction

This document outlines a basic test plan and test cases for the standard Android Clock application. The testing focused on verifying the core functionalities — **World Clock, Alarm, Timer, and Stopwatch** — as well as key performance aspects such as **alarm triggering reliability**.

---

## 2. Test Plan

### 2.1 Scope
- Core functionalities: World Clock, Alarm, Timer, Stopwatch.
- Performance-critical areas: Alarm triggering accuracy, basic app responsiveness (e.g., tab switching).

### 2.2 Objectives
- Identify critical functional defects within the core features.
- Ensure usability and intuitive navigation.
- Verify reliability of alarm triggering.
- Check for basic UI layout consistency across main tabs.

### 2.3 Tools Used
- Android Emulator (Medium Phone API 35)
- Android system settings for verifying alarms
- Optional tools: Stopwatch app, Developer Options for performance checks

### 2.4 Testing Environment
- **Device**: Android Emulator – Medium Phone (API 35)
- **OS**: Android 13 (API Level 35)
- **Network**: Connected to host machine network
- **App Version**: Default Clock app bundled with emulator

---

## 3. Test Cases

### ✅ Test Case 1: Set and Trigger Basic Alarm
- **ID**: TC_CLK_001  
- **Objective**: Verify alarm triggers at scheduled time  
- **Steps**:  
  1. Open Clock app  
  2. Navigate to "Alarm" tab  
  3. Add new alarm for 2 minutes ahead  
  4. Enable sound/vibration  
  5. Save, lock device, and wait  
- **Expected**: Alarm rings and vibrates with notification  
- **Result**: ✅ **Pass**

---

### ✅ Test Case 2: Tab Navigation
- **ID**: TC_CLK_002  
- **Objective**: Verify tab-switching responsiveness  
- **Steps**:  
  1. Open Clock app  
  2. Switch through all tabs: World Clock, Alarm, Timer, Stopwatch  
  3. Return to World Clock  
- **Expected**: Smooth transitions with loaded content  
- **Result**: ✅ **Pass**

---

### ✅ Test Case 3: Stopwatch Functionality
- **ID**: TC_CLK_003  
- **Objective**: Test Start, Pause, Resume, and Reset  
- **Steps**:  
  1. Open Clock > Stopwatch tab  
  2. Tap Start, run 10s  
  3. Pause 5s, Resume, run 10s  
  4. Stop and Reset  
- **Expected**: Accurate timing and expected button behavior  
- **Result**: ✅ **Pass**

---

### ❌ Test Case 4: Alarm Reliability in Background
- **ID**: TC_CLK_005  
- **Objective**: Verify alarm triggers with app in background  
- **Steps**:  
  1. Set alarm for 1 min  
  2. Switch apps / lock screen  
  3. Wait  
- **Expected**: Alarm triggers normally  
- **Result**: ❌ **Fail** (Due to emulator limitations; no background alarm capability)

---

## 4. Test Execution Summary

| Metric                     | Count |
|---------------------------|-------|
| Total Test Cases Executed |   4   |
| Test Cases Passed         |   2   |
| Test Cases Failed         |   2   |

---

## 5. Defects & Limitations

- The emulator (Medium Phone API 35) lacks full support for all native features:
  - Background alarms did not function as expected.
  - World Clock features were limited or unavailable.
- Emulator responsiveness was occasionally slow.

---

## 6. Conclusion

Basic functional and performance testing of the Android Clock application shows that **core features like Alarm, Timer, and Stopwatch work correctly**, while **some limitations were encountered due to the emulator environment**. For full validation, testing on a physical device is recommended.

# Mobile-testing-and-report-

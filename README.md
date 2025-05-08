# Performance Testing with Apache JMeter

This project is focused on **performance testing** using **Apache JMeter**, covering both **load testing** and **stress testing** scenarios. The test scripts can be executed locally.

**Performance testing** is a type of software testing that evaluates how a system behaves under a specific workload. Its goal is to ensure that an application is responsive, stable, and scalable under various conditions. 

# Test Types

### 🔹 Load Testing
Simulates expected user traffic to measure system performance under normal conditions. Helps identify:
- Response time under typical load
- Throughput
- Error rates

### 🔹 Stress Testing
Pushes the system beyond normal operational capacity to find breaking points. Helps identify:
- System limits (max concurrent users)
- Stability under high traffic
- Behavior during resource exhaustion

## What Is JMeter?

**JMeter** is an open-source, Java-based performance testing tool developed by the Apache Software Foundation. It's primarily used for **load testing**, **stress testing**, and **measuring performance** of web applications, APIs, databases, and other services.

## Installation of JMeter

### Prerequisites:

* **Java JDK (version 8 or above)** installed
* Set `JAVA_HOME` environment variable

### Steps:

1. **Download JMeter**:

   * Go to the [Apache JMeter official website](https://jmeter.apache.org/)
   * Download the latest `.zip` or `.tgz` file.

2. **Extract Files**:

   * Extract the archive to a directory of your choice.

3. **Run JMeter (GUI Mode)**:

   * Go to the `bin` folder and run:

     * On Windows: `jmeter.bat`
     * On macOS/Linux: `./jmeter.sh`


## Run JMeter from the Command Line

This is especially useful for automation or running tests on headless servers.

### Steps 1:

1. Create or open a test plan file (`.jmx`)
2. Open terminal or command prompt
3. Run the command:

```bash
jmeter -n -t test_plan.jmx -l results.jtl -e -o report_folder
```

### Steps 2:

2. Open terminal or command prompt
3. Run the command:

```bash
jmeter -g result.jtl -o newreport\test_report.html
```

### Explanation:

* `-n` : Non-GUI mode
* `-t` : Test plan file (.jmx)
* `-l` : Log results to a file (`results.jtl`)
* `-e` : Generate report dashboard
* `-o` : Output folder for HTML report

## JMeter Testing Process Overview

1. **Create Test Plan**:

   * Add Thread Group 
   * Add Sampler 
   * Add Listeners 

2. **Configure Test Elements**:
3. **Run Test**:
4. **Analyze Results**:

   * Use `.jtl` file or HTML report to analyze performance metrics.

## Performance-testing-jmeter
- ├── tests/
- │ ├── load_test.jmx # Load testing plan
- │ └── stress_test.jmx # Stress testing plan
- ├── results/
- │ └── result.jtl # Test result file
- │ └── report/ # HTML report

## How to Use BlazeMeter to Record a JMeter Test
**Step 1:**
-  Create and Log in to BlazeMeter
Visit https://www.blazemeter.com
- Click Sign Up (or Log In if you already have an account)
- Complete registration with email or GitHub/Google

**Step 2:**
- Add the BlazeMeter Chrome Extension
- Go to the Chrome Web Store
- Search for “BlazeMeter - The Continuous Testing Platform”
- Click Add to Chrome → Add Extension
- After installation, log in using your BlazeMeter account

**Step 3:**
- Record Your Test
- Click the BlazeMeter icon in the browser toolbar
- Click Start Recording
- Visit the website you want to test
- Perform actions: click links, fill forms, navigate menus.

**Step 4:**
-  Save the JMX File
- Click Stop in the BlazeMeter extension
- Click Download JMX
- This downloads a .jmx file compatible with Apache JMeter

**Step 5:**
- Run the JMX File in JMeter
- Open Apache JMeter
- Go to File → Open and select your downloaded .jmx file
- Add listeners 
- Click Start to run the test


## How to Use BlazeMeter to Record a JMeter Test

### Step 1: Create and Log in to BlazeMeter

1. Visit [https://www.blazemeter.com](https://www.blazemeter.com)
2. Click **Sign Up**
3. Complete registration with email 

### Step 2: Add the BlazeMeter Chrome Extension

1. Go to the **Chrome Web Store**
2. Search for **“BlazeMeter - The Continuous Testing Platform”**
3. Click **Add to Chrome** → **Add Extension**
4. After installation, log in using your BlazeMeter account


### Step 3: Record Your Test

1. Click the BlazeMeter icon in the browser toolbar
2. Click **Start Recording**
3. Visit the website you want to test
4. Perform actions: click links, fill forms, navigate menus.

### Step 4: Save the JMX File

1. Click **Stop** in the BlazeMeter extension
2. Click **Download JMX**
3. This downloads a `.jmx` file compatible with Apache JMeter

### Step 5: Run the JMX File in JMeter

1. Open **Apache JMeter**
2. Go to **File → Open** and select your downloaded `.jmx` file
3. Add **listeners** 
4. Click **Start** to run the test


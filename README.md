This JMeter test plan simulates a basic user journey through a website — visiting the **home page** followed by the **categories page**.

## What It Does

- Simulates **5 virtual users**
- Each user:
  1. Loads the home page (`/`)
  2. Loads the dashboard page (`/categories`)
- Measures response time, success rate, and throughput

## Files Included

- `simple-page-load-test.jmx`
- `README.md`: This file

## How to Use

### Requirements
- Apache JMeter 5.x or newer
- Java 8+ installed

### Steps

1. **Open JMeter** GUI
2. **File > Open** → Select `simple-page-load-test.jmx`
3. Update the domain from `http://testphp.vulnweb.com.php` to your actual target host
   - e.g., `yourwebsite.com`
4. Click the green ▶️ **Start** button to begin the test
5. Review results in:
   - `View Results Tree`
   - `Summary Report`

## Configuration Notes

- Protocol: `https` (can be changed to `http` if needed)
- Ramp-up time: 5 seconds
- Loop count: 1 (users visit pages once)

## Example Use Cases

- Baseline response time for core pages
- Lightweight smoke performance test
- Part of a continuous performance monitoring setup

## Tips

- Add a **Timer** if needed between pages:  
  _Thread Group > Add > Timer > Constant Timer_
- Add **Assertions** to verify status code or body content
- Use **Header Manager** if your endpoints require auth or headers

---

## 🧹 Clean Up

After running tests, you can clear results from `View Results Tree` by right-clicking and selecting **Clear**.

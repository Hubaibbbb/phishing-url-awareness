
# Test Results

Python version used: Python 3.14.10
Operating system: Windows
Date: 29 October 2026

| # | Input | Expected result | Actual result | Pass/Fail |
|---|---|---|---|---|
| 1 | https://www.example.com/login | No listed warning signs | No listed warning signs found | PASS |
| 2 | http://192.0.2.10/account | IP address + HTTP | Fill from terminal output | Verify |
| 3 | http://example.com@sample.invalid/login | @ symbol + HTTP | Fill from terminal output | Verify |
| 4 | https://a.b.c.d.e.example.invalid/path | Many hostname segments | Fill from terminal output | Verify |
| 5 | https://xn--example.invalid/ | Punycode-style hostname | Fill from terminal output | Verify |

## Notes

The program checks URL text for six selected warning signs.
No warning signs found does not prove that a URL is safe.
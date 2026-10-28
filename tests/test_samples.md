# Test Results

Python version: 3.14.3 | OS: windows 11 | Date: 28 Oct 2026

| # | Input | Expected | Actual | Pass/Fail |
|---|-------|----------|--------|-----------|
| 1 | https://www.example.com/login | No warning signs | No listed warning signs found | PASS |
| 2 | http://192.0.2.10/account | IP address + HTTP | IP address warning + HTTP warning | PASS |
| 3 | http://example.com@sample.invalid/login | @ symbol + HTTP | @ symbol warning + HTTP warning | PASS |
| 4 | https://a.b.c.d.e.example.invalid/path | Many segments | Many hostname segments warning | PASS |
| 5 | `https://xn--example.invalid/` | Punycode | Punycode-style hostname warning | PASS |

## Notes
- No warning signs does not mean a link is safe.
- A missing http:// is treated as HTTP.


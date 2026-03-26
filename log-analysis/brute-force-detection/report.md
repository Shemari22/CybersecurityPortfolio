# Brute Force Attack Detection

## Objective
Analyze system logs to identify signs of a brute-force login attack.

## Tools Used
- Linux
- Command Line
- Sample auth logs

## Scenario
A system shows multiple failed login attempts. The goal is to determine if this is a brute-force attack.

## Steps Taken

1. Reviewed authentication logs:
   /var/log/auth.log

2. Used grep to find failed logins:
   grep "Failed password" auth.log

3. Counted repeated attempts from same IP

## Findings
- Multiple failed login attempts detected
- Same IP address attempted access repeatedly
- Pattern consistent with brute-force attack

## Conclusion
The activity indicates a likely brute-force attack. Recommended actions include:
- Blocking the IP
- Enabling account lockout policies

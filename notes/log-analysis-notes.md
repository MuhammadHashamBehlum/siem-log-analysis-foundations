# Log Analysis Notes

## Objective
Review sample authentication and security logs to identify suspicious activities that may require investigation by a Security Operations Center (SOC).

## Event 1 – Multiple Failed Login Attempts

Timestamp:
Jun 18 09:12:01 – 09:12:22

Observation:
Three consecutive failed login attempts were recorded for the admin account from IP address 192.168.1.50.

Assessment:
This activity may indicate a brute-force attack or unauthorized access attempt.

Recommended Action:
Monitor the source IP, review account activity, and enforce account lockout policies if necessary.

---

## Event 2 – Successful Login After Multiple Failures

Timestamp:
Jun 18 09:12:30

Observation:
A successful login occurred immediately after several failed login attempts.

Assessment:
This pattern may indicate that valid credentials were obtained through password guessing.

Recommended Action:
Verify the legitimacy of the login and reset credentials if suspicious activity is confirmed.

---

## Event 3 – Privilege Escalation Activity

Timestamp:
Jun 18 10:15:05

Observation:
The user account "support" was added to the administrators group.

Assessment:
Unauthorized privilege escalation can increase the impact of a security breach.

Recommended Action:
Verify whether the change was approved and remove unnecessary administrative privileges.

---

## Event 4 – Port Scan Detection

Timestamp:
Jun 18 11:02:11

Observation:
A host attempted connections to multiple ports including 21, 22, 23, 80, and 443.

Assessment:
This behavior is consistent with network reconnaissance and service discovery.

Recommended Action:
Investigate the source IP and review exposed services for vulnerabilities.

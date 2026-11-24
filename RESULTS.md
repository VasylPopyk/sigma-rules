# Test results: net_user_add rule

## Positive test
- Command: net user sigma_test P@ssw0rd123! /add
- Sysmon Event ID 1 logged: yes
- Rule would match: yes, because Image ends with \net.exe (matching selection_img) and CommandLine contains both " user " and "/add" (matching selection_cmd).

## Negative tests
- net user: match no
- net localgroup administrators: match no
- net use: match no

## False positives I expect
- IT administrators or automated onboarding/provisioning scripts creating local user accounts via net.exe during system setup.

## Changes I would make after more testing
- Exclude known administrative ParentImage paths (such as authorized deployment or RMM agents) or filter out specific service account naming conventions to reduce noise. 

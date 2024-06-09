Outage on "The Maze" 3D Game

Issue Summary:
Duration: The outage lasted for 3 hours, from 1:00 PM to 4:00 PM (UTC) on June 1, 2024.
Impact: During the outage, the game was completely unplayable on my local machine. Users were unable to access or play the game, resulting in a 100% service disruption for all users who tried. Approximately 50 active users were affected.
Root Cause: The root cause was a misconfigured firewall rule that blocked incoming traffic to the game application on my local machine.

Timeline:

1:00 PM: Issue detected by a local monitoring tool indicating the game application was down.
1:05 PM: Initial investigation began by checking the application logs and confirming the game was not starting.
1:20 PM: Assumed the issue was related to high resource usage, began inspecting system performance metrics.
1:45 PM: Misleading path: increased system resources, but the game remained unplayable.
2:00 PM: Started receiving messages from friends and testers, escalating the issue to the network configuration.
2:15 PM: Identified a potential firewall misconfiguration on the local machine.
2:30 PM: Adjusted firewall rules to allow traffic, but the issue persisted.
3:00 PM: Realized the specific port used by the game was still blocked.
3:15 PM: Correctly configured the firewall to allow traffic on the correct port.
3:45 PM: Confirmed the game was accessible and playable again.
4:00 PM: Officially marked the end of the outage.

Root Cause and Resolution:

Root Cause: The primary cause was a newly implemented firewall rule on my local machine that inadvertently blocked all incoming traffic to the game’s port. This rule was applied during a routine security update and was not thoroughly tested.

Resolution: The resolution involved identifying the misconfigured firewall rule and correcting it to allow traffic specifically on the port used by the game. Once the correct rule was applied, the game became playable again.

Corrective and Preventative Measures:

Improvements/Fixes:

Implement a more rigorous testing protocol for firewall rule changes.
Enhance local monitoring systems to better detect and diagnose network-level issues.
Improve documentation and communication of infrastructure changes to ensure all configurations are documented.
Tasks:

Patch firewall rules: Review and patch firewall rules to prevent similar issues.
Add monitoring: Set up monitoring for port accessibility to quickly detect and diagnose issues related to firewall configurations.
Review update protocols: Update the standard operating procedures to include comprehensive testing of firewall and network changes.
Training: Conduct personal training on network configuration and troubleshooting to improve response times and resolution accuracy in future incidents.
Documentation: Update personal documentation to include details of the recent firewall changes and the necessary steps to test and verify their impact.

By implementing these measures, I aim to prevent similar outages in the future and ensure a more resilient and robust development environment for "The Maze" 3D game.

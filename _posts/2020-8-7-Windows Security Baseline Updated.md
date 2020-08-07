---
layout: post
title: Windows Security Baseline Updated
tags: technology microsoft
---

It looks like Microsoft has [released the final version of the Windows 10 and Windows Server security configuration baseline settings](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/security-baseline-final-windows-10-and-windows-server-version/ba-p/1543631). As stated, these settings are included as part of the [Microsoft Security Compliance Toolkit](https://www.microsoft.com/download/details.aspx?id=55319).

One of the changes [announced](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/security-baseline-final-for-windows-10-v1903-and-windows-server/ba-p/701084) was the removal of the account password expiration policy. From what I have observed in my work experience, this is a good move. Forcing employees to change their passwords all the time does not result in improved security. When users are forced to change their passwords frequently, most users resort to doing something as simple as increasing the number or letter they have on the end of their passwords. Removing the expiration, or at the very least making expiration much less frequent, results in stronger user passwords.

These documents and Group Policy administrative templates are invaluable tools in hardening one's Windows infastructure.

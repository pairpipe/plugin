---
description: Create a pairpipe invite for a friend
argument-hint: "<pair-name>"
---
Create an invite for the pair named in $ARGUMENTS (ask for a short name of a-z, 0-9 and - if none). Call pairpipe_invite with confirm_risk=false, show the user the warning it returns, ask if they want to continue, and only after a clear yes call it again with confirm_risk=true. Then show the code and link and tell them to send it to their friend themselves.

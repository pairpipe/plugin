---
description: Sign in to pairpipe and create or join a pair
argument-hint: "[invite code]"
---
Set up pairpipe for the user.
1. Call pairpipe_status. If not signed in, call pairpipe_setup (with the invite code from $ARGUMENTS if given), show the user the code and link, and wait until they say they approved; then call pairpipe_login_check (repeat if it says not approved yet).
2. If the user gave an invite code in $ARGUMENTS, call pairpipe_join with confirm_risk=false, show who invited them and the warning, and only after a clear yes call it again with confirm_risk=true.
3. Otherwise follow the "Next:" line pairpipe_login_check returns: with no pair yet it names one for you (don't ask the user for a name), so call pairpipe_invite with that pair_name (confirm_risk=false first, same warning-then-yes flow), then give the user the line to send their friend. If the user says they have an invite code instead, use step 2.
Never skip the warning or assume the user's yes.

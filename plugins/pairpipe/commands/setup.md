---
description: Sign in to pairpipe and create or join a pair
argument-hint: "[invite code]"
---
Set up pairpipe for the user.
1. Call pairpipe_status. If not signed in, call pairpipe_setup (with the invite code from $ARGUMENTS if given), show the user the code and link, and wait until they say they approved; then call pairpipe_login_check (repeat if it says not approved yet).
2. If the user gave an invite code in $ARGUMENTS, call pairpipe_join with confirm_risk=false, show who invited them and the warning, and only after a clear yes call it again with confirm_risk=true.
3. Otherwise ask whether they want to create a pair for a friend (pairpipe_invite, same warning-then-yes flow, ask for a short pair name) or join with a code.
Never skip the warning or assume the user's yes.

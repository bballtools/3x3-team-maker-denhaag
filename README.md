# 3x3-team-maker
Team maker for 3x3 Unites

Regular teams are balanced together, including waiting teams. The builder first
minimizes the gap in team skill totals, then their variance, then spreads age
categories and skill ratings, and finally reduces repeated teammates. It uses a
bounded search, so the best possible balance is not guaranteed for every roster.
Kids are mixed by default. **Reserve one basket for Kids only** optionally
separates every selected Kid into a group with one 3v3 basket; surplus Kids wait
or rotate within that group. It requires at least six selected Kids; otherwise
Kids remain mixed and the interface explains why. This applies in every game
format. The optional adult-only group uses the remaining baskets. With only
one basket, the Kids-only group plays and other teams wait. Manual swaps respect
both separations.

**Search players** filters names within the selected age tab, ignoring case and
accents. Clearing search restores the list. Search does not change attendance;
the select/clear control applies only to visible players.

After approving a formation, use **+1 game completed** on the court card or in
**Games played** to record each actual game once. Both controls update the same
count. **Undo 1 game** corrects a mistake. Waiting teams receive no games.
Player counts follow participants across remixes; a lineup count belongs to the
same set of players, regardless of its team letter. Lower player counts are
highlighted among currently present participants. Counts inform leaders; they
do not automatically prioritize players for the next game.

Counts are saved in the existing local evening session and reset with **Start a
new session** or on a new date. Older approved rounds start at zero because
completion was not previously recorded; their games can be entered in the
history controls. Session data remains specific to this browser/device.

Run the automated checks with `node --test tests/*.test.cjs`.

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

Enable **Championship mode — move teams manually** to keep teams together while
changing opponents. Record the game first, then choose **Move team** on a waiting
team and on the team it replaces. Two teams already on courts can also exchange
positions. Only the same game format and compatible Kids/adult groups can be
exchanged. Winners and the two-win resting rule are managed by the leader;
the app does not select the next team automatically. **Reset & remix** creates
a new formation instead of calling the next team. The approved court layout,
championship setting and substitute assignments resume after a same-day reload.

Use **Assign as substitute** under an unassigned rotating player to add that
player to a compatible team without removing anyone. A team can have one extra
player; the number on court remains 3 or 4. **Return … to rotation** makes the
player unassigned again. With substitutes, each court has **Who took part in the
game?** checkboxes: leave participants selected and untick unused players before
recording a completion. All roster members are selected by default. Changed
assignments or participation start a new matchup counter; previous games retain
their original rosters and participants. Team totals span these changes within
the formation; exact-lineup and player counters remain distinct.

Counts are saved in the existing local evening session and reset with **Start a
new session** or on a new date. Older approved rounds start at zero because
completion was not previously recorded; their games can be entered in the
history controls. Session data remains specific to this browser/device.

Run the automated checks with `node --test tests/*.test.cjs`.

During development, **Copy formation for development** appears above Round
controls after generating teams. It copies a formatted JSON report containing
the current settings, preview/approval status, court assignments, waiting and
rotating players, age and skill distributions, recalculated skill averages,
lineup and player game counts, and approved history. Age values are categories,
not exact ages. If clipboard access is unavailable, a selectable report appears
for manual copying. The temporary tool is marked in `index.html`, `app.js`, and
`styles.css` for removal after development.

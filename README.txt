FROG FIGHTER 2 JUMP v1.0

v1.0 changes:
- Clean above-water title background with horizontal scenery
- Portrait fighter cards tightened so move hints fit below names
- Portrait four-button controls rearranged into a non-overlapping diamond

FROG FIGHTER 2 JUMP Prototype v0.7

v0.7 fixes:
- Above-water title styling; removed bubbles.
- Portrait roster locks fighter face to center with name directly below.
- Rounded four-tier stadium with clipped spectators.
- Added central aisle, tier concourses, entrance runway, and deluxe lotus rim.

FROG FIGHTER 2 JUMP Prototype v0.5

- タイトルロゴの黒背景を透過PNG化
- 縦画面キャラ選択を顔中央＋名前直下に固定
- 4段観客席を丸い蓮の葉競技場の外枠と一体化
- レフリーを蓮の葉の外側へ移動

FROG FIGHTER 2 JUMP prototype v0.4

v0.4 fixes:
- Title logo embedded directly in HTML so it cannot go missing.
- Portrait fighter select: face centered, name underneath; eye/face alignment stabilized.
- Four spectator tiers moved lower in the vertical stadium.
- Referee moved off the main lotus-leaf fighting surface.
- CPU vertical damping removed so rival automatic jump height matches the player.


v0.7: above-water title background, two stair aisles + short entrance stairs, ring-side promenade, smaller lotus platform with surrounding deck, referee returned to ringside, logo embedded in HTML, portrait roster layout hard-locked.


FROG FIGHTER 2 JUMP v0.8
- タイトルを水中色から地上の空・日差し・緑の会場背景へ変更
- キャラ選択のカエルの両目を顔の中央へ補正
- 4段観客席を3列化・横密度アップして満員感を強化


v1.0: title sky brightened; portrait fighter cards keep eyes inside the card and selected card expands for move list; battle title-return button moved below HP.


v1.2 SAFE FIX: restored the full v1.0 package (HTML/CSS/JS/README), then applied only targeted CSS fixes. No extra startup JavaScript was added.


v1.3: portrait fighter cards no longer scale while selected, preventing eye/head clipping; selected fighter now expands to a 286px card with a large readable move list.


v1.4: structural portrait roster fix. Fighter faces/names/move panels now use normal vertical flow rather than stacked absolute positioning. Root dark-teal fallback removed. Title is pale sky with lotus leaves at the bottom.


v1.5: title changed to pale sky with lotus leaves only at bottom. Selected fighter now spans the full roster grid row and shows a full-width move sheet below the portrait, preventing clipping by the next fighter row.
 

v1.6
- Removed the old inline mobile roster layout that forced 168px height and overflow:hidden.
- Selected fighter now expands naturally and the complete move list remains visible.
- Unselected fighter cards remain compact in a 3-column grid.
- Title background is forced to a very pale white-blue sky; lotus leaves stay only along the bottom.


v1.7
- Title now uses an actual opaque pale-sky layer inside the title screen; shared/select-screen teal cannot show through.
- Lotus leaves are real bottom scenery elements, not full-screen pseudo gradients.
- Fighter cards stay in a fixed 3-column compact grid.
- Move list is a separate full-width panel inserted directly below the selected fighter's row, so names remain visible and long move lists are never clipped.


v1.8
- Title sky changed from nearly-white to a clearly visible pale blue.
- Character cards remain fixed 3-column cards even when selected.
- Selected-card legacy scaling/expansion is neutralized.
- Move list is rendered only in the independent full-width panel.
- Move panel now uses explicit command data, including Flauros commands.


v1.9
- Increased contrast on the pale title screen: subtitle/version/start/note are darker and easier to read.
- Added ultra-high-specificity portrait roster rules to override the old split-select absolute positioning.
- Fighter cards now remain three equal columns with centered faces and names directly underneath.
- Selected fighters never resize or move; selection is border-only.
- The independent move panel remains full-width and is the only element allowed to span all three columns.


v2.0
- Title screen only: increased subtitle contrast with dark teal lettering and a subtle pale edge.
- Darkened the version badge so its white lettering is easier to read.
- Character selection layout from v1.9 was intentionally left unchanged.


v2.4
- Fixed result-screen "選択画面に戻る" touch/click handling.
- Root cause: portrait #controls was z-index 45 while result buttons were z-index 42.
- Result buttons are now z-index 80 and explicitly pointer-interactive.
- Existing game return logic is unchanged.


v2.5 - vertical-battle character tuning: Mikael
- Tongue throw changed to a downward slam with very little horizontal travel.
- Burning Uppercut launch velocity increased from -520 to -745 for roughly double jump height.
- Burning Shot speed reduced from 315 to 190.
- Burning Kick now auto-aims its launch angle at the opponent (capped at ±55 degrees).
- Burning Cyclone horizontal launch/maintenance speed greatly reduced.


v2.6 - Gabriel vertical tuning
- Aqua Tornado angle increased to about 35 degrees upward.
- Aqua Stream angle increased to about 32 degrees downward.
- Aqua Vortex unchanged.
- Aqua Shot redesigned: launches upward, disappears above the screen once, then drops vertically near the opponent.
- Reflected Aqua Shot stops its scripted drop behavior and becomes a normal reflected projectile.


v2.7 - Gabriel Aqua Shot revision
- Aqua Shot returns to a forward projectile to match Forward + Punch.
- Redesigned as a thick high-pressure water shot rather than a slow water blob.
- Speed: 430, radius: 24, damage: 4.2, short charge.
- Aqua Tornado / Stream / Vortex unchanged from v2.6.

v2.8 - Raphael wind-element vertical redesign
- Pressure Cutter renamed Air Cutter; Forward+Punch/Kick fires two wind cutters.
- Carp Pressure Cutter replaced by Air Blade with large wind-blade form and top-to-bottom / bottom-to-top curved trajectories.
- High-speed Bubble Move renamed Air Boost; Up+Guard rises first, then crosses to the opposite upper side while wrapped in wind.
- Raphael's Air Cutter / Air Blade are slightly stronger, faster and larger while airborne.
- CPU Raphael updated to use the new wind moves.

v2.9 - Raphael Air Hover
- Air Boost replaced by Air Hover.
- Up + Guard activates about 5 seconds of hovering.
- Raphael receives a short upward lift on activation.
- During hover: left/right moves horizontally, up rises, down descends; no input holds position.
- Hover movement is bounded to the playable screen.

v2.10 - startup fix
- Fixed a JavaScript syntax error introduced while replacing Raphael's Air Boost movement with Air Hover.
- The extra closing brace prevented jump-game.js from loading, so the title Start button had no handler.
- Air Hover behavior from v2.9 is retained.

v2.11 - Air Blade visibility fix
- Added dedicated rendering for Raphael's Air Blade.
- Air Blade is now a large crescent-shaped wind blade with white/cyan glow.
- Added a short wind trail so the curved up/down trajectories are easier to see.
- Uses a known visible projectile color token internally while retaining airBlade behavior.

v2.12 - Air Blade spawn fix
- Root cause found: specialAirBlade set specialT before calling specialWater2Shot, so the shared projectile function rejected the shot as "already in a special".
- Air Blade now creates its projectile directly after a 0.30s windup.
- Removed redundant second rotation in Air Blade rendering.
- Existing large crescent wind-blade visual and curved trajectories are retained.

v2.13 - Raphael vertical blade correction
- Back + Punch renamed Air Guillotine: spawns directly above the opponent and travels straight down.
- Back + Kick Air Blade: spawns directly below the opponent and travels straight up.
- Both attacks use a broad guillotine-blade wind shape instead of a crescent projectile.
- Airborne Raphael gets a modest speed/size/damage bonus.

v2.14 - Raphael hover attacks
- Air Cutter can now be fired during Air Hover.
- Air Guillotine and upward Air Blade can now be fired during Air Hover.
- Using these attacks does not cancel Air Hover or reset its remaining duration.
- Normal attack recovery still applies, so attacks cannot be infinitely stacked on the same frame.

v2.15
- Character select order: Samael and Satanael swapped, placing Satanael next to Seraphiel.
- Uriel White Counter input bug fixed: it now uses Down -> Back + Guard as shown in the move list.
- Removed the accidental Guard x2 activation for White Counter.

v2.16
- Uriel Guardian Tackle: Forward + Guard.
- Uriel White Counter: Back + Guard.

v2.17
- Remiel Frost Shot: projectile radius 15 -> 22 (about 1.47x), speed 270 -> 210 (about 78%).

v2.18
- Jihal Lightning Dash damage -20%: 9.5 -> 7.6.
- Thunder Charge damage -10% across charge levels.
- Bolt Shot redesigned as a long horizontal lightning spear with a wider horizontal hitbox.

v2.19
- Remiel mirage Frost Shot now matches the real Frost Shot size (r22) and speed (210), so the decoy is not exposed by projectile size.
- Mirage Frost Shot now has a real hitbox and deals half damage (2.4 vs 4.8).
- Mirage Frost Shot can also be reflected by guard, preserving the game's projectile counterplay.

v2.20
- Kokabiel Gravity Ball: weak horizontal pull, strong downward gravity; hit also slams downward.
- Gravity Zone: substantially stronger downward gravity, slightly smaller radius.
- Meteor Rain: reduced from five wide meteors to three larger meteors concentrated around the opponent.
- Universal wall cling: while airborne and near a side wall, holding Guard freezes the fighter on the wall for about 0.58 sec.
- Wall cling has about 0.72 sec re-use cooldown and releases immediately when Guard is released.

v2.21
- JUMP tongue ~28% longer with vertical aim assist.
- Wall cling: Back + Tongue; remains while Tongue is held, releases on button-up; 0.30s reuse delay.
- Remiel mirage copies punch/kick/tongue. Small damage; mirage tongue never grabs. Mirage vanishes after copied melee/tongue connects.

v2.22
- Gravity Zone now always appears low near the lotus arena floor.
- Gravity Ball hit applies 1.35 sec lingering strong downward gravity.
- Remiel mirage can also connect Mirage Kick for 50% damage (4.9), then disappears.
- Remiel mirage can also connect Mirage Counter for 50% damage (3.6), then disappears.

v2.23
- Sariel Blood Moon formation/survival time shortened by about 17%: moon life 3.0s -> 2.5s, special lock 3.25s -> 2.75s.
- Added four subtle gold wall-anchor balls to each extreme side of the arena as visual cues for Back + Tongue wall cling.

v2.24
- Lucifer Ice Shot enlarged from radius 17 to 24 (~1.41x), speed reduced from 255 to 225.
- Ice Shot remains faster than Remiel's Frost Shot (210), preserving character distinction.
- Hell Crash now auto-corrects its initial vertical launch angle toward the opponent, capped at about ±45 degrees; it is not continuous homing.

v2.25
- Lilith Bubble Shot command changed: Back+Punch fires forward; Down+Punch fires diagonally downward.
- Bubble Shot enlarged (r27), slowed (145), and gains upward buoyancy in the latter half of its flight.
- Removed Back+Tongue Bubble Shot so Back+Tongue remains available for the universal wall cling.
- Added Down+Kick Guillotine Kick: horizontal kick pose with a fast straight-down dive and downward knockback.

v2.26
- Lilith Guillotine Kick now keeps its attack hitbox active for the entire downward dive.
- Added swept vertical collision between the previous and current frame positions so the fast dive cannot skip through an opponent.

v2.27
- Fixed Guillotine Kick collision being accidentally placed inside the kick-button press handler.
- Guillotine Kick collision now runs every frame throughout the downward dive.
- Collision follows the visible horizontal kicking leg and sweeps from the previous to current frame position.
- Guillotine Kick remains active for a full high-altitude fall and ends on landing.

v2.28
- Beelzebub is now always visible and selectable as a normal character; no unlock flag is required.

v2.29
- Added the missing Beelzebub character card directly to the selection HTML, between Flauros and Samael. It is always visible.

v2.30
- Corrected Beelzebub character-select colors to match the in-game design:
  near-black purple body, vivid toxic-green eye bumps, white eye areas, green mouth and muted magenta cheeks.

v2.31
- Flauros Hell Flame changed to a very tall vertical fire pillar rising from near the lotus/playfield floor to the top of the screen.
- Hell Flame hit area now follows the full vertical pillar.
- Inferno Claw lower endpoint raised so Flauros no longer dives beneath the lotus leaves / too far below the visible play area.

v2.37
- Satanael Dark Pressure now leaves a 1.35-second lingering downward pull after the initial pressure.
- Inferno Wave now rises from around the lotus/playfield level to about normal jump height (~300px), with a wider flame-wall hitbox and matching visuals.
- Dark Ray and Seraphic Ray unchanged.

v2.38
- Seraphic Upper vertical launch increased about 3x (-235 -> -705).
- Seraphic Ray origin now follows Seraphiel throughout charge/fire instead of remaining at the activation point.
- Seraphic Cyclone rotation changed to continuous time-based spin so it no longer visually lingers upside-down.
- Seraphic Shot enlarged (r15 -> r25) and given a strong sinusoidal/helical flight path.

v2.39
- Satanael Dark Ray root now follows Satanael's current position/facing.
- Kawazu Spin Kick Cutter projectiles are now cross-shaped light blades.
- Added Kawazu Forward+Punch Triple Upper: three high-speed behind-the-opponent passes with rising uppercuts.
- Restored Kawazu secret: one full direction rotation + Tongue; grabs, tongue-wraps/spins the opponent, then drops them upside-down.

v2.40
- Restored the old Kawazu secret-technique tongue-wrap visual/rotation sequence based on the legacy behavior.
- Spin Kick Cutter cross-light projectiles now rotate much faster.

v2.43
- JUMP story non-frog encounters are Azazel (dragonfly) and Belial (spider), using the existing piranha/crayfish internal boss implementations from the old JUMP data.
- Their story battles now use a dedicated outdoor lotus-pond stage instead of LOTUS STADIUM.
- Outdoor stage: bright sky, clouds, pond water, reeds, natural lotus leaves/flowers, large battle lotus leaf, no grandstand and no referee.
- Story text updated from Leviathan/Asmodeus water-version names to Azazel/Belial.

v2.44
- Character select intentionally keeps Leviathan and Asmodeus.
- Story special encounters remain Azazel (dragonfly) and Belial (spider).
- Story boss start now explicitly forces the outdoor lotus-pond theme and narrative callback is single-fire to prevent skipping.
- Practice help now states: wall-side direction + Tongue button = wall cling.

v2.45
- Character select and opponent select renamed Leviathan -> Azazel, Asmodeus -> Belial.
- Character-card icons changed from fish/crayfish to flying-insect/spider imagery.
- Story restriction message updated to Azazel/Belial.
- Legacy Leviathan/Asmodeus name aliases remain internally for old save compatibility.

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

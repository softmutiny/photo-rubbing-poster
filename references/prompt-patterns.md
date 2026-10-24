# 分步提示词

以下是组织生成指令的骨架。实际调用前由助手把括号内容换成照片中的事实及本次设计决定；不向用户索取“预输入”。每次声明输入图的角色，只生成当前阶段需要的结果。先服从用户限定的阶段，再选择对应段落。

## 黑白母版

> Input 1 is the subject photograph. Input 2, if supplied, is a print-mark reference only; exclude its subjects, text and UI. Make ONLY an intermediate black-and-white stone-rubbing asset, not a poster. Extract [actual subject and its identifying structures]. Keep [silhouette, count, pose, overlap and fine features that matter]. Remove [specific incidental background elements]. Form broad solid BLACK ink masses on clean white paper, with very fine WHITE negative contour lines, restrained irregular ink loss and slightly broken transfer edges. Flatten photographic highlights, shadows and continuous gray modeling into printed shapes. Do not merely desaturate the photo or outline every edge. No typography, colored blocks, added objects, all-over noise, metallic light or embossed rendering. Keep the full chosen subject inspectable with practical margins.

检查：它是否仍像照片、亮边素描或均匀排线？如果是，先修墨块，别急着套色。

## 套色与透明素材

> Input is the established black-and-white rubbing, not a new subject suggestion. Change ONLY the ink colors and, if needed, the background alpha. Preserve the recognizable silhouette and internal structural hierarchy. Map the dominant solid ink masses to [chosen deep matte ink]. Allow [muted accent ink] only in [selected areas]. Keep negative etched gaps revealing the background; do not turn every fine line into bright gold. Keep the flat printed shape, no realistic metal highlights, glow or bevel. When transparency is requested, output real alpha around the subject and through the negative gaps, not a painted checkerboard or white fringe. No layout or text in this asset stage.

透明输出另设工具的透明背景参数。代码检查 alpha，避免把预览底色当作输出内容。需要用白底看形时保留白底母版，不反复重做透明层。

## 无字底稿

> Input 1 is the established colored rubbing layer to composite. Input 2, if supplied, is a layout/print reference only. Make the intermediate artwork BEFORE text. Preserve [subject invariants]. Arrange the motif according to its actual directional shape: [specific crop, position and relation to the color field]. Use [small selected palette] in broad calm flat paper planes. Keep dark solid ink as the main visual mass and [accent] secondary. Let a small portion overlap color planes only if it helps this composition. Quiet paper fiber; no relief, stains or uniform loud distress. [Any subtle background trace] comes from the source and stays lower in contrast than the motif. Reserve [title area] without filling it with decoration. Absolutely no letters, calligraphy, numbers, brand, seals, new subject matter or screenshot UI.

不要每次使用相同百分比。对于窄竖挂饰，先处理它与色面边线平行、重合的问题；对于枝条，保留自然展开而不是机械居中缩小。

## 加字

> Input is the established NO-TEXT ground. Add typography only; preserve the existing subject and color composition. Exact title: “[confirmed title]”. Exact caption: “[confirmed caption, or omit it]”. Place [specific arrangement and hierarchy based on this ground]. Use [chosen type character and matte ink color] consistent with the printed image. Require correct characters and reading order. Do not invent dates, venue, brand, extra slogans, red seals or pseudo calligraphy. Do not alter the motif while adding words. Deliver one finished artwork.

看结果核对字形和阅读顺序。文字失真时，只修文字或返回无字底稿，不通过重绘全主体来修字。

## 修复“全金线、墨块丢失”

这是本案例最有价值的修正，应在确有此问题时使用。

> Input 1 is the current poster, the edit target. Input 2 is its black-and-white mother asset, authoritative for solid ink mass and subject shape. Correct ONLY the subject ink treatment. Restore broad calm [dark matte ink] masses for [the specific solid bodies]. Reduce busy interior scratches and uniform bright outlines; keep just essential thin negative contour marks and a few natural missed-ink patches, exposing the underlying paper color. Let muted [accent] survive only at [selected edge, local detail or a color-plane crossing]. This is flat printed ink, not shiny metallic drawing. Keep the exact background, typography and layout visually stable. Do not invent new objects. Verify the result rather than assuming these invariants held.

## 单项构图修订

> Use the nearest correct poster as the edit target. Address [one diagnosed spatial issue]. Move/crop/scale [specific existing motif] by [case-specific amount], preserving its recognizable structure and pose. Adjust the color-field boundary only if necessary to resolve its relation to the motif. Preserve the established ink hierarchy and correct title/caption. If the prior edit thickened paper texture, flatten that unintended change. Do not add decorations to fill empty space or revert to rendering the original photograph from scratch.

修订后用相同尺寸预览比较。判断主体与空间的关系是否改变，而非仅确认颜色、颗粒或纸纹又换了一种。

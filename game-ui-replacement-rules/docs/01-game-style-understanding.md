# 01 Game Style Understanding

> Generated from the uploaded `游戏名_app_url_20260513.xlsx` and the provided game-style-understanding prompt. Last updated: 2026-05-13.

## Prompt Review and Batch Adaptation

- 原 prompt 的方向是正确的：先做文字资料研究，再提炼视觉身份，最后转译成工具 UI / 面板 / 背景建议。
- 批量处理 50 款游戏时，不建议为每款完整展开 7 大章节，否则文档会膨胀且难以维护。本文件采用“每款游戏一条知识库条目”的压缩结构：Text Research Summary + Game Style Understanding + Auto Brief + UI Translation + Tool Background Prompt + GitHub Metadata。
- `app_url` 保留为 source_checked；对于不确定或较新的游戏，详情页可作为二次复核来源。本文只提取可迁移的风格原则，不复刻 logo、角色、IP 专属图形或具体商业素材。
- 背景 prompt 均遵守：服务 UI、45%–60% 安全区、低信息密度、低对比、低饱和、边缘装饰、中心克制、无清晰文字、无假 UI。

## Global Quality Gate

- **是否只是机械套用了代表色**：否；每条包含世界语义、材质、形状、状态和误判风险。
- **是否误判具名游戏风格**：已尽量基于游戏长期稳定定位；低/中置信条目已在 source_confidence 体现。
- **brief 是否来自 Game Style Understanding**：是；Brief 字段由 identity、mood、material、palette、semantics 回推。
- **背景是否服务 UI，而不是完整插画**：是；每条背景 prompt 都强制中央 50% 左右安全区。
- **普通态、选中态、警示态是否混淆**：已明确 selected 与 warning/error 的颜色语义分离。
- **装饰语义是否符合游戏世界**：是；角标和装饰均来自 game world semantics。
- **文字是否清晰**：要求正文使用高对比字体，小字不依赖描边或发光。
- **小卡片是否过度复杂**：已要求小卡简化，大卡可承载风格纹理。
- **Maker 成本是否过高**：目标 4–5；优先圆角、边框、阴影、静态贴图、九宫格和简单 tween。
- **是否有硬编码游戏名映射**：没有写死生成逻辑；条目可作为风格原型继续抽象。

## Entries

## 01. 心动小镇

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/45213
- **game_type**: 生活模拟 / 社交 / 建造装饰
- **core_gameplay**: 开放小镇生活、家园布置、钓鱼采集、社交与轻压力日常循环
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 温暖治愈的手作小镇生活模拟
- **genre_presentation**: 把生活模拟视觉化为柔软、低压力、可亲近的社区日常，而不是写实城镇或硬核经营。
- **primary_mood**: 温暖、轻松、松弛、陪伴感
- **world_semantics**: 小镇街角、木屋、手作家具、花草、便签、邮票、路牌、咖啡、海边微风
- **common_ui_material_language**: 浅色纸卡、浅木纹、布料贴纸、半透明磨砂卡片
- **shape_language**: 大圆角、软阴影、手绘不规则边、贴纸角标、轻量卡片层叠
- **palette_tendency**: 奶油白作面板底；浅木色/暖棕作边框；草绿/天蓝作辅助；珊瑚橙/暖黄作选中和奖励，不用高饱和红做普通选中
- **accent_semantics**: 树叶、邮票、手写标签、木牌、花瓣、小房子、猫爪
- **background_language**: 浅暖天空或小镇远景，中心留出干净低纹理区域，边缘放树影、屋檐、路牌和花草
- **misclassification_risks**: 被误判成真实田园、儿童绘本或高饱和农场经营

### 3. Auto Game Style Brief
- **style_keywords**: 温暖治愈的手作小镇生活模拟
- **mood**: 温暖、轻松、松弛、陪伴感
- **world_semantics**: 小镇街角、木屋、手作家具、花草、便签、邮票、路牌、咖啡、海边微风
- **material_language**: 浅色纸卡、浅木纹、布料贴纸、半透明磨砂卡片
- **shape_language**: 大圆角、软阴影、手绘不规则边、贴纸角标、轻量卡片层叠
- **palette_intent**: 奶油白作面板底；浅木色/暖棕作边框；草绿/天蓝作辅助；珊瑚橙/暖黄作选中和奖励，不用高饱和红做普通选中
- **state_language**: selected 用暖黄描边+小贴纸；disabled 降低饱和和透明度；locked 用小锁牌；warning 才用柔和橙红
- **accent_semantics**: 树叶、邮票、手写标签、木牌、花瓣、小房子、猫爪
- **background_language**: 浅暖天空或小镇远景，中心留出干净低纹理区域，边缘放树影、屋檐、路牌和花草
- **forbidden_directions**: 被误判成真实田园、儿童绘本或高饱和农场经营
- **maker_safe_assets**: Maker 目标 5：圆角矩形、boxShadow、少量贴纸 PNG、九宫格木纹边框即可实现

### 4. UI Translation Recommendations
- **panel_design**: 面板用奶油白半透明卡片配浅木边，普通卡简化贴纸纹理，大卡可加手绘角花和轻微纸张颗粒
- **state_design**: selected 用暖黄描边+小贴纸；disabled 降低饱和和透明度；locked 用小锁牌；warning 才用柔和橙红
- **text_design**: 标题可用圆润手写感，正文使用清晰黑棕色；小字禁止强描边
- **accent_design**: 树叶、邮票、手写标签、木牌、花瓣、小房子、猫爪。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 浅暖天空或小镇远景，中心留出干净低纹理区域，边缘放树影、屋檐、路牌和花草。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 5：圆角矩形、boxShadow、少量贴纸 PNG、九宫格木纹边框即可实现

### 5. Tool Background Prompt
> 生成温暖手作小镇生活感工具背景，奶油白与浅木色基调，中央 50% 干净低纹理 UI 安全区，边缘有模糊小屋、绿植、木牌和花草贴纸，柔和日光，低对比低饱和，无清晰文字、无按钮、无角色主视觉。

### 6. Quality Gate
- **check_result**: pass with risk note — 被误判成真实田园、儿童绘本或高饱和农场经营
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 心动小镇
aliases: []
category: 生活模拟 / 社交 / 建造装饰
visual_identity: 温暖治愈的手作小镇生活模拟
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [cozy, life-sim, town]
misclassification_risks: 被误判成真实田园、儿童绘本或高饱和农场经营
maker_feasibility_target: "4-5"
tags: [cozy, life-sim, town, handmade]
```

## 02. 乱涂彩世界

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/748842
- **game_type**: 休闲射击 / 二次元 / 涂鸦染色
- **core_gameplay**: 以染色、弹幕射击、神明娘伙伴与无厘头漫画剧情驱动的轻爽闯关
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 潮酷涂鸦系二次元爆涂休闲射击
- **genre_presentation**: 把射击视觉化为颜料喷溅、颜色反应、漫画梗和黑白世界被染色的反差。
- **primary_mood**: 高能、搞怪、解压、彩色爆发
- **world_semantics**: 颜料枪、喷漆罐、涂鸦、黑白世界、神明娘、漫画分格、外星入侵、爆色进度条
- **common_ui_material_language**: 高饱和油漆、贴纸胶带、漫画纸、塑料喷罐、亮面颜料层
- **shape_language**: 不规则喷溅边、漫画爆炸框、粗描边、倾斜标签、圆角卡片
- **palette_tendency**: 黑白灰作底层世界；青/粉/黄/紫作染色强调；白色面板保证可读；红色仅作危险或火系反应
- **accent_semantics**: 喷漆滴落、胶带、手绘箭头、漫画感叹号、颜料块、神格小徽章
- **background_language**: 灰白城市或漫画纸底，边缘被彩色颜料侵蚀，中央保持浅色干净区域
- **misclassification_risks**: 误判成普通赛博霓虹或儿童绘画；不要把所有区域都喷满颜料

### 3. Auto Game Style Brief
- **style_keywords**: 潮酷涂鸦系二次元爆涂休闲射击
- **mood**: 高能、搞怪、解压、彩色爆发
- **world_semantics**: 颜料枪、喷漆罐、涂鸦、黑白世界、神明娘、漫画分格、外星入侵、爆色进度条
- **material_language**: 高饱和油漆、贴纸胶带、漫画纸、塑料喷罐、亮面颜料层
- **shape_language**: 不规则喷溅边、漫画爆炸框、粗描边、倾斜标签、圆角卡片
- **palette_intent**: 黑白灰作底层世界；青/粉/黄/紫作染色强调；白色面板保证可读；红色仅作危险或火系反应
- **state_language**: selected 用彩色描边+喷溅角标；warning 用红黑警示，不可与普通彩色装饰混淆
- **accent_semantics**: 喷漆滴落、胶带、手绘箭头、漫画感叹号、颜料块、神格小徽章
- **background_language**: 灰白城市或漫画纸底，边缘被彩色颜料侵蚀，中央保持浅色干净区域
- **forbidden_directions**: 误判成普通赛博霓虹或儿童绘画；不要把所有区域都喷满颜料
- **maker_safe_assets**: Maker 目标 4：喷溅贴图、粗描边矩形、简单缩放弹跳，避免复杂流体动效

### 4. UI Translation Recommendations
- **panel_design**: 白底漫画卡+粗黑边+少量颜料飞溅，主按钮可用彩色胶囊但字区必须纯净
- **state_design**: selected 用彩色描边+喷溅角标；warning 用红黑警示，不可与普通彩色装饰混淆
- **text_design**: 标题可用漫画粗体，正文用黑色无衬线；副文字放在纯色底上
- **accent_design**: 喷漆滴落、胶带、手绘箭头、漫画感叹号、颜料块、神格小徽章。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 灰白城市或漫画纸底，边缘被彩色颜料侵蚀，中央保持浅色干净区域。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 4：喷溅贴图、粗描边矩形、简单缩放弹跳，避免复杂流体动效

### 5. Tool Background Prompt
> 生成潮酷涂鸦染色工具背景，黑白灰漫画城市/纸面作为弱背景，四周有青粉黄紫颜料喷溅和胶带贴纸，中央 50% 留白低纹理，低信息密度，无角色、无假 UI、无清晰文字。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成普通赛博霓虹或儿童绘画；不要把所有区域都喷满颜料
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 乱涂彩世界
aliases: []
category: 休闲射击 / 二次元 / 涂鸦染色
visual_identity: 潮酷涂鸦系二次元爆涂休闲射击
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [graffiti, paint, anime]
misclassification_risks: 误判成普通赛博霓虹或儿童绘画；不要把所有区域都喷满颜料
maker_feasibility_target: "4-5"
tags: [graffiti, paint, anime, casual-shooter]
```

## 03. 潜水员戴夫

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/720041
- **game_type**: 冒险 / 经营 / 像素
- **core_gameplay**: 白天潜水探索、捕鱼收集，夜晚寿司店经营的混合玩法
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 复古像素海底冒险 + 寿司店经营
- **genre_presentation**: 把冒险和经营视觉化为蓝绿色海底深度、像素物件和夜间小店烟火气的双场景切换。
- **primary_mood**: 幽默、探索、轻松、海底神秘
- **world_semantics**: 潜水装备、海藻、鱼群、氧气瓶、寿司柜台、木质菜单、像素道具
- **common_ui_material_language**: 像素化玻璃面板、深海蓝透明板、木牌菜单、餐厅纸卡
- **shape_language**: 像素边、矩形块、轻量描边、小图标网格
- **palette_tendency**: 深海蓝/青绿作背景；米白作菜单面板；木棕作经营区；橙黄作新鲜度和奖励；红色只作氧气/危险
- **accent_semantics**: 气泡、鱼影、寿司、氧气表、像素箭头、木牌价格签
- **background_language**: 海底渐层或寿司店模糊远景，中央安全区不要有密集鱼群和强水纹
- **misclassification_risks**: 误判成纯海洋治愈或纯餐厅经营，忽略像素幽默与双场景

### 3. Auto Game Style Brief
- **style_keywords**: 复古像素海底冒险 + 寿司店经营
- **mood**: 幽默、探索、轻松、海底神秘
- **world_semantics**: 潜水装备、海藻、鱼群、氧气瓶、寿司柜台、木质菜单、像素道具
- **material_language**: 像素化玻璃面板、深海蓝透明板、木牌菜单、餐厅纸卡
- **shape_language**: 像素边、矩形块、轻量描边、小图标网格
- **palette_intent**: 深海蓝/青绿作背景；米白作菜单面板；木棕作经营区；橙黄作新鲜度和奖励；红色只作氧气/危险
- **state_language**: selected 用气泡高光或橙黄菜单贴；locked 用小锁/深海阴影；warning 用氧气红
- **accent_semantics**: 气泡、鱼影、寿司、氧气表、像素箭头、木牌价格签
- **background_language**: 海底渐层或寿司店模糊远景，中央安全区不要有密集鱼群和强水纹
- **forbidden_directions**: 误判成纯海洋治愈或纯餐厅经营，忽略像素幽默与双场景
- **maker_safe_assets**: Maker 目标 5：像素边框、海底渐变、少量鱼/气泡 icon，低成本

### 4. UI Translation Recommendations
- **panel_design**: 深蓝半透明卡或木质菜单卡，像素描边控制在 1-2 层
- **state_design**: selected 用气泡高光或橙黄菜单贴；locked 用小锁/深海阴影；warning 用氧气红
- **text_design**: 标题可用复古像素字，正文保持常规清晰字体
- **accent_design**: 气泡、鱼影、寿司、氧气表、像素箭头、木牌价格签。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 海底渐层或寿司店模糊远景，中央安全区不要有密集鱼群和强水纹。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 5：像素边框、海底渐变、少量鱼/气泡 icon，低成本

### 5. Tool Background Prompt
> 生成复古像素海底工具背景，深海蓝绿色柔和渐变，边缘有模糊鱼影、气泡、海草与少量寿司店木牌元素，中央 50% 干净低纹理，低对比，无清晰文字、无按钮、无角色主视觉。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成纯海洋治愈或纯餐厅经营，忽略像素幽默与双场景
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 潜水员戴夫
aliases: []
category: 冒险 / 经营 / 像素
visual_identity: 复古像素海底冒险 + 寿司店经营
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [pixel, underwater, restaurant]
misclassification_risks: 误判成纯海洋治愈或纯餐厅经营，忽略像素幽默与双场景
maker_feasibility_target: "4-5"
tags: [pixel, underwater, restaurant, adventure]
```

## 04. 鹅鸭杀

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/258720
- **game_type**: 社交推理 / 派对
- **core_gameplay**: 多人身份推理、任务、会议投票与阵营欺骗
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 卡通鸟类社交推理派对
- **genre_presentation**: 把狼人杀式推理视觉化为圆润鸟类角色、轻松搞笑与任务地图中的悬疑反差。
- **primary_mood**: 搞笑、紧张、友尽、轻悬疑
- **world_semantics**: 鹅、鸭、会议桌、投票牌、任务清单、脚印、警报、可疑标记
- **common_ui_material_language**: 扁平塑料卡、白板纸、任务便签、圆形徽章
- **shape_language**: 圆润、厚描边、气泡式对话框、投票卡片
- **palette_tendency**: 浅灰/米白作面板；蓝绿作安全/任务；黄色作讨论和提醒；红色仅用于警报、淘汰或危险
- **accent_semantics**: 羽毛、脚印、问号、投票贴纸、警报灯、身份徽章
- **background_language**: 简单地图舱室或农场/空间站远景，边缘放脚印和任务纸，中央干净
- **misclassification_risks**: 误判成儿童低龄卡通；需要保留“可疑/投票/推理”语义

### 3. Auto Game Style Brief
- **style_keywords**: 卡通鸟类社交推理派对
- **mood**: 搞笑、紧张、友尽、轻悬疑
- **world_semantics**: 鹅、鸭、会议桌、投票牌、任务清单、脚印、警报、可疑标记
- **material_language**: 扁平塑料卡、白板纸、任务便签、圆形徽章
- **shape_language**: 圆润、厚描边、气泡式对话框、投票卡片
- **palette_intent**: 浅灰/米白作面板；蓝绿作安全/任务；黄色作讨论和提醒；红色仅用于警报、淘汰或危险
- **state_language**: selected 用黄色投票框；warning 用红色警报灯；disabled 灰化但保留轮廓
- **accent_semantics**: 羽毛、脚印、问号、投票贴纸、警报灯、身份徽章
- **background_language**: 简单地图舱室或农场/空间站远景，边缘放脚印和任务纸，中央干净
- **forbidden_directions**: 误判成儿童低龄卡通；需要保留“可疑/投票/推理”语义
- **maker_safe_assets**: Maker 目标 5：圆角卡、贴纸、脚印 icon、简单弹跳动效

### 4. UI Translation Recommendations
- **panel_design**: 圆角厚卡+投票便签风，大卡可加头像圆章，小卡只保留身份/状态
- **state_design**: selected 用黄色投票框；warning 用红色警报灯；disabled 灰化但保留轮廓
- **text_design**: 标题可圆润粗体，正文黑灰；状态词用高对比标签
- **accent_design**: 羽毛、脚印、问号、投票贴纸、警报灯、身份徽章。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 简单地图舱室或农场/空间站远景，边缘放脚印和任务纸，中央干净。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 5：圆角卡、贴纸、脚印 icon、简单弹跳动效

### 5. Tool Background Prompt
> 生成卡通社交推理工具背景，浅灰蓝地图房间或派对桌远景，边缘有羽毛、脚印、投票贴纸和警报小灯，中央 50% 留白低纹理，低饱和低对比，无清晰文字、无假按钮。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成儿童低龄卡通；需要保留“可疑/投票/推理”语义
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 鹅鸭杀
aliases: []
category: 社交推理 / 派对
visual_identity: 卡通鸟类社交推理派对
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [party, deduction, cartoon]
misclassification_risks: 误判成儿童低龄卡通；需要保留“可疑/投票/推理”语义
maker_feasibility_target: "4-5"
tags: [party, deduction, cartoon, social]
```

## 05. 以闪亮之名

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/218210
- **game_type**: 女性向 / 换装 / 生活
- **core_gameplay**: 高自由度捏脸、服装搭配、家园与社交内容
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 现代高定时装生活美学
- **genre_presentation**: 把换装视觉化为时尚杂志、轻奢摄影棚、珠光玻璃和精致妆造系统。
- **primary_mood**: 精致、闪耀、优雅、自由表达
- **world_semantics**: 高定礼服、化妆镜、衣架、珠宝、镜面、摄影灯、香水瓶
- **common_ui_material_language**: 珠光玻璃、半透明亚克力、丝绸纸、金属细边、柔光卡片
- **shape_language**: 纤细圆角、轻薄层叠、细线框、留白丰富
- **palette_tendency**: 珍珠白作底；浅粉/香槟金作高级感；银灰作信息层；玫瑰金/星光蓝作选中；黑色用于时尚对比
- **accent_semantics**: 钻石、缎带、衣架、镜框、星光、香水瓶、杂志页角
- **background_language**: 柔焦摄影棚或衣帽间边缘元素，中央保持纯净高亮但不过曝
- **misclassification_risks**: 误判成普通粉色少女或婚礼风，忽略现代时装杂志感

### 3. Auto Game Style Brief
- **style_keywords**: 现代高定时装生活美学
- **mood**: 精致、闪耀、优雅、自由表达
- **world_semantics**: 高定礼服、化妆镜、衣架、珠宝、镜面、摄影灯、香水瓶
- **material_language**: 珠光玻璃、半透明亚克力、丝绸纸、金属细边、柔光卡片
- **shape_language**: 纤细圆角、轻薄层叠、细线框、留白丰富
- **palette_intent**: 珍珠白作底；浅粉/香槟金作高级感；银灰作信息层；玫瑰金/星光蓝作选中；黑色用于时尚对比
- **state_language**: selected 用玫瑰金细描边+星点；warning 用珊瑚红小标签，不污染整体
- **accent_semantics**: 钻石、缎带、衣架、镜框、星光、香水瓶、杂志页角
- **background_language**: 柔焦摄影棚或衣帽间边缘元素，中央保持纯净高亮但不过曝
- **forbidden_directions**: 误判成普通粉色少女或婚礼风，忽略现代时装杂志感
- **maker_safe_assets**: Maker 目标 4：渐变卡、细边框、静态星光、轻量玻璃遮罩

### 4. UI Translation Recommendations
- **panel_design**: 大卡用磨砂玻璃+细金属边，小卡去掉复杂花纹只保留光泽
- **state_design**: selected 用玫瑰金细描边+星点；warning 用珊瑚红小标签，不污染整体
- **text_design**: 标题可高对比优雅字重，正文现代无衬线，字间距略松
- **accent_design**: 钻石、缎带、衣架、镜框、星光、香水瓶、杂志页角。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 柔焦摄影棚或衣帽间边缘元素，中央保持纯净高亮但不过曝。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 4：渐变卡、细边框、静态星光、轻量玻璃遮罩

### 5. Tool Background Prompt
> 生成现代高定时装工具背景，珍珠白和香槟粉基调，柔焦衣帽间/摄影棚边缘，少量丝带、镜面和星光点缀，中央 50% 清爽留白，低对比，无清晰文字、无假 UI、无人物大图。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成普通粉色少女或婚礼风，忽略现代时装杂志感
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 以闪亮之名
aliases: []
category: 女性向 / 换装 / 生活
visual_identity: 现代高定时装生活美学
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [fashion, dress-up, luxury]
misclassification_risks: 误判成普通粉色少女或婚礼风，忽略现代时装杂志感
maker_feasibility_target: "4-5"
tags: [fashion, dress-up, luxury, modern]
```

## 06. 植物大战僵尸2

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/54031
- **game_type**: 塔防 / 休闲 / 卡通
- **core_gameplay**: 植物单位放置、僵尸波次、跨时空主题关卡
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 诙谐卡通植物塔防
- **genre_presentation**: 把塔防视觉化为后院棋盘、夸张植物表情、僵尸喜剧和清晰的格子攻防。
- **primary_mood**: 幽默、轻松、策略、闹腾
- **world_semantics**: 草坪格子、向日葵、坚果、豌豆、墓碑、路障、时空旅行
- **common_ui_material_language**: 草地板、木牌、泥土卡、漫画纸、石碑按钮
- **shape_language**: 圆润夸张、厚描边、棋盘网格、木牌标签
- **palette_tendency**: 草绿作环境；泥土棕作边框；阳光黄作资源/选中；灰紫作僵尸和危险；红色仅作警告
- **accent_semantics**: 阳光、叶子、种子包、墓碑、路障桶、泥土裂纹
- **background_language**: 浅草坪或时空主题远景，边缘植物/墓碑，中心安全区不放密集格子
- **misclassification_risks**: 误判成普通农场或儿童园艺，必须保留塔防棋盘和僵尸喜剧

### 3. Auto Game Style Brief
- **style_keywords**: 诙谐卡通植物塔防
- **mood**: 幽默、轻松、策略、闹腾
- **world_semantics**: 草坪格子、向日葵、坚果、豌豆、墓碑、路障、时空旅行
- **material_language**: 草地板、木牌、泥土卡、漫画纸、石碑按钮
- **shape_language**: 圆润夸张、厚描边、棋盘网格、木牌标签
- **palette_intent**: 草绿作环境；泥土棕作边框；阳光黄作资源/选中；灰紫作僵尸和危险；红色仅作警告
- **state_language**: selected 用阳光黄光圈；locked 用灰墓碑；warning 用僵尸紫/红警示
- **accent_semantics**: 阳光、叶子、种子包、墓碑、路障桶、泥土裂纹
- **background_language**: 浅草坪或时空主题远景，边缘植物/墓碑，中心安全区不放密集格子
- **forbidden_directions**: 误判成普通农场或儿童园艺，必须保留塔防棋盘和僵尸喜剧
- **maker_safe_assets**: Maker 目标 5：木牌九宫格、叶子图标、阳光贴图

### 4. UI Translation Recommendations
- **panel_design**: 木牌/泥土面板，按钮像种子包但文字区平整
- **state_design**: selected 用阳光黄光圈；locked 用灰墓碑；warning 用僵尸紫/红警示
- **text_design**: 标题可漫画粗体，正文深棕/黑色
- **accent_design**: 阳光、叶子、种子包、墓碑、路障桶、泥土裂纹。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 浅草坪或时空主题远景，边缘植物/墓碑，中心安全区不放密集格子。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 5：木牌九宫格、叶子图标、阳光贴图

### 5. Tool Background Prompt
> 生成诙谐卡通植物塔防工具背景，浅绿色草坪和柔和泥土地面，边缘有模糊植物叶片、木牌、少量墓碑轮廓，中央 50% 干净低纹理，低饱和，无清晰文字、无假 UI。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成普通农场或儿童园艺，必须保留塔防棋盘和僵尸喜剧
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 植物大战僵尸2
aliases: []
category: 塔防 / 休闲 / 卡通
visual_identity: 诙谐卡通植物塔防
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [cartoon, tower-defense, plants]
misclassification_risks: 误判成普通农场或儿童园艺，必须保留塔防棋盘和僵尸喜剧
maker_feasibility_target: "4-5"
tags: [cartoon, tower-defense, plants, zombies]
```

## 07. 崩坏：星穹铁道

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/224267
- **game_type**: 回合制 RPG / 太空幻想
- **core_gameplay**: 列车穿越星海、多星球冒险、角色回合制战斗
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 星际列车式华丽太空幻想 RPG
- **genre_presentation**: 把回合制 RPG 视觉化为星轨旅行、车票、档案、行星文明和精致科幻魔法混合界面。
- **primary_mood**: 史诗、浪漫、神秘、精致
- **world_semantics**: 星穹列车、车票、星轨、行星、命途符号、档案馆、空间站
- **common_ui_material_language**: 深色玻璃 HUD、金属细边、星图纸、车票卡、能量纹理
- **shape_language**: 圆角与锐角结合、细线框、轨道弧线、星图节点
- **palette_tendency**: 深蓝/黑作宇宙底；银白作信息层；金色作高级/命途；青蓝/紫作能量；红色只作危险
- **accent_semantics**: 车票、星轨、星星节点、命途徽记、列车窗、档案夹
- **background_language**: 深色星空或列车舷窗远景，中心避免高亮星云和密集粒子
- **misclassification_risks**: 误判成通用蓝紫科幻手游；要保留列车旅行与档案质感

### 3. Auto Game Style Brief
- **style_keywords**: 星际列车式华丽太空幻想 RPG
- **mood**: 史诗、浪漫、神秘、精致
- **world_semantics**: 星穹列车、车票、星轨、行星、命途符号、档案馆、空间站
- **material_language**: 深色玻璃 HUD、金属细边、星图纸、车票卡、能量纹理
- **shape_language**: 圆角与锐角结合、细线框、轨道弧线、星图节点
- **palette_intent**: 深蓝/黑作宇宙底；银白作信息层；金色作高级/命途；青蓝/紫作能量；红色只作危险
- **state_language**: selected 用金色轨道光；warning 用红橙小警示；disabled 降亮度并保留线框
- **accent_semantics**: 车票、星轨、星星节点、命途徽记、列车窗、档案夹
- **background_language**: 深色星空或列车舷窗远景，中心避免高亮星云和密集粒子
- **forbidden_directions**: 误判成通用蓝紫科幻手游；要保留列车旅行与档案质感
- **maker_safe_assets**: Maker 目标 4：玻璃卡、线框、星点贴图，避免复杂宇宙粒子

### 4. UI Translation Recommendations
- **panel_design**: 深色磨砂玻璃卡+细金边/银边，大卡可加星图线，小卡简洁
- **state_design**: selected 用金色轨道光；warning 用红橙小警示；disabled 降亮度并保留线框
- **text_design**: 标题可细致高对比，正文用浅灰白，避免小字发光
- **accent_design**: 车票、星轨、星星节点、命途徽记、列车窗、档案夹。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 深色星空或列车舷窗远景，中心避免高亮星云和密集粒子。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 4：玻璃卡、线框、星点贴图，避免复杂宇宙粒子

### 5. Tool Background Prompt
> 生成星际列车太空幻想工具背景，深蓝黑柔和星空与远处列车舷窗/星轨轮廓，中央 50% 干净暗色低纹理 UI 安全区，边缘少量金色星图线和车票元素，低对比，无文字无假 UI。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成通用蓝紫科幻手游；要保留列车旅行与档案质感
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 崩坏：星穹铁道
aliases: []
category: 回合制 RPG / 太空幻想
visual_identity: 星际列车式华丽太空幻想 RPG
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [space-fantasy, turn-based-rpg, train]
misclassification_risks: 误判成通用蓝紫科幻手游；要保留列车旅行与档案质感
maker_feasibility_target: "4-5"
tags: [space-fantasy, turn-based-rpg, train, anime]
```

## 08. 我的休闲时光

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/242251
- **game_type**: 装修模拟 / 休闲 / 生活
- **core_gameplay**: DIY 小窝、服装造型、猫、种花、网购、料理钓鱼等佛系生活
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 柔和手绘宅家装修生活模拟
- **genre_presentation**: 把休闲模拟视觉化为温馨小屋、软萌家居、猫咪陪伴和轻手绘生活质感。
- **primary_mood**: 佛系、温馨、可爱、慢节奏
- **world_semantics**: 小窝、猫、花盆、家具、咖啡、网购纸箱、钓鱼、料理
- **common_ui_material_language**: 米白纸卡、布艺贴片、浅木、软塑料按钮
- **shape_language**: 大圆角、软卡片、轻手绘描边、贴纸式小图标
- **palette_tendency**: 奶油白/浅粉作底；浅木棕作结构；薄荷绿/天蓝作辅助；暖橙作奖励；灰色用于已完成/不可用
- **accent_semantics**: 猫爪、花朵、纸箱、咖啡杯、沙发、窗帘、小鱼
- **background_language**: 温馨房间或窗边远景，边缘放家具和绿植，中心简洁
- **misclassification_risks**: 误判成高饱和儿童装修或真实家装软件

### 3. Auto Game Style Brief
- **style_keywords**: 柔和手绘宅家装修生活模拟
- **mood**: 佛系、温馨、可爱、慢节奏
- **world_semantics**: 小窝、猫、花盆、家具、咖啡、网购纸箱、钓鱼、料理
- **material_language**: 米白纸卡、布艺贴片、浅木、软塑料按钮
- **shape_language**: 大圆角、软卡片、轻手绘描边、贴纸式小图标
- **palette_intent**: 奶油白/浅粉作底；浅木棕作结构；薄荷绿/天蓝作辅助；暖橙作奖励；灰色用于已完成/不可用
- **state_language**: selected 用暖橙描边+猫爪；locked 用小门牌；warning 用柔和红棕
- **accent_semantics**: 猫爪、花朵、纸箱、咖啡杯、沙发、窗帘、小鱼
- **background_language**: 温馨房间或窗边远景，边缘放家具和绿植，中心简洁
- **forbidden_directions**: 误判成高饱和儿童装修或真实家装软件
- **maker_safe_assets**: Maker 目标 5：圆角矩形、贴纸、淡纹理、简单缩放

### 4. UI Translation Recommendations
- **panel_design**: 布艺/纸质圆角卡，卡片之间保持宽松呼吸感
- **state_design**: selected 用暖橙描边+猫爪；locked 用小门牌；warning 用柔和红棕
- **text_design**: 标题圆润可爱，正文深灰，副文浅棕
- **accent_design**: 猫爪、花朵、纸箱、咖啡杯、沙发、窗帘、小鱼。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 温馨房间或窗边远景，边缘放家具和绿植，中心简洁。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 5：圆角矩形、贴纸、淡纹理、简单缩放

### 5. Tool Background Prompt
> 生成柔和手绘宅家生活工具背景，奶油白浅粉基调，边缘有模糊家具、猫爪、绿植、咖啡杯和纸箱贴纸，中央 50% 干净低纹理，柔和室内光，无清晰文字、无假 UI。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成高饱和儿童装修或真实家装软件
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 我的休闲时光
aliases: []
category: 装修模拟 / 休闲 / 生活
visual_identity: 柔和手绘宅家装修生活模拟
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [cozy, home, decor]
misclassification_risks: 误判成高饱和儿童装修或真实家装软件
maker_feasibility_target: "4-5"
tags: [cozy, home, decor, casual]
```

## 09. 三角洲行动

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/330259
- **game_type**: 战术射击 / 搜打撤 / 军事
- **core_gameplay**: 现代战术小队、枪械、撤离、兵种协作和高信息密度战斗
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 现代战术军事 HUD
- **genre_presentation**: 把射击视觉化为专业军规终端、装备仓、战术地图、枪械参数和紧张但克制的信息系统。
- **primary_mood**: 专业、紧张、硬核、冷静
- **world_semantics**: 战术地图、军用装备、弹匣、编号、坐标、护甲、警戒条、补给箱
- **common_ui_material_language**: 磨砂军用终端、碳纤维、旧金属、橡胶、半透明 HUD
- **shape_language**: 硬边、切角、网格线、短横条、编号标签、窄边框
- **palette_tendency**: 深橄榄/枪灰作底；浅灰绿作信息；琥珀黄作选中/任务；红色只用于受伤/危险；蓝色用于友军/系统
- **accent_semantics**: 螺丝、军用编号、坐标线、弹孔、警戒三角、装备插槽
- **background_language**: 暗绿灰战术地图或仓库墙面，中央低纹理，边缘放装备箱与地图线
- **misclassification_risks**: 误判成赛博霓虹或泛科幻蓝 UI；不要过多发光

### 3. Auto Game Style Brief
- **style_keywords**: 现代战术军事 HUD
- **mood**: 专业、紧张、硬核、冷静
- **world_semantics**: 战术地图、军用装备、弹匣、编号、坐标、护甲、警戒条、补给箱
- **material_language**: 磨砂军用终端、碳纤维、旧金属、橡胶、半透明 HUD
- **shape_language**: 硬边、切角、网格线、短横条、编号标签、窄边框
- **palette_intent**: 深橄榄/枪灰作底；浅灰绿作信息；琥珀黄作选中/任务；红色只用于受伤/危险；蓝色用于友军/系统
- **state_language**: selected 用琥珀黄边框+扫描线；locked 用金属锁/封条；warning 用红色高优先级
- **accent_semantics**: 螺丝、军用编号、坐标线、弹孔、警戒三角、装备插槽
- **background_language**: 暗绿灰战术地图或仓库墙面，中央低纹理，边缘放装备箱与地图线
- **forbidden_directions**: 误判成赛博霓虹或泛科幻蓝 UI；不要过多发光
- **maker_safe_assets**: Maker 目标 4：切角 SVG/九宫格、线框、静态噪声，避免真实 3D 金属

### 4. UI Translation Recommendations
- **panel_design**: 深色硬边面板+切角边框+网格底纹，小卡减少材质保留编号
- **state_design**: selected 用琥珀黄边框+扫描线；locked 用金属锁/封条；warning 用红色高优先级
- **text_design**: 标题窄体硬朗，正文浅灰；小字不要依赖发光
- **accent_design**: 螺丝、军用编号、坐标线、弹孔、警戒三角、装备插槽。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 暗绿灰战术地图或仓库墙面，中央低纹理，边缘放装备箱与地图线。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 4：切角 SVG/九宫格、线框、静态噪声，避免真实 3D 金属

### 5. Tool Background Prompt
> 生成现代战术军事工具背景，深橄榄与枪灰基调，中央 50% 干净低纹理 HUD 安全区，边缘有战术地图线、装备箱轮廓、编号贴纸和微弱扫描线，低饱和低对比，无清晰文字、无假按钮。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成赛博霓虹或泛科幻蓝 UI；不要过多发光
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 三角洲行动
aliases: []
category: 战术射击 / 搜打撤 / 军事
visual_identity: 现代战术军事 HUD
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [tactical, military, shooter]
misclassification_risks: 误判成赛博霓虹或泛科幻蓝 UI；不要过多发光
maker_feasibility_target: "4-5"
tags: [tactical, military, shooter, hud]
```

## 10. 明日方舟：终末地

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/232326
- **game_type**: 科幻 RPG / 策略建造 / 开放探索
- **core_gameplay**: 行星开拓、工业设施、角色协作与资源链条构建
- **confidence**: medium

### 2. Game Style Understanding
- **recognized_visual_identity**: 荒星工业科幻开拓 RPG
- **genre_presentation**: 把探索和建造视觉化为荒星基地、工业终端、轨道物流、矿物能源和低调冷硬的企业设施感。
- **primary_mood**: 克制、专业、荒凉、探索
- **world_semantics**: 荒星地表、基地终端、轨道运输、矿石、能源管线、干员装备、工业标识
- **common_ui_material_language**: 工业终端玻璃、金属板、磨砂黑面、警示胶带、矿石能量条
- **shape_language**: 硬边切角、模块化网格、编号块、细线 HUD
- **palette_tendency**: 灰黑/岩土色作底；白灰作文字；青蓝作系统能源；橙黄作警示/交互；红色只作事故
- **accent_semantics**: 管线、矿石、工业编号、警示条、物流箭头、基地图标
- **background_language**: 荒星地貌或基地墙体远景，中央保持低对比网格
- **misclassification_risks**: 误判成传统明日方舟医疗黑白 UI 或通用未来蓝

### 3. Auto Game Style Brief
- **style_keywords**: 荒星工业科幻开拓 RPG
- **mood**: 克制、专业、荒凉、探索
- **world_semantics**: 荒星地表、基地终端、轨道运输、矿石、能源管线、干员装备、工业标识
- **material_language**: 工业终端玻璃、金属板、磨砂黑面、警示胶带、矿石能量条
- **shape_language**: 硬边切角、模块化网格、编号块、细线 HUD
- **palette_intent**: 灰黑/岩土色作底；白灰作文字；青蓝作系统能源；橙黄作警示/交互；红色只作事故
- **state_language**: selected 用青蓝光条或橙黄任务边；warning 与 selected 颜色区分
- **accent_semantics**: 管线、矿石、工业编号、警示条、物流箭头、基地图标
- **background_language**: 荒星地貌或基地墙体远景，中央保持低对比网格
- **forbidden_directions**: 误判成传统明日方舟医疗黑白 UI 或通用未来蓝
- **maker_safe_assets**: Maker 目标 4：线框、切角、轻贴图，避免复杂 3D 基地

### 4. UI Translation Recommendations
- **panel_design**: 模块化硬边卡+工业细线，大卡可加入管线/能源槽，小卡简化
- **state_design**: selected 用青蓝光条或橙黄任务边；warning 与 selected 颜色区分
- **text_design**: 标题冷静工业字，正文高可读无衬线
- **accent_design**: 管线、矿石、工业编号、警示条、物流箭头、基地图标。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 荒星地貌或基地墙体远景，中央保持低对比网格。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 4：线框、切角、轻贴图，避免复杂 3D 基地

### 5. Tool Background Prompt
> 生成荒星工业科幻工具背景，灰黑岩土与低饱和青蓝基调，边缘有基地管线、矿石、物流箭头和工业编号块，中央 50% 干净低纹理 UI 安全区，无清晰文字、无假 UI、无强光源。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成传统明日方舟医疗黑白 UI 或通用未来蓝
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 明日方舟：终末地
aliases: []
category: 科幻 RPG / 策略建造 / 开放探索
visual_identity: 荒星工业科幻开拓 RPG
source_confidence: medium
last_updated: 2026-05-13
recommended_archetypes: [sci-fi, industrial, arknights]
misclassification_risks: 误判成传统明日方舟医疗黑白 UI 或通用未来蓝
maker_feasibility_target: "4-5"
tags: [sci-fi, industrial, arknights, exploration]
```

## 11. 我的世界：移动版

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/43639
- **game_type**: 沙盒 / 生存 / 建造
- **core_gameplay**: 方块采集、合成、建造、生存探索
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 体素方块沙盒生存建造
- **genre_presentation**: 把沙盒视觉化为像素方块、合成格、物品栏和可拼装的世界材料。
- **primary_mood**: 自由、创造、探索、轻冒险
- **world_semantics**: 草方块、木板、矿石、工作台、背包格、火把、红石、洞穴
- **common_ui_material_language**: 像素方块、木板、石砖、物品栏槽、半透明黑底
- **shape_language**: 直角、像素边、8-bit 网格、块面拼接
- **palette_tendency**: 草绿/泥棕作自然底；石灰作结构；木棕作面板；青钻/红石作稀有和状态；红色只作受伤
- **accent_semantics**: 方块、镐子、矿石、火把、合成格、像素箭头
- **background_language**: 低细节体素地形远景，中央干净块状渐变
- **misclassification_risks**: 误判成普通像素复古，必须保留体素方块和合成语义

### 3. Auto Game Style Brief
- **style_keywords**: 体素方块沙盒生存建造
- **mood**: 自由、创造、探索、轻冒险
- **world_semantics**: 草方块、木板、矿石、工作台、背包格、火把、红石、洞穴
- **material_language**: 像素方块、木板、石砖、物品栏槽、半透明黑底
- **shape_language**: 直角、像素边、8-bit 网格、块面拼接
- **palette_intent**: 草绿/泥棕作自然底；石灰作结构；木棕作面板；青钻/红石作稀有和状态；红色只作受伤
- **state_language**: selected 用白色像素描边或钻石青；locked 用基岩灰
- **accent_semantics**: 方块、镐子、矿石、火把、合成格、像素箭头
- **background_language**: 低细节体素地形远景，中央干净块状渐变
- **forbidden_directions**: 误判成普通像素复古，必须保留体素方块和合成语义
- **maker_safe_assets**: Maker 目标 5：方块贴图、格子背景、像素边框

### 4. UI Translation Recommendations
- **panel_design**: 木板/石砖九宫格面板，按钮直角或小圆角像物品槽
- **state_design**: selected 用白色像素描边或钻石青；locked 用基岩灰
- **text_design**: 标题可像素体，正文保持清晰无衬线/像素大字
- **accent_design**: 方块、镐子、矿石、火把、合成格、像素箭头。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 低细节体素地形远景，中央干净块状渐变。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 5：方块贴图、格子背景、像素边框

### 5. Tool Background Prompt
> 生成体素方块沙盒工具背景，柔和草方块与木板石砖边缘装饰，中央 50% 干净低纹理块状安全区，少量矿石和合成格图案，低对比，无清晰文字、无假 UI。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成普通像素复古，必须保留体素方块和合成语义
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 我的世界：移动版
aliases: []
category: 沙盒 / 生存 / 建造
visual_identity: 体素方块沙盒生存建造
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [voxel, sandbox, crafting]
misclassification_risks: 误判成普通像素复古，必须保留体素方块和合成语义
maker_feasibility_target: "4-5"
tags: [voxel, sandbox, crafting, survival]
```

## 12. 王者荣耀

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/2301
- **game_type**: MOBA / 竞技 / 英雄
- **core_gameplay**: 5v5 英雄对战、技能成长、皮肤和赛事化竞技
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 华丽东方幻想竞技 MOBA
- **genre_presentation**: 把 MOBA 视觉化为英雄殿堂、战场徽章、金色段位、技能符文和高 polish 竞技面板。
- **primary_mood**: 热血、荣耀、华丽、竞技
- **world_semantics**: 英雄徽章、王者冠冕、战场地图、技能符文、段位牌、峡谷能量
- **common_ui_material_language**: 深蓝玻璃、金属金边、玉石/水晶、旗帜布纹
- **shape_language**: 对称构图、金边浮雕、圆角+尖角混合、徽章化
- **palette_tendency**: 深蓝/靛紫作底；金色作荣耀与选中；白色作文字；红蓝区分敌我；绿色仅作生命/安全
- **accent_semantics**: 冠冕、段位星、符文、旗帜、剑盾、战场路线
- **background_language**: 深蓝峡谷/宫殿远景，中央避免复杂英雄和强光
- **misclassification_risks**: 误判成泛蓝紫魔幻手游，需保留竞技和荣耀段位语义

### 3. Auto Game Style Brief
- **style_keywords**: 华丽东方幻想竞技 MOBA
- **mood**: 热血、荣耀、华丽、竞技
- **world_semantics**: 英雄徽章、王者冠冕、战场地图、技能符文、段位牌、峡谷能量
- **material_language**: 深蓝玻璃、金属金边、玉石/水晶、旗帜布纹
- **shape_language**: 对称构图、金边浮雕、圆角+尖角混合、徽章化
- **palette_intent**: 深蓝/靛紫作底；金色作荣耀与选中；白色作文字；红蓝区分敌我；绿色仅作生命/安全
- **state_language**: selected 用金色光圈/段位星；warning 用红色敌情，不作普通装饰
- **accent_semantics**: 冠冕、段位星、符文、旗帜、剑盾、战场路线
- **background_language**: 深蓝峡谷/宫殿远景，中央避免复杂英雄和强光
- **forbidden_directions**: 误判成泛蓝紫魔幻手游，需保留竞技和荣耀段位语义
- **maker_safe_assets**: Maker 目标 4：九宫格金边、徽章 icon、静态光效

### 4. UI Translation Recommendations
- **panel_design**: 大卡可用金边浮雕，小卡使用简化金线+深蓝底
- **state_design**: selected 用金色光圈/段位星；warning 用红色敌情，不作普通装饰
- **text_design**: 标题可高对比华丽，正文白色或浅金但需足够对比
- **accent_design**: 冠冕、段位星、符文、旗帜、剑盾、战场路线。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 深蓝峡谷/宫殿远景，中央避免复杂英雄和强光。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 4：九宫格金边、徽章 icon、静态光效

### 5. Tool Background Prompt
> 生成华丽东方幻想竞技工具背景，深蓝靛紫基调，边缘有金色符文、旗帜、峡谷建筑轮廓和段位星徽，中央 50% 干净低纹理，低对比，无英雄大图、无清晰文字、无假 UI。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成泛蓝紫魔幻手游，需保留竞技和荣耀段位语义
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 王者荣耀
aliases: []
category: MOBA / 竞技 / 英雄
visual_identity: 华丽东方幻想竞技 MOBA
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [moba, heroic, fantasy]
misclassification_risks: 误判成泛蓝紫魔幻手游，需保留竞技和荣耀段位语义
maker_feasibility_target: "4-5"
tags: [moba, heroic, fantasy, competitive]
```

## 13. 鸣潮

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/234280
- **game_type**: 开放世界 ARPG / 二次元
- **core_gameplay**: 末世后探索、共鸣能力、动作战斗与声骸收集
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 后启示录声波科幻二次元开放世界
- **genre_presentation**: 把动作开放世界视觉化为冷白黑灰、声波共振、断裂城市和高机动战斗界面。
- **primary_mood**: 孤寂、清冷、锋利、探索
- **world_semantics**: 共鸣、声波、残响、废墟、黑石、白色装甲、频谱线
- **common_ui_material_language**: 冷白玻璃、黑灰金属、频谱 HUD、半透明能量层
- **shape_language**: 锐利切角、细线、波形曲线、留白与断裂边
- **palette_tendency**: 黑/白/灰作大基调；青蓝作共鸣和系统；少量红橙作危险；避免大面积紫粉
- **accent_semantics**: 波形、频谱、碎片、黑石纹、坐标点、声骸符号
- **background_language**: 低饱和废墟/天空远景，中央浅灰或深灰安全区
- **misclassification_risks**: 误判成通用赛博二次元或末世废土脏乱风

### 3. Auto Game Style Brief
- **style_keywords**: 后启示录声波科幻二次元开放世界
- **mood**: 孤寂、清冷、锋利、探索
- **world_semantics**: 共鸣、声波、残响、废墟、黑石、白色装甲、频谱线
- **material_language**: 冷白玻璃、黑灰金属、频谱 HUD、半透明能量层
- **shape_language**: 锐利切角、细线、波形曲线、留白与断裂边
- **palette_intent**: 黑/白/灰作大基调；青蓝作共鸣和系统；少量红橙作危险；避免大面积紫粉
- **state_language**: selected 用青蓝频谱边；warning 用红橙故障条；disabled 去饱和
- **accent_semantics**: 波形、频谱、碎片、黑石纹、坐标点、声骸符号
- **background_language**: 低饱和废墟/天空远景，中央浅灰或深灰安全区
- **forbidden_directions**: 误判成通用赛博二次元或末世废土脏乱风
- **maker_safe_assets**: Maker 目标 4：线框、波形 SVG、透明遮罩，避免复杂粒子

### 4. UI Translation Recommendations
- **panel_design**: 冷白/黑灰半透明卡+青蓝细线，小卡极简
- **state_design**: selected 用青蓝频谱边；warning 用红橙故障条；disabled 去饱和
- **text_design**: 标题冷峻纤细，正文高对比黑白，避免大面积发光
- **accent_design**: 波形、频谱、碎片、黑石纹、坐标点、声骸符号。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 低饱和废墟/天空远景，中央浅灰或深灰安全区。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 4：线框、波形 SVG、透明遮罩，避免复杂粒子

### 5. Tool Background Prompt
> 生成后启示录声波科幻工具背景，黑白灰低饱和城市废墟远景，边缘有青蓝频谱线、碎片和坐标点，中央 50% 干净低纹理安全区，冷清光感，无清晰文字、无假 UI、无角色。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成通用赛博二次元或末世废土脏乱风
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 鸣潮
aliases: []
category: 开放世界 ARPG / 二次元
visual_identity: 后启示录声波科幻二次元开放世界
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [post-apocalyptic, resonance, anime]
misclassification_risks: 误判成通用赛博二次元或末世废土脏乱风
maker_feasibility_target: "4-5"
tags: [post-apocalyptic, resonance, anime, open-world]
```

## 14. Phigros

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/165287
- **game_type**: 音乐节奏 / 抽象
- **core_gameplay**: 动态判定线、谱面节奏和音乐章节体验
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 极简抽象几何音乐节奏
- **genre_presentation**: 把节奏游戏视觉化为线条、几何、速度、空白和音乐动势，而不是具象世界观。
- **primary_mood**: 纯净、专注、律动、实验
- **world_semantics**: 判定线、音符、几何块、波形、章节封面、节拍轨迹
- **common_ui_material_language**: 纯色面板、半透明玻璃、细线网格、轻粒子
- **shape_language**: 极简矩形、锐利线段、非对称动态构图
- **palette_tendency**: 黑/白/深灰作底；高纯度单色作章节强调；青紫粉黄可按曲风变化；警示色极少用
- **accent_semantics**: 音符点、判定线、波形、几何碎片、节拍光点
- **background_language**: 大面积纯色/渐变，边缘少量线条和音符，中心绝对干净
- **misclassification_risks**: 误判成通用霓虹 EDM；需要保留克制极简和动态线条

### 3. Auto Game Style Brief
- **style_keywords**: 极简抽象几何音乐节奏
- **mood**: 纯净、专注、律动、实验
- **world_semantics**: 判定线、音符、几何块、波形、章节封面、节拍轨迹
- **material_language**: 纯色面板、半透明玻璃、细线网格、轻粒子
- **shape_language**: 极简矩形、锐利线段、非对称动态构图
- **palette_intent**: 黑/白/深灰作底；高纯度单色作章节强调；青紫粉黄可按曲风变化；警示色极少用
- **state_language**: selected 用细亮线/节拍脉冲；warning 用小红点，不大面积
- **accent_semantics**: 音符点、判定线、波形、几何碎片、节拍光点
- **background_language**: 大面积纯色/渐变，边缘少量线条和音符，中心绝对干净
- **forbidden_directions**: 误判成通用霓虹 EDM；需要保留克制极简和动态线条
- **maker_safe_assets**: Maker 目标 5：纯色块、线段 SVG、简单位移/缩放 tween

### 4. UI Translation Recommendations
- **panel_design**: 面板极简，低边框或无边框，靠线条和间距建立层级
- **state_design**: selected 用细亮线/节拍脉冲；warning 用小红点，不大面积
- **text_design**: 标题可现代几何，正文极简高对比
- **accent_design**: 音符点、判定线、波形、几何碎片、节拍光点。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 大面积纯色/渐变，边缘少量线条和音符，中心绝对干净。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 5：纯色块、线段 SVG、简单位移/缩放 tween

### 5. Tool Background Prompt
> 生成极简抽象音乐节奏工具背景，黑白灰或深色渐变，边缘有少量几何线段、音符点和波形，中央 55% 纯净低纹理安全区，低信息密度，无清晰文字、无假 UI。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成通用霓虹 EDM；需要保留克制极简和动态线条
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: Phigros
aliases: []
category: 音乐节奏 / 抽象
visual_identity: 极简抽象几何音乐节奏
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [rhythm, minimal, geometry]
misclassification_risks: 误判成通用霓虹 EDM；需要保留克制极简和动态线条
maker_feasibility_target: "4-5"
tags: [rhythm, minimal, geometry, music]
```

## 15. 杖剑传说

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/717836
- **game_type**: 放置 RPG / 异世界冒险
- **core_gameplay**: 轻松放置成长、异世界探索、伙伴、圣兽与转职技能搭配
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 轻爽异世界放置冒险
- **genre_presentation**: 把异世界 RPG 视觉化为浮空岛、小木屋、地图迷雾、幻兽伙伴和不压迫的成长感。
- **primary_mood**: 轻松、明亮、冒险、陪伴
- **world_semantics**: 浮空岛、软床、小木屋、地图迷雾、圣兽、宝箱、剑与法杖
- **common_ui_material_language**: 羊皮纸、浅木、软布、宝石小徽章、地图纸
- **shape_language**: 圆润厚卡、卷轴边、木牌、地图折角
- **palette_tendency**: 暖白/浅黄作面板；木棕作结构；天空蓝/草绿作探索；金色作宝物；红色仅作战斗警示
- **accent_semantics**: 宝箱、云朵、法杖、短剑、地图针、羊、圣兽脚印
- **background_language**: 天空浮岛和小木屋远景，中央保持云雾留白
- **misclassification_risks**: 误判成硬核西幻暗黑或泛 RPG 蓝紫

### 3. Auto Game Style Brief
- **style_keywords**: 轻爽异世界放置冒险
- **mood**: 轻松、明亮、冒险、陪伴
- **world_semantics**: 浮空岛、软床、小木屋、地图迷雾、圣兽、宝箱、剑与法杖
- **material_language**: 羊皮纸、浅木、软布、宝石小徽章、地图纸
- **shape_language**: 圆润厚卡、卷轴边、木牌、地图折角
- **palette_intent**: 暖白/浅黄作面板；木棕作结构；天空蓝/草绿作探索；金色作宝物；红色仅作战斗警示
- **state_language**: selected 用金色宝箱光或蓝色探索边；locked 用迷雾遮罩
- **accent_semantics**: 宝箱、云朵、法杖、短剑、地图针、羊、圣兽脚印
- **background_language**: 天空浮岛和小木屋远景，中央保持云雾留白
- **forbidden_directions**: 误判成硬核西幻暗黑或泛 RPG 蓝紫
- **maker_safe_assets**: Maker 目标 5：木牌、纸卡、云朵贴图、简单弹跳

### 4. UI Translation Recommendations
- **panel_design**: 纸质/木质圆角面板，大卡可加地图纹，小卡保留宝箱角标
- **state_design**: selected 用金色宝箱光或蓝色探索边；locked 用迷雾遮罩
- **text_design**: 标题冒险手写感，正文深棕清晰
- **accent_design**: 宝箱、云朵、法杖、短剑、地图针、羊、圣兽脚印。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 天空浮岛和小木屋远景，中央保持云雾留白。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 5：木牌、纸卡、云朵贴图、简单弹跳

### 5. Tool Background Prompt
> 生成轻爽异世界放置冒险工具背景，浅天空蓝和暖白云雾，边缘有浮空岛、小木屋、宝箱、地图折角和法杖短剑小图标，中央 50% 干净低纹理，低对比，无角色、无清晰文字。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成硬核西幻暗黑或泛 RPG 蓝紫
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 杖剑传说
aliases: []
category: 放置 RPG / 异世界冒险
visual_identity: 轻爽异世界放置冒险
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [idle-rpg, isekai, light-fantasy]
misclassification_risks: 误判成硬核西幻暗黑或泛 RPG 蓝紫
maker_feasibility_target: "4-5"
tags: [idle-rpg, isekai, light-fantasy, adventure]
```

## 16. 原神

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/168332
- **game_type**: 开放世界 RPG / 二次元幻想
- **core_gameplay**: 七国探索、元素反应、角色养成与冒险解谜
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 明亮诗意的元素幻想开放世界
- **genre_presentation**: 把幻想 RPG 视觉化为自然地貌、元素符号、冒险者图鉴、古典纹样和轻透明界面。
- **primary_mood**: 明亮、诗意、冒险、神秘
- **world_semantics**: 元素符号、风之翼、地图、七国建筑、蒲公英、晶蝶、冒险手册
- **common_ui_material_language**: 浅色羊皮纸、半透明玻璃、石纹、金属细边、元素晶石
- **shape_language**: 圆角、细金边、卷草纹、轻浮雕、图鉴卡
- **palette_tendency**: 米白/浅灰作面板；金色作高级和选中；青绿/天蓝作探索；元素色作状态；红色只作危险/火元素
- **accent_semantics**: 元素徽记、晶蝶、羽毛、地图针、卷草纹、星星
- **background_language**: 柔和天空/自然远景，边缘放建筑和元素纹样，中心干净
- **misclassification_risks**: 误判成通用二次元魔幻或高饱和手游

### 3. Auto Game Style Brief
- **style_keywords**: 明亮诗意的元素幻想开放世界
- **mood**: 明亮、诗意、冒险、神秘
- **world_semantics**: 元素符号、风之翼、地图、七国建筑、蒲公英、晶蝶、冒险手册
- **material_language**: 浅色羊皮纸、半透明玻璃、石纹、金属细边、元素晶石
- **shape_language**: 圆角、细金边、卷草纹、轻浮雕、图鉴卡
- **palette_intent**: 米白/浅灰作面板；金色作高级和选中；青绿/天蓝作探索；元素色作状态；红色只作危险/火元素
- **state_language**: selected 用金色细边+元素光；warning 用红色火焰图标，不作通用选中
- **accent_semantics**: 元素徽记、晶蝶、羽毛、地图针、卷草纹、星星
- **background_language**: 柔和天空/自然远景，边缘放建筑和元素纹样，中心干净
- **forbidden_directions**: 误判成通用二次元魔幻或高饱和手游
- **maker_safe_assets**: Maker 目标 4：九宫格细边、元素 SVG、静态光点

### 4. UI Translation Recommendations
- **panel_design**: 浅纸卡+细金边+元素小徽章，小卡避免复杂花纹
- **state_design**: selected 用金色细边+元素光；warning 用红色火焰图标，不作通用选中
- **text_design**: 标题可古典细腻，正文深灰或白色高对比
- **accent_design**: 元素徽记、晶蝶、羽毛、地图针、卷草纹、星星。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 柔和天空/自然远景，边缘放建筑和元素纹样，中心干净。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 4：九宫格细边、元素 SVG、静态光点

### 5. Tool Background Prompt
> 生成明亮元素幻想工具背景，浅天空与自然远景，边缘有柔和建筑轮廓、元素符号、晶蝶和卷草纹，中央 50% 干净低纹理 UI 安全区，低饱和低对比，无角色、无假 UI、无清晰文字。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成通用二次元魔幻或高饱和手游
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 原神
aliases: []
category: 开放世界 RPG / 二次元幻想
visual_identity: 明亮诗意的元素幻想开放世界
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [elemental-fantasy, open-world, anime]
misclassification_risks: 误判成通用二次元魔幻或高饱和手游
maker_feasibility_target: "4-5"
tags: [elemental-fantasy, open-world, anime, adventure]
```

## 17. 洛克王国：世界

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/188212
- **game_type**: 精灵收集 / 开放世界 / 社交
- **core_gameplay**: 精灵收集对战、开放世界探索、魔法学院与自由社交
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 明亮童年魔法精灵大世界
- **genre_presentation**: 把精灵收集视觉化为魔法学院、精灵伙伴、孵蛋、奇景和轻快社交。
- **primary_mood**: 明亮、童趣、怀旧、轻快
- **world_semantics**: 精灵球/捕捉器、魔法书、学院、新生、孵蛋、奇景、菜园、伙伴羁绊
- **common_ui_material_language**: 魔法书纸、圆润玻璃、糖果色徽章、浅木/石板
- **shape_language**: 圆润厚卡、学院徽章、书页折角、星星魔法线
- **palette_tendency**: 天空蓝/奶油白作底；草绿作探索；金色作奖励；紫蓝作魔法；红色仅作危险
- **accent_semantics**: 魔法星、精灵脚印、书签、蛋壳、学院徽章、蝴蝶结
- **background_language**: 魔法学院或草地远景，中心清爽，边缘放精灵脚印和书页
- **misclassification_risks**: 误判成冷蓝仙侠或低龄宠物乐园；要保留学院与精灵收集

### 3. Auto Game Style Brief
- **style_keywords**: 明亮童年魔法精灵大世界
- **mood**: 明亮、童趣、怀旧、轻快
- **world_semantics**: 精灵球/捕捉器、魔法书、学院、新生、孵蛋、奇景、菜园、伙伴羁绊
- **material_language**: 魔法书纸、圆润玻璃、糖果色徽章、浅木/石板
- **shape_language**: 圆润厚卡、学院徽章、书页折角、星星魔法线
- **palette_intent**: 天空蓝/奶油白作底；草绿作探索；金色作奖励；紫蓝作魔法；红色仅作危险
- **state_language**: selected 用金色星星描边；locked 用书锁；warning 用红色感叹号
- **accent_semantics**: 魔法星、精灵脚印、书签、蛋壳、学院徽章、蝴蝶结
- **background_language**: 魔法学院或草地远景，中心清爽，边缘放精灵脚印和书页
- **forbidden_directions**: 误判成冷蓝仙侠或低龄宠物乐园；要保留学院与精灵收集
- **maker_safe_assets**: Maker 目标 5：书页、星星、徽章、圆角卡

### 4. UI Translation Recommendations
- **panel_design**: 书页卡+圆润玻璃按钮，大卡可加学院徽章，小卡只放精灵脚印
- **state_design**: selected 用金色星星描边；locked 用书锁；warning 用红色感叹号
- **text_design**: 标题圆润魔法感，正文深蓝灰清晰
- **accent_design**: 魔法星、精灵脚印、书签、蛋壳、学院徽章、蝴蝶结。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 魔法学院或草地远景，中心清爽，边缘放精灵脚印和书页。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 5：书页、星星、徽章、圆角卡

### 5. Tool Background Prompt
> 生成明亮童年魔法精灵工具背景，天空蓝和奶油白基调，边缘有魔法学院远景、草地、精灵脚印、书页和星星魔法线，中央 50% 干净低纹理，无角色大图、无清晰文字、无假 UI。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成冷蓝仙侠或低龄宠物乐园；要保留学院与精灵收集
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 洛克王国：世界
aliases: []
category: 精灵收集 / 开放世界 / 社交
visual_identity: 明亮童年魔法精灵大世界
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [pet-collection, magic, open-world]
misclassification_risks: 误判成冷蓝仙侠或低龄宠物乐园；要保留学院与精灵收集
maker_feasibility_target: "4-5"
tags: [pet-collection, magic, open-world, nostalgia]
```

## 18. 蛋仔派对

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/206776
- **game_type**: 派对 / 休闲竞技 / UGC
- **core_gameplay**: 多人闯关、圆滚角色、派对地图与 UGC 创作
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 糖果玩具体圆滚派对竞技
- **genre_presentation**: 把派对竞技视觉化为软塑料玩具、糖果色关卡、圆形角色和强社交表情。
- **primary_mood**: 欢乐、闹腾、可爱、竞技
- **world_semantics**: 蛋仔、弹簧、障碍、糖果、盲盒、游乐场、表情贴纸
- **common_ui_material_language**: 亮面软塑料、糖果胶、贴纸、泡泡玻璃
- **shape_language**: 超圆润、厚块面、充气感、胶囊按钮
- **palette_tendency**: 高明度蓝粉黄作主视觉；白色作面板；紫/橙作活动；红色只作失败/危险
- **accent_semantics**: 糖豆、星星、贴纸、弹簧、盲盒、彩带、表情
- **background_language**: 游乐场或玩具盒边缘，中央大面积浅色安全区
- **misclassification_risks**: 误判成普通儿童乐园；要保留竞技闯关和盲盒玩具质感

### 3. Auto Game Style Brief
- **style_keywords**: 糖果玩具体圆滚派对竞技
- **mood**: 欢乐、闹腾、可爱、竞技
- **world_semantics**: 蛋仔、弹簧、障碍、糖果、盲盒、游乐场、表情贴纸
- **material_language**: 亮面软塑料、糖果胶、贴纸、泡泡玻璃
- **shape_language**: 超圆润、厚块面、充气感、胶囊按钮
- **palette_intent**: 高明度蓝粉黄作主视觉；白色作面板；紫/橙作活动；红色只作失败/危险
- **state_language**: selected 用彩虹描边或弹跳光；locked 用盲盒锁；warning 红色障碍标记
- **accent_semantics**: 糖豆、星星、贴纸、弹簧、盲盒、彩带、表情
- **background_language**: 游乐场或玩具盒边缘，中央大面积浅色安全区
- **forbidden_directions**: 误判成普通儿童乐园；要保留竞技闯关和盲盒玩具质感
- **maker_safe_assets**: Maker 目标 5：圆角、渐变、贴纸、简单弹跳 tween

### 4. UI Translation Recommendations
- **panel_design**: 圆鼓鼓面板+软塑料高光，小卡用胶囊形态
- **state_design**: selected 用彩虹描边或弹跳光；locked 用盲盒锁；warning 红色障碍标记
- **text_design**: 标题可胖圆体，正文深色高对比
- **accent_design**: 糖豆、星星、贴纸、弹簧、盲盒、彩带、表情。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 游乐场或玩具盒边缘，中央大面积浅色安全区。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 5：圆角、渐变、贴纸、简单弹跳 tween

### 5. Tool Background Prompt
> 生成糖果玩具派对工具背景，浅蓝粉黄柔和基调，边缘有充气障碍、彩带、糖豆、星星和盲盒贴纸，中央 50% 干净低纹理，低信息密度，无清晰文字、无假按钮。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成普通儿童乐园；要保留竞技闯关和盲盒玩具质感
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 蛋仔派对
aliases: []
category: 派对 / 休闲竞技 / UGC
visual_identity: 糖果玩具体圆滚派对竞技
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [party, toy, cute]
misclassification_risks: 误判成普通儿童乐园；要保留竞技闯关和盲盒玩具质感
maker_feasibility_target: "4-5"
tags: [party, toy, cute, ugc]
```

## 19. 鬼谷八荒

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/700558
- **game_type**: 修仙 / 沙盒 / 角色扮演
- **core_gameplay**: 开放修仙、宗门、机缘、功法、境界成长与随机事件
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 东方水墨修仙沙盒
- **genre_presentation**: 把修仙沙盒视觉化为山海卷轴、法阵、丹炉、宗门令牌和命运事件。
- **primary_mood**: 玄妙、苍茫、修行、古朴
- **world_semantics**: 山海、云雾、八卦、丹炉、符箓、宗门、功法卷轴、灵石
- **common_ui_material_language**: 宣纸、墨迹、古铜、玉石、卷轴、石碑
- **shape_language**: 水墨边、卷轴角、篆刻印章、圆形法阵
- **palette_tendency**: 米黄宣纸作面板；墨黑作文字；青绿/玉色作灵力；朱砂作印章和重点；暗红只作危机
- **accent_semantics**: 符箓、八卦、印章、灵石、丹药、山形纹
- **background_language**: 水墨山峦和云雾远景，中央淡宣纸留白
- **misclassification_risks**: 误判成冷蓝仙侠或宫廷古风；要保留沙盒修行和道法语义

### 3. Auto Game Style Brief
- **style_keywords**: 东方水墨修仙沙盒
- **mood**: 玄妙、苍茫、修行、古朴
- **world_semantics**: 山海、云雾、八卦、丹炉、符箓、宗门、功法卷轴、灵石
- **material_language**: 宣纸、墨迹、古铜、玉石、卷轴、石碑
- **shape_language**: 水墨边、卷轴角、篆刻印章、圆形法阵
- **palette_intent**: 米黄宣纸作面板；墨黑作文字；青绿/玉色作灵力；朱砂作印章和重点；暗红只作危机
- **state_language**: selected 用朱砂印/玉色光；warning 用暗红劫雷符，不作普通选中
- **accent_semantics**: 符箓、八卦、印章、灵石、丹药、山形纹
- **background_language**: 水墨山峦和云雾远景，中央淡宣纸留白
- **forbidden_directions**: 误判成冷蓝仙侠或宫廷古风；要保留沙盒修行和道法语义
- **maker_safe_assets**: Maker 目标 4：纸纹、墨线、印章贴图，避免复杂水墨动画

### 4. UI Translation Recommendations
- **panel_design**: 宣纸面板+墨线边+朱砂小印，小卡极简
- **state_design**: selected 用朱砂印/玉色光；warning 用暗红劫雷符，不作普通选中
- **text_design**: 标题可书法化，正文必须宋/黑体清晰
- **accent_design**: 符箓、八卦、印章、灵石、丹药、山形纹。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 水墨山峦和云雾远景，中央淡宣纸留白。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 4：纸纹、墨线、印章贴图，避免复杂水墨动画

### 5. Tool Background Prompt
> 生成东方水墨修仙工具背景，米黄宣纸和淡墨山海云雾，边缘有八卦、符箓、灵石和卷轴角，中央 50% 淡色留白低纹理，低对比，无清晰文字、无假 UI、无角色。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成冷蓝仙侠或宫廷古风；要保留沙盒修行和道法语义
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 鬼谷八荒
aliases: []
category: 修仙 / 沙盒 / 角色扮演
visual_identity: 东方水墨修仙沙盒
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [xianxia, ink, cultivation]
misclassification_risks: 误判成冷蓝仙侠或宫廷古风；要保留沙盒修行和道法语义
maker_feasibility_target: "4-5"
tags: [xianxia, ink, cultivation, sandbox]
```

## 20. 异环

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/714119
- **game_type**: 超自然都市 / 开放世界 RPG
- **core_gameplay**: 玩家作为异象猎人，在海特洛市接取委托、解决都市异象并体验生活经营
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 超自然都市怪谈开放世界 RPG
- **genre_presentation**: 把开放世界视觉化为现代都市、古董店委托、异象怪谈、轻喜剧角色与稍陌生的日常城市。
- **primary_mood**: 都市、怪奇、轻喜剧、时髦
- **world_semantics**: 海特洛市、异象猎人、古董店、电视头海獭、涂鸦滑板、委托档案、店铺经营
- **common_ui_material_language**: 都市玻璃、霓虹招牌、档案纸、古董金属、街头贴纸
- **shape_language**: 现代圆角卡、街区标牌、档案夹、轻切角、贴纸叠层
- **palette_tendency**: 夜色蓝灰/城市灰作底；霓虹粉青作异象；暖黄作店铺生活；红色仅作异常危险
- **accent_semantics**: 委托单、古董标签、涂鸦、电视头图标、交通牌、异常封条
- **background_language**: 低对比城市街角/古董店远景，异象元素放边缘，中心干净
- **misclassification_risks**: 误判成赛博朋克或纯二次元都市；需保留超自然怪谈和生活经营

### 3. Auto Game Style Brief
- **style_keywords**: 超自然都市怪谈开放世界 RPG
- **mood**: 都市、怪奇、轻喜剧、时髦
- **world_semantics**: 海特洛市、异象猎人、古董店、电视头海獭、涂鸦滑板、委托档案、店铺经营
- **material_language**: 都市玻璃、霓虹招牌、档案纸、古董金属、街头贴纸
- **shape_language**: 现代圆角卡、街区标牌、档案夹、轻切角、贴纸叠层
- **palette_intent**: 夜色蓝灰/城市灰作底；霓虹粉青作异象；暖黄作店铺生活；红色仅作异常危险
- **state_language**: selected 用霓虹青粉边；warning 用异常红封条；locked 用档案锁
- **accent_semantics**: 委托单、古董标签、涂鸦、电视头图标、交通牌、异常封条
- **background_language**: 低对比城市街角/古董店远景，异象元素放边缘，中心干净
- **forbidden_directions**: 误判成赛博朋克或纯二次元都市；需保留超自然怪谈和生活经营
- **maker_safe_assets**: Maker 目标 4：城市渐变、贴纸、封条、简单光晕

### 4. UI Translation Recommendations
- **panel_design**: 半透明城市卡+档案夹标签，局部霓虹但不过亮
- **state_design**: selected 用霓虹青粉边；warning 用异常红封条；locked 用档案锁
- **text_design**: 标题现代都市感，正文深浅对比清楚
- **accent_design**: 委托单、古董标签、涂鸦、电视头图标、交通牌、异常封条。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 低对比城市街角/古董店远景，异象元素放边缘，中心干净。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 4：城市渐变、贴纸、封条、简单光晕

### 5. Tool Background Prompt
> 生成超自然都市工具背景，夜蓝灰现代街区与古董店远景，边缘有霓虹招牌、委托单、异常封条、涂鸦和小怪谈图标，中央 50% 干净低纹理，低饱和低对比，无清晰文字、无假 UI、无角色主视觉。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成赛博朋克或纯二次元都市；需保留超自然怪谈和生活经营
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 异环
aliases: []
category: 超自然都市 / 开放世界 RPG
visual_identity: 超自然都市怪谈开放世界 RPG
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [urban-fantasy, supernatural, open-world]
misclassification_risks: 误判成赛博朋克或纯二次元都市；需保留超自然怪谈和生活经营
maker_feasibility_target: "4-5"
tags: [urban-fantasy, supernatural, open-world, anime]
```

## 21. 最强蜗牛

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/187376
- **game_type**: 放置 / 收集 / 荒诞剧情
- **core_gameplay**: 蜗牛进化、收集贵重品、探索和无厘头叙事
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 荒诞手账式蜗牛放置收集
- **genre_presentation**: 把放置收集视觉化为蜗牛基地、伪科学档案、博物馆藏品和密集梗图式幽默。
- **primary_mood**: 荒诞、搞笑、猎奇、收集癖
- **world_semantics**: 蜗牛壳、贵重品、基因、抽屉、档案、便签、地球仪、恶搞小物
- **common_ui_material_language**: 旧纸、手账贴纸、木桌、档案夹、复古塑料、瓶罐
- **shape_language**: 手作不规则、贴纸堆叠、圆角纸片、旧票据
- **palette_tendency**: 旧纸黄/木棕作底；红蓝印章作重点；绿色作成长/基因；紫金作稀有；红色作危险/吐槽
- **accent_semantics**: 蜗牛壳、印章、便签、瓶盖、旧票、博物馆标签
- **background_language**: 桌面手账/收藏柜边缘，中央留出浅纸面
- **misclassification_risks**: 误判成普通可爱动物或硬核科幻进化

### 3. Auto Game Style Brief
- **style_keywords**: 荒诞手账式蜗牛放置收集
- **mood**: 荒诞、搞笑、猎奇、收集癖
- **world_semantics**: 蜗牛壳、贵重品、基因、抽屉、档案、便签、地球仪、恶搞小物
- **material_language**: 旧纸、手账贴纸、木桌、档案夹、复古塑料、瓶罐
- **shape_language**: 手作不规则、贴纸堆叠、圆角纸片、旧票据
- **palette_intent**: 旧纸黄/木棕作底；红蓝印章作重点；绿色作成长/基因；紫金作稀有；红色作危险/吐槽
- **state_language**: selected 用红蓝印章或金色藏品框；warning 用红色吐槽标
- **accent_semantics**: 蜗牛壳、印章、便签、瓶盖、旧票、博物馆标签
- **background_language**: 桌面手账/收藏柜边缘，中央留出浅纸面
- **forbidden_directions**: 误判成普通可爱动物或硬核科幻进化
- **maker_safe_assets**: Maker 目标 5：贴纸、纸纹、印章、收藏品 icon

### 4. UI Translation Recommendations
- **panel_design**: 纸片堆叠卡+印章角标，大卡可放藏品阴影，小卡不要堆梗
- **state_design**: selected 用红蓝印章或金色藏品框；warning 用红色吐槽标
- **text_design**: 标题可手账粗体，正文黑棕清晰
- **accent_design**: 蜗牛壳、印章、便签、瓶盖、旧票、博物馆标签。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 桌面手账/收藏柜边缘，中央留出浅纸面。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 5：贴纸、纸纹、印章、收藏品 icon

### 5. Tool Background Prompt
> 生成荒诞手账式放置收集工具背景，旧纸黄和木桌基调，边缘有蜗牛壳、便签、档案夹、印章、瓶盖和收藏柜阴影，中央 50% 清爽纸面安全区，低对比，无清晰文字、无假 UI。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成普通可爱动物或硬核科幻进化
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 最强蜗牛
aliases: []
category: 放置 / 收集 / 荒诞剧情
visual_identity: 荒诞手账式蜗牛放置收集
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [idle, absurd, scrapbook]
misclassification_risks: 误判成普通可爱动物或硬核科幻进化
maker_feasibility_target: "4-5"
tags: [idle, absurd, scrapbook, collection]
```

## 22. 明日方舟

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/70253
- **game_type**: 策略塔防 / 二次元 / 末世科幻
- **core_gameplay**: 干员部署、感染者叙事、罗德岛制药和战术关卡
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 医疗工业末世策略 UI
- **genre_presentation**: 把塔防视觉化为制药公司终端、干员档案、灾害警报、黑白灰工业和战术网格。
- **primary_mood**: 克制、严肃、专业、压抑
- **world_semantics**: 罗德岛、感染、源石、医疗箱、干员档案、战术地图、警示标识
- **common_ui_material_language**: 黑白工业终端、医疗档案纸、磨砂玻璃、橙色警示胶带
- **shape_language**: 硬边、切角、模块网格、编号、条形码
- **palette_tendency**: 黑白灰作主基调；青蓝作系统；橙黄作警示和选中；红色仅作危机/错误
- **accent_semantics**: 医疗十字、条形码、源石碎片、战术编号、警示线、档案夹
- **background_language**: 暗灰工业墙/战术地图远景，中心低纹理
- **misclassification_risks**: 误判成泛科幻蓝或废土脏乱；要保留医疗工业和档案克制

### 3. Auto Game Style Brief
- **style_keywords**: 医疗工业末世策略 UI
- **mood**: 克制、严肃、专业、压抑
- **world_semantics**: 罗德岛、感染、源石、医疗箱、干员档案、战术地图、警示标识
- **material_language**: 黑白工业终端、医疗档案纸、磨砂玻璃、橙色警示胶带
- **shape_language**: 硬边、切角、模块网格、编号、条形码
- **palette_intent**: 黑白灰作主基调；青蓝作系统；橙黄作警示和选中；红色仅作危机/错误
- **state_language**: selected 用橙黄短条/边框；warning 用红色危机，不作选中
- **accent_semantics**: 医疗十字、条形码、源石碎片、战术编号、警示线、档案夹
- **background_language**: 暗灰工业墙/战术地图远景，中心低纹理
- **forbidden_directions**: 误判成泛科幻蓝或废土脏乱；要保留医疗工业和档案克制
- **maker_safe_assets**: Maker 目标 5：矩形、切角、条形码、警示贴图

### 4. UI Translation Recommendations
- **panel_design**: 硬边黑白卡+橙色小条，卡片不要过度发光
- **state_design**: selected 用橙黄短条/边框；warning 用红色危机，不作选中
- **text_design**: 标题冷峻，正文白/黑高对比，信息层级明确
- **accent_design**: 医疗十字、条形码、源石碎片、战术编号、警示线、档案夹。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 暗灰工业墙/战术地图远景，中心低纹理。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 5：矩形、切角、条形码、警示贴图

### 5. Tool Background Prompt
> 生成医疗工业末世策略工具背景，黑白灰低饱和工业墙与战术地图线，边缘有橙色警示条、医疗十字、条形码和源石碎片，中央 50% 干净低纹理，无清晰文字、无假 UI。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成泛科幻蓝或废土脏乱；要保留医疗工业和档案克制
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 明日方舟
aliases: []
category: 策略塔防 / 二次元 / 末世科幻
visual_identity: 医疗工业末世策略 UI
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [arknights, tactical, industrial]
misclassification_risks: 误判成泛科幻蓝或废土脏乱；要保留医疗工业和档案克制
maker_feasibility_target: "4-5"
tags: [arknights, tactical, industrial, dystopia]
```

## 23. 尘白禁区

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/222089
- **game_type**: 科幻射击 / 二次元 / 动作
- **core_gameplay**: 队员协作、枪械射击、泰坦/灾变背景与基地系统
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 雪域战术科幻美少女射击
- **genre_presentation**: 把 TPS 视觉化为白灰冷色、战术装备、隔离区、枪械 HUD 和高洁净实验室质感。
- **primary_mood**: 冷峻、紧张、清洁、战斗
- **world_semantics**: 禁区、雪尘、枪械、战术服、实验室、数据终端、弹药、隔离门
- **common_ui_material_language**: 冷白磨砂玻璃、枪灰金属、冰蓝 HUD、橡胶装备
- **shape_language**: 硬边圆角混合、切角、数据线、装备插槽
- **palette_tendency**: 冷白/浅灰作面板；深灰作结构；冰蓝作系统；黄色作战术提示；红色只作伤害/警报
- **accent_semantics**: 弹匣、十字准星、隔离线、雪粒、芯片、装备槽
- **background_language**: 冷白实验室或雪域禁区远景，中心不放高亮角色
- **misclassification_risks**: 误判成通用蓝白科幻医疗；需保留枪械战术和禁区冷感

### 3. Auto Game Style Brief
- **style_keywords**: 雪域战术科幻美少女射击
- **mood**: 冷峻、紧张、清洁、战斗
- **world_semantics**: 禁区、雪尘、枪械、战术服、实验室、数据终端、弹药、隔离门
- **material_language**: 冷白磨砂玻璃、枪灰金属、冰蓝 HUD、橡胶装备
- **shape_language**: 硬边圆角混合、切角、数据线、装备插槽
- **palette_intent**: 冷白/浅灰作面板；深灰作结构；冰蓝作系统；黄色作战术提示；红色只作伤害/警报
- **state_language**: selected 用冰蓝描边；warning 用红色警报；locked 用隔离封条
- **accent_semantics**: 弹匣、十字准星、隔离线、雪粒、芯片、装备槽
- **background_language**: 冷白实验室或雪域禁区远景，中心不放高亮角色
- **forbidden_directions**: 误判成通用蓝白科幻医疗；需保留枪械战术和禁区冷感
- **maker_safe_assets**: Maker 目标 4：玻璃卡、线框、准星 icon、少量噪声

### 4. UI Translation Recommendations
- **panel_design**: 冷白半透明卡+灰色硬边，局部冰蓝线条
- **state_design**: selected 用冰蓝描边；warning 用红色警报；locked 用隔离封条
- **text_design**: 标题窄体科技感，正文深灰/白高可读
- **accent_design**: 弹匣、十字准星、隔离线、雪粒、芯片、装备槽。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 冷白实验室或雪域禁区远景，中心不放高亮角色。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 4：玻璃卡、线框、准星 icon、少量噪声

### 5. Tool Background Prompt
> 生成雪域战术科幻工具背景，冷白浅灰与冰蓝基调，边缘有实验室隔离门、枪械轮廓、准星、数据线和雪尘颗粒，中央 50% 干净低纹理，低对比，无角色、无假 UI、无清晰文字。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成通用蓝白科幻医疗；需保留枪械战术和禁区冷感
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 尘白禁区
aliases: []
category: 科幻射击 / 二次元 / 动作
visual_identity: 雪域战术科幻美少女射击
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [sci-fi, tactical, shooter]
misclassification_risks: 误判成通用蓝白科幻医疗；需保留枪械战术和禁区冷感
maker_feasibility_target: "4-5"
tags: [sci-fi, tactical, shooter, snow]
```

## 24. 球球旅行记

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/726060
- **game_type**: 烹饪 / 时间管理 / 旅行
- **core_gameplay**: 飞机厨房服务、乘客餐食、环球城市关卡和设备升级
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 环球航班烹饪时间管理
- **genre_presentation**: 把烹饪经营视觉化为空中厨房、托盘、城市旅行、快节奏服务和食物满足感。
- **primary_mood**: 明快、忙碌、治愈、旅行感
- **world_semantics**: 飞机舷窗、餐车、托盘、汉堡牛排、城市明信片、登机牌、厨房设备
- **common_ui_material_language**: 干净塑料托盘、航空蓝玻璃、菜单纸卡、不锈钢厨房面
- **shape_language**: 圆角卡、登机牌切角、托盘格、清爽图标
- **palette_tendency**: 天空蓝/云白作底；餐食暖黄/橙作奖励；深蓝作航空信息；绿色作完成；红色仅作超时
- **accent_semantics**: 登机牌、云朵、餐盘、城市贴纸、餐车、计时器
- **background_language**: 云层和机舱厨房远景，边缘放食物/城市明信片，中心清洁
- **misclassification_risks**: 误判成普通餐厅经营，必须保留航班和旅行语义

### 3. Auto Game Style Brief
- **style_keywords**: 环球航班烹饪时间管理
- **mood**: 明快、忙碌、治愈、旅行感
- **world_semantics**: 飞机舷窗、餐车、托盘、汉堡牛排、城市明信片、登机牌、厨房设备
- **material_language**: 干净塑料托盘、航空蓝玻璃、菜单纸卡、不锈钢厨房面
- **shape_language**: 圆角卡、登机牌切角、托盘格、清爽图标
- **palette_intent**: 天空蓝/云白作底；餐食暖黄/橙作奖励；深蓝作航空信息；绿色作完成；红色仅作超时
- **state_language**: selected 用蓝色登机牌边或金色餐盘；warning 用红色计时器
- **accent_semantics**: 登机牌、云朵、餐盘、城市贴纸、餐车、计时器
- **background_language**: 云层和机舱厨房远景，边缘放食物/城市明信片，中心清洁
- **forbidden_directions**: 误判成普通餐厅经营，必须保留航班和旅行语义
- **maker_safe_assets**: Maker 目标 5：圆角卡、食物/机票 icon、简单进度条

### 4. UI Translation Recommendations
- **panel_design**: 白蓝圆角卡+登机牌标签，食物图标小而干净
- **state_design**: selected 用蓝色登机牌边或金色餐盘；warning 用红色计时器
- **text_design**: 标题亲切圆体，正文深蓝灰
- **accent_design**: 登机牌、云朵、餐盘、城市贴纸、餐车、计时器。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 云层和机舱厨房远景，边缘放食物/城市明信片，中心清洁。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 5：圆角卡、食物/机票 icon、简单进度条

### 5. Tool Background Prompt
> 生成环球航班烹饪工具背景，天空蓝云白基调，边缘有飞机舷窗、餐车、托盘、城市明信片和少量食物图标，中央 50% 干净低纹理，低对比，无清晰文字、无假 UI。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成普通餐厅经营，必须保留航班和旅行语义
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 球球旅行记
aliases: []
category: 烹饪 / 时间管理 / 旅行
visual_identity: 环球航班烹饪时间管理
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [cooking, time-management, travel]
misclassification_risks: 误判成普通餐厅经营，必须保留航班和旅行语义
maker_feasibility_target: "4-5"
tags: [cooking, time-management, travel, airplane]
```

## 25. 绝区零

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/234493
- **game_type**: 都市动作 / 二次元 / 箱庭
- **core_gameplay**: 代理人战斗、录像店、空洞灾害、街区生活与潮流文化
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 潮流街区录像带式都市动作
- **genre_presentation**: 把动作游戏视觉化为街头文化、录像带故障、黑黄警示、贴纸招牌和高节奏打击感。
- **primary_mood**: 酷、躁动、幽默、街头
- **world_semantics**: 录像店、空洞、代理人、邦布、警示条、街头贴纸、CRT 噪声
- **common_ui_material_language**: 粗糙塑料、贴纸胶带、黑黄警示胶、CRT 玻璃、混凝土墙
- **shape_language**: 厚块面、粗描边、切角标签、斜贴纸、错位排版
- **palette_tendency**: 黑/白/灰作强对比；黄色作核心强调；红色作危险；青粉作为潮流点缀；避免大面积柔粉
- **accent_semantics**: 邦布图标、VHS、警示胶带、涂鸦、街牌、故障条
- **background_language**: 街区墙面/录像店远景，边缘贴纸和警示条，中心控制对比
- **misclassification_risks**: 误判成赛博朋克霓虹；核心是街头录像带与黑黄警示

### 3. Auto Game Style Brief
- **style_keywords**: 潮流街区录像带式都市动作
- **mood**: 酷、躁动、幽默、街头
- **world_semantics**: 录像店、空洞、代理人、邦布、警示条、街头贴纸、CRT 噪声
- **material_language**: 粗糙塑料、贴纸胶带、黑黄警示胶、CRT 玻璃、混凝土墙
- **shape_language**: 厚块面、粗描边、切角标签、斜贴纸、错位排版
- **palette_intent**: 黑/白/灰作强对比；黄色作核心强调；红色作危险；青粉作为潮流点缀；避免大面积柔粉
- **state_language**: selected 用黄色粗边/标签；warning 用红黑危险条；disabled 用灰化故障
- **accent_semantics**: 邦布图标、VHS、警示胶带、涂鸦、街牌、故障条
- **background_language**: 街区墙面/录像店远景，边缘贴纸和警示条，中心控制对比
- **forbidden_directions**: 误判成赛博朋克霓虹；核心是街头录像带与黑黄警示
- **maker_safe_assets**: Maker 目标 4：贴纸、斜标签、噪声纹理、简单抖动

### 4. UI Translation Recommendations
- **panel_design**: 厚卡+黑白底+黄色标签，贴纸层在 overlay 上方
- **state_design**: selected 用黄色粗边/标签；warning 用红黑危险条；disabled 用灰化故障
- **text_design**: 标题可粗体错位，正文必须黑白高对比
- **accent_design**: 邦布图标、VHS、警示胶带、涂鸦、街牌、故障条。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 街区墙面/录像店远景，边缘贴纸和警示条，中心控制对比。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 4：贴纸、斜标签、噪声纹理、简单抖动

### 5. Tool Background Prompt
> 生成潮流街区录像带都市动作工具背景，黑白灰城市墙面和暖黄警示条，边缘有录像带、涂鸦贴纸、街牌和 CRT 噪声，中央 50% 干净低纹理，低信息密度，无清晰文字、无假 UI、无角色。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成赛博朋克霓虹；核心是街头录像带与黑黄警示
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 绝区零
aliases: []
category: 都市动作 / 二次元 / 箱庭
visual_identity: 潮流街区录像带式都市动作
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [urban, street, action]
misclassification_risks: 误判成赛博朋克霓虹；核心是街头录像带与黑黄警示
maker_feasibility_target: "4-5"
tags: [urban, street, action, vhs]
```

## 26. 火影忍者

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/2247
- **game_type**: 横版格斗 / 动漫 IP
- **core_gameplay**: 忍者角色、忍术连招、奥义大招、2V2 和竞技格斗
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 热血忍者卷轴格斗
- **genre_presentation**: 把格斗视觉化为忍术、卷轴、查克拉、木叶标识和高速连击的动漫战斗气势。
- **primary_mood**: 热血、燃、速度、羁绊
- **world_semantics**: 木叶、护额、手里剑、卷轴、查克拉、苦无、忍术印、火之意志
- **common_ui_material_language**: 卷轴纸、忍具金属、木牌、布料护额、查克拉能量
- **shape_language**: 斜切速度线、卷轴边、粗描边、忍具角标
- **palette_tendency**: 橙红作热血/火；黑灰作忍具；米黄作卷轴；蓝色作查克拉；红色用于危险和火系强调
- **accent_semantics**: 手里剑、苦无、护额、卷轴、忍术印、火焰、疾风线
- **background_language**: 忍村屋檐/卷轴纹理远景，中心清爽不放角色战斗
- **misclassification_risks**: 误判成泛日式武士或普通动漫热血；必须保留忍术和卷轴

### 3. Auto Game Style Brief
- **style_keywords**: 热血忍者卷轴格斗
- **mood**: 热血、燃、速度、羁绊
- **world_semantics**: 木叶、护额、手里剑、卷轴、查克拉、苦无、忍术印、火之意志
- **material_language**: 卷轴纸、忍具金属、木牌、布料护额、查克拉能量
- **shape_language**: 斜切速度线、卷轴边、粗描边、忍具角标
- **palette_intent**: 橙红作热血/火；黑灰作忍具；米黄作卷轴；蓝色作查克拉；红色用于危险和火系强调
- **state_language**: selected 用蓝色查克拉或橙色火光；warning 用红色爆符
- **accent_semantics**: 手里剑、苦无、护额、卷轴、忍术印、火焰、疾风线
- **background_language**: 忍村屋檐/卷轴纹理远景，中心清爽不放角色战斗
- **forbidden_directions**: 误判成泛日式武士或普通动漫热血；必须保留忍术和卷轴
- **maker_safe_assets**: Maker 目标 4：卷轴边、忍具 icon、速度线贴图

### 4. UI Translation Recommendations
- **panel_design**: 卷轴卡+金属护额条，大卡可加查克拉速度线
- **state_design**: selected 用蓝色查克拉或橙色火光；warning 用红色爆符
- **text_design**: 标题可粗劲动漫感，正文深棕/白高可读
- **accent_design**: 手里剑、苦无、护额、卷轴、忍术印、火焰、疾风线。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 忍村屋檐/卷轴纹理远景，中心清爽不放角色战斗。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 4：卷轴边、忍具 icon、速度线贴图

### 5. Tool Background Prompt
> 生成热血忍者卷轴格斗工具背景，米黄卷轴纸与深灰忍具基调，边缘有木叶屋檐、手里剑、苦无、护额、橙色火焰和蓝色查克拉线，中央 50% 干净低纹理，无清晰文字、无假 UI、无角色。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成泛日式武士或普通动漫热血；必须保留忍术和卷轴
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 火影忍者
aliases: []
category: 横版格斗 / 动漫 IP
visual_identity: 热血忍者卷轴格斗
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [ninja, anime, fighting]
misclassification_risks: 误判成泛日式武士或普通动漫热血；必须保留忍术和卷轴
maker_feasibility_target: "4-5"
tags: [ninja, anime, fighting, scroll]
```

## 27. 龙族：卡塞尔之门

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/382099
- **game_type**: 策略 RPG / 都市幻想 / IP
- **core_gameplay**: 卡塞尔学院、混血种、屠龙冒险、言灵与角色羁绊
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 黑金学院派屠龙都市幻想
- **genre_presentation**: 把策略 RPG 视觉化为精英学院、龙血秘仪、言灵档案、黑金校徽和青春宿命感。
- **primary_mood**: 热血、忧郁、神秘、学院感
- **world_semantics**: 卡塞尔学院、龙血、言灵、校徽、长剑、档案、论坛、混血种
- **common_ui_material_language**: 黑金金属、皮革档案、学院徽章、暗色玻璃、羊皮纸
- **shape_language**: 学院徽章、细金边、暗色卡、锐角装饰
- **palette_tendency**: 黑/深棕作底；金色作学院荣耀；暗红作龙血/危机；冷蓝作言灵；米白作档案
- **accent_semantics**: 校徽、龙鳞、长剑、档案夹、封蜡、论坛标签
- **background_language**: 暗色学院走廊/档案馆远景，中心保持阅读区
- **misclassification_risks**: 误判成普通西幻屠龙或青春校园；需要都市学院和龙族宿命

### 3. Auto Game Style Brief
- **style_keywords**: 黑金学院派屠龙都市幻想
- **mood**: 热血、忧郁、神秘、学院感
- **world_semantics**: 卡塞尔学院、龙血、言灵、校徽、长剑、档案、论坛、混血种
- **material_language**: 黑金金属、皮革档案、学院徽章、暗色玻璃、羊皮纸
- **shape_language**: 学院徽章、细金边、暗色卡、锐角装饰
- **palette_intent**: 黑/深棕作底；金色作学院荣耀；暗红作龙血/危机；冷蓝作言灵；米白作档案
- **state_language**: selected 用金边校徽；warning 用暗红龙血封条
- **accent_semantics**: 校徽、龙鳞、长剑、档案夹、封蜡、论坛标签
- **background_language**: 暗色学院走廊/档案馆远景，中心保持阅读区
- **forbidden_directions**: 误判成普通西幻屠龙或青春校园；需要都市学院和龙族宿命
- **maker_safe_assets**: Maker 目标 4：金边卡、徽章、封蜡贴图

### 4. UI Translation Recommendations
- **panel_design**: 暗色档案卡+金边徽章，大卡可加封蜡/龙鳞纹
- **state_design**: selected 用金边校徽；warning 用暗红龙血封条
- **text_design**: 标题学院 serif/黑体混合，正文米白/浅灰清晰
- **accent_design**: 校徽、龙鳞、长剑、档案夹、封蜡、论坛标签。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 暗色学院走廊/档案馆远景，中心保持阅读区。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 4：金边卡、徽章、封蜡贴图

### 5. Tool Background Prompt
> 生成黑金学院派屠龙都市幻想工具背景，深棕黑与暗金基调，边缘有学院走廊、校徽、龙鳞、长剑、档案夹和封蜡，中央 50% 干净低纹理，低对比，无清晰文字、无假 UI、无角色。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成普通西幻屠龙或青春校园；需要都市学院和龙族宿命
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 龙族：卡塞尔之门
aliases: []
category: 策略 RPG / 都市幻想 / IP
visual_identity: 黑金学院派屠龙都市幻想
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [urban-fantasy, dragon, academy]
misclassification_risks: 误判成普通西幻屠龙或青春校园；需要都市学院和龙族宿命
maker_feasibility_target: "4-5"
tags: [urban-fantasy, dragon, academy, strategy-rpg]
```

## 28. TapAim

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/815993
- **game_type**: FPS 训练工具 / 靶场
- **core_gameplay**: 移动端 FPS 靶场、练枪、反应和天赋测试
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 专业轻量移动 FPS 靶场工具
- **genre_presentation**: 把训练工具视觉化为干净靶场、数据指标、准星、命中率和性能测试界面。
- **primary_mood**: 专业、清晰、效率、训练感
- **world_semantics**: 准星、靶球、命中率、反应时间、灵敏度、排行榜、训练模块
- **common_ui_material_language**: 深浅 HUD 面板、磨砂玻璃、靶场墙面、数据卡
- **shape_language**: 极简硬边、圆形靶点、网格、进度条
- **palette_tendency**: 深灰/白作底；蓝色作训练系统；绿色作通过/提升；橙色作注意；红色只作失误
- **accent_semantics**: 准星、靶心、计时器、数据柱、触控点、陀螺仪图标
- **background_language**: 低对比靶场网格或训练室墙面，中心安全区留白
- **misclassification_risks**: 误判成军事战场；它更像训练工具而非战斗场景

### 3. Auto Game Style Brief
- **style_keywords**: 专业轻量移动 FPS 靶场工具
- **mood**: 专业、清晰、效率、训练感
- **world_semantics**: 准星、靶球、命中率、反应时间、灵敏度、排行榜、训练模块
- **material_language**: 深浅 HUD 面板、磨砂玻璃、靶场墙面、数据卡
- **shape_language**: 极简硬边、圆形靶点、网格、进度条
- **palette_intent**: 深灰/白作底；蓝色作训练系统；绿色作通过/提升；橙色作注意；红色只作失误
- **state_language**: selected 用蓝色准星框；warning 用橙/红失误标识
- **accent_semantics**: 准星、靶心、计时器、数据柱、触控点、陀螺仪图标
- **background_language**: 低对比靶场网格或训练室墙面，中心安全区留白
- **forbidden_directions**: 误判成军事战场；它更像训练工具而非战斗场景
- **maker_safe_assets**: Maker 目标 5：圆点、准星、数据条、轻量 HUD

### 4. UI Translation Recommendations
- **panel_design**: 清爽数据卡+靶心 icon，避免战场脏污纹理
- **state_design**: selected 用蓝色准星框；warning 用橙/红失误标识
- **text_design**: 标题科技无衬线，数字大且清晰
- **accent_design**: 准星、靶心、计时器、数据柱、触控点、陀螺仪图标。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 低对比靶场网格或训练室墙面，中心安全区留白。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 5：圆点、准星、数据条、轻量 HUD

### 5. Tool Background Prompt
> 生成专业移动 FPS 靶场工具背景，深灰与白色训练室网格，边缘有蓝色准星、靶点、命中率数据条和计时器图标，中央 55% 干净低纹理，低对比，无清晰文字、无假 UI、无战场人物。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成军事战场；它更像训练工具而非战斗场景
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: TapAim
aliases: []
category: FPS 训练工具 / 靶场
visual_identity: 专业轻量移动 FPS 靶场工具
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [fps-training, utility, aim]
misclassification_risks: 误判成军事战场；它更像训练工具而非战斗场景
maker_feasibility_target: "4-5"
tags: [fps-training, utility, aim, hud]
```

## 29. 江南百景图

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/179371
- **game_type**: 模拟经营 / 古风建造
- **core_gameplay**: 古代江南城市营造、居民、生产与布局
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 雅致江南水墨市井营造
- **genre_presentation**: 把模拟经营视觉化为江南画卷、白墙黛瓦、水路桥巷、印章和古籍账册。
- **primary_mood**: 雅致、烟火气、古朴、悠然
- **world_semantics**: 江南水乡、白墙黛瓦、石桥、船、灯笼、账册、印章、亭台
- **common_ui_material_language**: 宣纸、青砖、木牌、古籍账本、印泥、淡墨
- **shape_language**: 卷轴边、细墨线、方形印章、屋檐角、留白
- **palette_tendency**: 米白/宣纸黄作面板；墨黑作文字；黛青/水绿作环境；朱砂作印章和重点；金色少量作奖励
- **accent_semantics**: 印章、折扇、船桨、灯笼、瓦片、铜钱、桥纹
- **background_language**: 淡墨江南远景，边缘白墙黛瓦/水波，中心干净宣纸
- **misclassification_risks**: 误判成宫廷金红或仙侠水墨；需保留市井经营和江南雅致

### 3. Auto Game Style Brief
- **style_keywords**: 雅致江南水墨市井营造
- **mood**: 雅致、烟火气、古朴、悠然
- **world_semantics**: 江南水乡、白墙黛瓦、石桥、船、灯笼、账册、印章、亭台
- **material_language**: 宣纸、青砖、木牌、古籍账本、印泥、淡墨
- **shape_language**: 卷轴边、细墨线、方形印章、屋檐角、留白
- **palette_intent**: 米白/宣纸黄作面板；墨黑作文字；黛青/水绿作环境；朱砂作印章和重点；金色少量作奖励
- **state_language**: selected 用朱砂印章；warning 用暗红告示；locked 用木牌锁
- **accent_semantics**: 印章、折扇、船桨、灯笼、瓦片、铜钱、桥纹
- **background_language**: 淡墨江南远景，边缘白墙黛瓦/水波，中心干净宣纸
- **forbidden_directions**: 误判成宫廷金红或仙侠水墨；需保留市井经营和江南雅致
- **maker_safe_assets**: Maker 目标 5：纸纹、印章、瓦片/桥 icon

### 4. UI Translation Recommendations
- **panel_design**: 宣纸面板+淡墨边+朱砂印，小卡简洁
- **state_design**: selected 用朱砂印章；warning 用暗红告示；locked 用木牌锁
- **text_design**: 标题可古风但正文深墨清晰
- **accent_design**: 印章、折扇、船桨、灯笼、瓦片、铜钱、桥纹。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 淡墨江南远景，边缘白墙黛瓦/水波，中心干净宣纸。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 5：纸纹、印章、瓦片/桥 icon

### 5. Tool Background Prompt
> 生成雅致江南水墨市井工具背景，米白宣纸与淡青水墨基调，边缘有白墙黛瓦、石桥、水波、灯笼和朱砂印章，中央 50% 干净低纹理，无清晰文字、无假 UI、无角色。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成宫廷金红或仙侠水墨；需保留市井经营和江南雅致
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 江南百景图
aliases: []
category: 模拟经营 / 古风建造
visual_identity: 雅致江南水墨市井营造
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [jiangnan, ink, city-builder]
misclassification_risks: 误判成宫廷金红或仙侠水墨；需保留市井经营和江南雅致
maker_feasibility_target: "4-5"
tags: [jiangnan, ink, city-builder, ancient-china]
```

## 30. 名将杀

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/737825
- **game_type**: 卡牌 / 历史 / 桌游策略
- **core_gameplay**: 经典杀牌身份策略、战国至秦汉名将策士与多人博弈
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 战国秦汉谋略杀牌桌游
- **genre_presentation**: 把卡牌策略视觉化为竹简、兵符、青铜器、战旗和历史谋略牌局。
- **primary_mood**: 谋略、古朴、竞技、烽火
- **world_semantics**: 名将、策士、竹简、兵符、战旗、杀牌、古战场、秦汉纹样
- **common_ui_material_language**: 竹简、羊皮纸、青铜、暗木桌面、印章
- **shape_language**: 矩形牌框、青铜浮雕、竹简横线、旗帜角标
- **palette_tendency**: 竹简黄/暗木棕作底；青铜绿作边框；朱砂红作杀/攻击；金色作稀有/胜利；黑墨作文字
- **accent_semantics**: 兵符、战旗、印章、剑戈、竹简、火漆
- **background_language**: 古战场或木桌牌局边缘，中心留出纸面安全区
- **misclassification_risks**: 误判成三国武将立绘手游；要保留桌游卡牌和秦汉谋略

### 3. Auto Game Style Brief
- **style_keywords**: 战国秦汉谋略杀牌桌游
- **mood**: 谋略、古朴、竞技、烽火
- **world_semantics**: 名将、策士、竹简、兵符、战旗、杀牌、古战场、秦汉纹样
- **material_language**: 竹简、羊皮纸、青铜、暗木桌面、印章
- **shape_language**: 矩形牌框、青铜浮雕、竹简横线、旗帜角标
- **palette_intent**: 竹简黄/暗木棕作底；青铜绿作边框；朱砂红作杀/攻击；金色作稀有/胜利；黑墨作文字
- **state_language**: selected 用金色牌框或朱砂印；warning 用红色杀牌，不作普通选中
- **accent_semantics**: 兵符、战旗、印章、剑戈、竹简、火漆
- **background_language**: 古战场或木桌牌局边缘，中心留出纸面安全区
- **forbidden_directions**: 误判成三国武将立绘手游；要保留桌游卡牌和秦汉谋略
- **maker_safe_assets**: Maker 目标 4：卡牌框、竹简纹、兵符 icon

### 4. UI Translation Recommendations
- **panel_design**: 卡牌式面板+青铜边，普通小卡减少浮雕
- **state_design**: selected 用金色牌框或朱砂印；warning 用红色杀牌，不作普通选中
- **text_design**: 标题古朴硬朗，正文深墨清楚
- **accent_design**: 兵符、战旗、印章、剑戈、竹简、火漆。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 古战场或木桌牌局边缘，中心留出纸面安全区。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 4：卡牌框、竹简纹、兵符 icon

### 5. Tool Background Prompt
> 生成战国秦汉谋略杀牌工具背景，竹简黄与暗木棕基调，边缘有青铜纹、战旗、兵符、卡牌角标和淡淡烽火远景，中央 50% 干净低纹理，低对比，无清晰文字、无假 UI。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成三国武将立绘手游；要保留桌游卡牌和秦汉谋略
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 名将杀
aliases: []
category: 卡牌 / 历史 / 桌游策略
visual_identity: 战国秦汉谋略杀牌桌游
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [card, history, strategy]
misclassification_risks: 误判成三国武将立绘手游；要保留桌游卡牌和秦汉谋略
maker_feasibility_target: "4-5"
tags: [card, history, strategy, tabletop]
```

## 31. 再玩亿关

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/247977
- **game_type**: 休闲解压 / 迷你游戏合集
- **core_gameplay**: 多类型解压、拼图、收纳、体育、益智和迷你关卡合集
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 清新可爱解压迷你游戏合集
- **genre_presentation**: 把休闲合集视觉化为柔和卡通、满足感小物、收纳格、拼图块和轻量挑战。
- **primary_mood**: 轻松、满足、治愈、亲民
- **world_semantics**: 拼图、收纳盒、按钮机关、小球、清洁、体育小物、关卡卡片
- **common_ui_material_language**: 柔软塑料、纸卡、橡皮泥、浅色收纳盒
- **shape_language**: 圆润块面、卡片网格、拼图边、软按钮
- **palette_tendency**: 浅米白/浅蓝作底；马卡龙粉绿黄作分类；橙黄作完成奖励；红色仅作失败
- **accent_semantics**: 拼图块、收纳格、小星星、手指提示、清洁刷、勾选贴纸
- **background_language**: 浅色桌面/收纳盒远景，中央清爽
- **misclassification_risks**: 误判成幼儿教育或单一三消；需保留多玩法合集和解压感

### 3. Auto Game Style Brief
- **style_keywords**: 清新可爱解压迷你游戏合集
- **mood**: 轻松、满足、治愈、亲民
- **world_semantics**: 拼图、收纳盒、按钮机关、小球、清洁、体育小物、关卡卡片
- **material_language**: 柔软塑料、纸卡、橡皮泥、浅色收纳盒
- **shape_language**: 圆润块面、卡片网格、拼图边、软按钮
- **palette_intent**: 浅米白/浅蓝作底；马卡龙粉绿黄作分类；橙黄作完成奖励；红色仅作失败
- **state_language**: selected 用黄色星星/勾选；warning 用小红叉
- **accent_semantics**: 拼图块、收纳格、小星星、手指提示、清洁刷、勾选贴纸
- **background_language**: 浅色桌面/收纳盒远景，中央清爽
- **forbidden_directions**: 误判成幼儿教育或单一三消；需保留多玩法合集和解压感
- **maker_safe_assets**: Maker 目标 5：圆角卡、拼图/勾选 icon、简单缩放

### 4. UI Translation Recommendations
- **panel_design**: 白色圆角卡+马卡龙分类标签，小卡极简
- **state_design**: selected 用黄色星星/勾选；warning 用小红叉
- **text_design**: 标题可圆润亲切，正文深灰
- **accent_design**: 拼图块、收纳格、小星星、手指提示、清洁刷、勾选贴纸。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 浅色桌面/收纳盒远景，中央清爽。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 5：圆角卡、拼图/勾选 icon、简单缩放

### 5. Tool Background Prompt
> 生成清新可爱解压迷你游戏工具背景，浅米白和马卡龙蓝绿粉基调，边缘有拼图块、收纳盒、小星星、清洁刷和勾选贴纸，中央 55% 干净低纹理，无清晰文字、无假 UI。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成幼儿教育或单一三消；需保留多玩法合集和解压感
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 再玩亿关
aliases: []
category: 休闲解压 / 迷你游戏合集
visual_identity: 清新可爱解压迷你游戏合集
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [casual, mini-games, satisfying]
misclassification_risks: 误判成幼儿教育或单一三消；需保留多玩法合集和解压感
maker_feasibility_target: "4-5"
tags: [casual, mini-games, satisfying, cute]
```

## 32. 遗弃之地

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/753196
- **game_type**: 中式民俗恐怖 / 横版策略塔防
- **core_gameplay**: 修法者、符咒天书、阴阳两界、随机法术和横版策略防守
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 黑白皮影中式民俗轻恐怖塔防
- **genre_presentation**: 把策略塔防视觉化为黑白剪影、皮影傀儡、符咒、阴阳界和低饱和恐怖民俗。
- **primary_mood**: 阴冷、诡异、克制、玄秘
- **world_semantics**: 皮影、符咒、天书、阴阳、修法者、纸人、傀儡线、法术手牌
- **common_ui_material_language**: 旧纸符、黑墨剪影、朱砂印、木刻皮影、暗色纸屏
- **shape_language**: 剪影边、符纸条、破损纸边、横版层次、细红线
- **palette_tendency**: 黑白灰作主视觉；旧纸黄作面板；朱砂红作法力/危险；暗青作阴气；避免鲜艳彩色
- **accent_semantics**: 符箓、纸人、傀儡线、铜钱、香炉、朱砂印
- **background_language**: 黑白纸屏/村落剪影远景，中央旧纸低纹理安全区
- **misclassification_risks**: 误判成血腥恐怖或普通水墨仙侠；应是民俗轻恐怖+皮影

### 3. Auto Game Style Brief
- **style_keywords**: 黑白皮影中式民俗轻恐怖塔防
- **mood**: 阴冷、诡异、克制、玄秘
- **world_semantics**: 皮影、符咒、天书、阴阳、修法者、纸人、傀儡线、法术手牌
- **material_language**: 旧纸符、黑墨剪影、朱砂印、木刻皮影、暗色纸屏
- **shape_language**: 剪影边、符纸条、破损纸边、横版层次、细红线
- **palette_intent**: 黑白灰作主视觉；旧纸黄作面板；朱砂红作法力/危险；暗青作阴气；避免鲜艳彩色
- **state_language**: selected 用朱砂印/红线；warning 用暗红符火；disabled 用灰白褪色
- **accent_semantics**: 符箓、纸人、傀儡线、铜钱、香炉、朱砂印
- **background_language**: 黑白纸屏/村落剪影远景，中央旧纸低纹理安全区
- **forbidden_directions**: 误判成血腥恐怖或普通水墨仙侠；应是民俗轻恐怖+皮影
- **maker_safe_assets**: Maker 目标 4：符纸、剪影、纸纹、红线，无复杂恐怖粒子

### 4. UI Translation Recommendations
- **panel_design**: 旧纸符面板+黑墨边，大卡可加皮影剪影，小卡克制
- **state_design**: selected 用朱砂印/红线；warning 用暗红符火；disabled 用灰白褪色
- **text_design**: 标题可篆刻/民俗感，正文黑墨清晰
- **accent_design**: 符箓、纸人、傀儡线、铜钱、香炉、朱砂印。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 黑白纸屏/村落剪影远景，中央旧纸低纹理安全区。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 4：符纸、剪影、纸纹、红线，无复杂恐怖粒子

### 5. Tool Background Prompt
> 生成黑白皮影中式民俗轻恐怖工具背景，旧纸黄和黑白灰基调，边缘有皮影剪影、符咒、纸人、傀儡线和少量朱砂红印，中央 50% 干净低纹理，无清晰文字、无假 UI、不过暗。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成血腥恐怖或普通水墨仙侠；应是民俗轻恐怖+皮影
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 遗弃之地
aliases: []
category: 中式民俗恐怖 / 横版策略塔防
visual_identity: 黑白皮影中式民俗轻恐怖塔防
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [folk-horror, shadow-puppet, tower-defense]
misclassification_risks: 误判成血腥恐怖或普通水墨仙侠；应是民俗轻恐怖+皮影
maker_feasibility_target: "4-5"
tags: [folk-horror, shadow-puppet, tower-defense, chinese]
```

## 33. 吉星派对

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/524022
- **game_type**: 联机派对 / 卡牌 / 二次元
- **core_gameplay**: 4 人派对、角色技能、手牌攻击、随机事件和友尽博弈
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 恶搞卡通二次元友尽派对
- **genre_presentation**: 把多人派对视觉化为卡牌陷阱、随机事件、夸张表情和明亮可爱的恶搞舞台。
- **primary_mood**: 欢乐、混乱、恶搞、竞技
- **world_semantics**: 4人棋盘、角色技能牌、随机事件、骰子、表情、恶作剧道具
- **common_ui_material_language**: 亮面纸牌、塑料棋子、贴纸、舞台灯牌
- **shape_language**: 圆润卡牌、厚描边、夸张表情框、彩色标签
- **palette_tendency**: 亮蓝/粉/黄作派对底；白色作信息卡；紫色作事件；红色只作攻击/惩罚
- **accent_semantics**: 骰子、卡牌、炸弹玩具、星星、表情贴纸、舞台灯
- **background_language**: 派对棋盘或舞台远景，边缘放卡牌/骰子，中心清爽
- **misclassification_risks**: 误判成普通美少女卡牌或低龄派对；需保留友尽随机事件

### 3. Auto Game Style Brief
- **style_keywords**: 恶搞卡通二次元友尽派对
- **mood**: 欢乐、混乱、恶搞、竞技
- **world_semantics**: 4人棋盘、角色技能牌、随机事件、骰子、表情、恶作剧道具
- **material_language**: 亮面纸牌、塑料棋子、贴纸、舞台灯牌
- **shape_language**: 圆润卡牌、厚描边、夸张表情框、彩色标签
- **palette_intent**: 亮蓝/粉/黄作派对底；白色作信息卡；紫色作事件；红色只作攻击/惩罚
- **state_language**: selected 用黄色聚光灯/卡牌边；warning 用红色恶作剧标
- **accent_semantics**: 骰子、卡牌、炸弹玩具、星星、表情贴纸、舞台灯
- **background_language**: 派对棋盘或舞台远景，边缘放卡牌/骰子，中心清爽
- **forbidden_directions**: 误判成普通美少女卡牌或低龄派对；需保留友尽随机事件
- **maker_safe_assets**: Maker 目标 5：卡牌框、骰子、贴纸、弹跳 tween

### 4. UI Translation Recommendations
- **panel_design**: 纸牌面板+彩色标签，小卡可像手牌
- **state_design**: selected 用黄色聚光灯/卡牌边；warning 用红色恶作剧标
- **text_design**: 标题活泼粗体，正文高对比
- **accent_design**: 骰子、卡牌、炸弹玩具、星星、表情贴纸、舞台灯。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 派对棋盘或舞台远景，边缘放卡牌/骰子，中心清爽。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 5：卡牌框、骰子、贴纸、弹跳 tween

### 5. Tool Background Prompt
> 生成恶搞二次元友尽派对工具背景，明亮蓝粉黄舞台或棋盘远景，边缘有卡牌、骰子、表情贴纸、玩具炸弹和星星，中央 50% 干净低纹理，低信息密度，无清晰文字、无假 UI。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成普通美少女卡牌或低龄派对；需保留友尽随机事件
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 吉星派对
aliases: []
category: 联机派对 / 卡牌 / 二次元
visual_identity: 恶搞卡通二次元友尽派对
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [party, anime, cards]
misclassification_risks: 误判成普通美少女卡牌或低龄派对；需保留友尽随机事件
maker_feasibility_target: "4-5"
tags: [party, anime, cards, chaos]
```

## 34. 铃兰之剑：为这和平的世界

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/209866
- **game_type**: 战棋 RPG / 中世纪幻想
- **core_gameplay**: 像素/HD-2D 风格战棋、佣兵团、国家冲突与叙事选择
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 温厚复古中世纪战棋史诗
- **genre_presentation**: 把战棋 RPG 视觉化为羊皮地图、佣兵旗帜、石质城镇、古典战术棋盘与怀旧像素质感。
- **primary_mood**: 史诗、温厚、策略、怀旧
- **world_semantics**: 佣兵团、棋盘格、羊皮地图、旗帜、长剑、石墙、酒馆、命运选择
- **common_ui_material_language**: 羊皮纸、旧木、石板、金属徽章、布旗
- **shape_language**: 厚实纸卡、棋盘格、旗帜角、像素细节
- **palette_tendency**: 羊皮黄作面板；棕/石灰作结构；深蓝/红作阵营；金色作奖励；红色用于敌对和危险
- **accent_semantics**: 旗帜、剑盾、地图针、酒馆杯、像素小徽章
- **background_language**: 羊皮地图/石城远景，中心低纹理
- **misclassification_risks**: 误判成日系轻幻想或暗黑西幻；需保留复古战棋和温厚叙事

### 3. Auto Game Style Brief
- **style_keywords**: 温厚复古中世纪战棋史诗
- **mood**: 史诗、温厚、策略、怀旧
- **world_semantics**: 佣兵团、棋盘格、羊皮地图、旗帜、长剑、石墙、酒馆、命运选择
- **material_language**: 羊皮纸、旧木、石板、金属徽章、布旗
- **shape_language**: 厚实纸卡、棋盘格、旗帜角、像素细节
- **palette_intent**: 羊皮黄作面板；棕/石灰作结构；深蓝/红作阵营；金色作奖励；红色用于敌对和危险
- **state_language**: selected 用金色棋格边；warning 用红色敌军旗
- **accent_semantics**: 旗帜、剑盾、地图针、酒馆杯、像素小徽章
- **background_language**: 羊皮地图/石城远景，中心低纹理
- **forbidden_directions**: 误判成日系轻幻想或暗黑西幻；需保留复古战棋和温厚叙事
- **maker_safe_assets**: Maker 目标 4：纸纹、棋盘淡纹、旗帜 icon

### 4. UI Translation Recommendations
- **panel_design**: 羊皮纸面板+旧木边，大卡可加棋盘格淡纹
- **state_design**: selected 用金色棋格边；warning 用红色敌军旗
- **text_design**: 标题古典，正文深棕清晰
- **accent_design**: 旗帜、剑盾、地图针、酒馆杯、像素小徽章。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 羊皮地图/石城远景，中心低纹理。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 4：纸纹、棋盘淡纹、旗帜 icon

### 5. Tool Background Prompt
> 生成复古中世纪战棋工具背景，羊皮纸与石灰棕基调，边缘有棋盘格、佣兵旗帜、长剑、地图针和石墙远景，中央 50% 干净低纹理，无清晰文字、无假 UI。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成日系轻幻想或暗黑西幻；需保留复古战棋和温厚叙事
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 铃兰之剑：为这和平的世界
aliases: []
category: 战棋 RPG / 中世纪幻想
visual_identity: 温厚复古中世纪战棋史诗
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [tactics-rpg, medieval, retro]
misclassification_risks: 误判成日系轻幻想或暗黑西幻；需保留复古战棋和温厚叙事
maker_feasibility_target: "4-5"
tags: [tactics-rpg, medieval, retro, hd2d]
```

## 35. 无限升级

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/241449
- **game_type**: 放置 RPG / 数值养成
- **core_gameplay**: 传统 RPG 养成、刷怪爆装、装备强化附魔、转生和御灵养成
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 传统数值放置 RPG 爆装成长
- **genre_presentation**: 把放置 RPG 视觉化为装备栏、属性面板、强化石、转生印记和持续升级的数字爽感。
- **primary_mood**: 爽快、直给、成长、收集
- **world_semantics**: 装备、宝石、神器、御灵、转生、技能、强化、属性数值
- **common_ui_material_language**: 暗色面板、金属装备槽、宝石按钮、卷轴属性卡
- **shape_language**: 矩形装备槽、硬边、等级标签、进度条、数值高亮
- **palette_tendency**: 深蓝黑/暗棕作底；金色作品质和提升；紫色作神器；绿色作成长；红色只作战斗伤害
- **accent_semantics**: 装备槽、宝石、箭头上升、等级牌、转生印、技能书
- **background_language**: 暗色装备仓/属性页远景，中央留出数值安全区
- **misclassification_risks**: 误判成通用魔幻 RPG；要保留纯数值成长和装备爆装

### 3. Auto Game Style Brief
- **style_keywords**: 传统数值放置 RPG 爆装成长
- **mood**: 爽快、直给、成长、收集
- **world_semantics**: 装备、宝石、神器、御灵、转生、技能、强化、属性数值
- **material_language**: 暗色面板、金属装备槽、宝石按钮、卷轴属性卡
- **shape_language**: 矩形装备槽、硬边、等级标签、进度条、数值高亮
- **palette_intent**: 深蓝黑/暗棕作底；金色作品质和提升；紫色作神器；绿色作成长；红色只作战斗伤害
- **state_language**: selected 用金色品质框；warning 用红色伤害/失败强化
- **accent_semantics**: 装备槽、宝石、箭头上升、等级牌、转生印、技能书
- **background_language**: 暗色装备仓/属性页远景，中央留出数值安全区
- **forbidden_directions**: 误判成通用魔幻 RPG；要保留纯数值成长和装备爆装
- **maker_safe_assets**: Maker 目标 5：矩形槽、品质边框、进度条、简单数字跳动

### 4. UI Translation Recommendations
- **panel_design**: 深色装备卡+金属边，小卡像装备格
- **state_design**: selected 用金色品质框；warning 用红色伤害/失败强化
- **text_design**: 标题硬朗，数字要大且清楚
- **accent_design**: 装备槽、宝石、箭头上升、等级牌、转生印、技能书。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 暗色装备仓/属性页远景，中央留出数值安全区。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 5：矩形槽、品质边框、进度条、简单数字跳动

### 5. Tool Background Prompt
> 生成传统数值放置 RPG 工具背景，暗蓝黑与金属棕基调，边缘有装备槽、宝石、技能书、升级箭头和转生印记，中央 50% 干净低纹理，低对比，无清晰文字、无假 UI。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成通用魔幻 RPG；要保留纯数值成长和装备爆装
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 无限升级
aliases: []
category: 放置 RPG / 数值养成
visual_identity: 传统数值放置 RPG 爆装成长
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [idle-rpg, progression, loot]
misclassification_risks: 误判成通用魔幻 RPG；要保留纯数值成长和装备爆装
maker_feasibility_target: "4-5"
tags: [idle-rpg, progression, loot, equipment]
```

## 36. 重返未来：1999

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/221062
- **game_type**: 策略 RPG / 神秘学 / 复古
- **core_gameplay**: 时间逆流、神秘学家、20 世纪文化切片与卡牌战斗
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 英伦复古神秘学时间旅行 RPG
- **genre_presentation**: 把策略 RPG 视觉化为旧报纸、胶片、唱片、雨夜、档案与超现实神秘符号。
- **primary_mood**: 怀旧、神秘、优雅、忧郁
- **world_semantics**: 1999、暴雨、旧报纸、神秘学、唱片、胶片、手提箱、时钟
- **common_ui_material_language**: 旧纸、打字稿、皮革箱、黄铜、胶片、磨砂玻璃
- **shape_language**: 复古矩形、邮票齿边、档案夹、黄铜圆角
- **palette_tendency**: 旧纸黄/褐色作面板；墨黑作文字；酒红作重点；黄铜金作高级；冷绿/蓝作神秘
- **accent_semantics**: 邮票、胶片、唱片、时钟、雨滴、打字机字条
- **background_language**: 雨夜窗边/旧档案室远景，中心纸面清爽
- **misclassification_risks**: 误判成普通蒸汽朋克或欧式宫廷；需保留 20 世纪现代复古与神秘学

### 3. Auto Game Style Brief
- **style_keywords**: 英伦复古神秘学时间旅行 RPG
- **mood**: 怀旧、神秘、优雅、忧郁
- **world_semantics**: 1999、暴雨、旧报纸、神秘学、唱片、胶片、手提箱、时钟
- **material_language**: 旧纸、打字稿、皮革箱、黄铜、胶片、磨砂玻璃
- **shape_language**: 复古矩形、邮票齿边、档案夹、黄铜圆角
- **palette_intent**: 旧纸黄/褐色作面板；墨黑作文字；酒红作重点；黄铜金作高级；冷绿/蓝作神秘
- **state_language**: selected 用酒红邮戳或黄铜框；warning 用暗红异常标
- **accent_semantics**: 邮票、胶片、唱片、时钟、雨滴、打字机字条
- **background_language**: 雨夜窗边/旧档案室远景，中心纸面清爽
- **forbidden_directions**: 误判成普通蒸汽朋克或欧式宫廷；需保留 20 世纪现代复古与神秘学
- **maker_safe_assets**: Maker 目标 4：纸纹、邮票边、胶片贴图

### 4. UI Translation Recommendations
- **panel_design**: 旧纸档案卡+黄铜细边，大卡可加胶片/邮票
- **state_design**: selected 用酒红邮戳或黄铜框；warning 用暗红异常标
- **text_design**: 标题复古 serif，正文黑色打字稿清晰
- **accent_design**: 邮票、胶片、唱片、时钟、雨滴、打字机字条。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 雨夜窗边/旧档案室远景，中心纸面清爽。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 4：纸纹、邮票边、胶片贴图

### 5. Tool Background Prompt
> 生成英伦复古神秘学工具背景，旧纸黄、褐色和雨夜蓝灰基调，边缘有报纸、胶片、唱片、黄铜时钟、手提箱和雨滴，中央 50% 干净低纹理，无清晰文字、无假 UI。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成普通蒸汽朋克或欧式宫廷；需保留 20 世纪现代复古与神秘学
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 重返未来：1999
aliases: []
category: 策略 RPG / 神秘学 / 复古
visual_identity: 英伦复古神秘学时间旅行 RPG
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [retro, occult, 1999]
misclassification_risks: 误判成普通蒸汽朋克或欧式宫廷；需保留 20 世纪现代复古与神秘学
maker_feasibility_target: "4-5"
tags: [retro, occult, 1999, strategy-rpg]
```

## 37. 瞬搭

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/712212
- **game_type**: 时尚换装 / 社交 / 生活
- **core_gameplay**: 自由搭配、捏脸、社区发帖、穿搭博主与多风格服饰收集
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 全球潮流时尚社交换装
- **genre_presentation**: 把换装视觉化为手机社媒、杂志版式、穿搭卡、抽奖礼盒和多元审美。
- **primary_mood**: 潮流、自我表达、精致、社交
- **world_semantics**: SU市、穿搭博主、衣橱、社区帖子、搭配挑战、抽奖券、时尚杂志
- **common_ui_material_language**: 白色手机卡、磨砂玻璃、杂志纸、亮面贴纸、金属小扣
- **shape_language**: 现代圆角、瀑布流卡片、标签化、轻薄层叠
- **palette_tendency**: 白/浅灰作平台底；黑色作时尚对比；粉紫/湖蓝作活动；金色作稀有；红色仅作限时提示
- **accent_semantics**: 衣架、相机、点赞、标签、抽奖券、闪光、杂志贴纸
- **background_language**: 柔焦城市/衣橱/社交 feed 边缘，中心干净
- **misclassification_risks**: 误判成传统少女粉或单一换装；需保留潮流社交和多元审美

### 3. Auto Game Style Brief
- **style_keywords**: 全球潮流时尚社交换装
- **mood**: 潮流、自我表达、精致、社交
- **world_semantics**: SU市、穿搭博主、衣橱、社区帖子、搭配挑战、抽奖券、时尚杂志
- **material_language**: 白色手机卡、磨砂玻璃、杂志纸、亮面贴纸、金属小扣
- **shape_language**: 现代圆角、瀑布流卡片、标签化、轻薄层叠
- **palette_intent**: 白/浅灰作平台底；黑色作时尚对比；粉紫/湖蓝作活动；金色作稀有；红色仅作限时提示
- **state_language**: selected 用黑白高对比或金色细边；warning 用红色限时角标
- **accent_semantics**: 衣架、相机、点赞、标签、抽奖券、闪光、杂志贴纸
- **background_language**: 柔焦城市/衣橱/社交 feed 边缘，中心干净
- **forbidden_directions**: 误判成传统少女粉或单一换装；需保留潮流社交和多元审美
- **maker_safe_assets**: Maker 目标 5：圆角卡、标签、相机/衣架 icon、简单滑入

### 4. UI Translation Recommendations
- **panel_design**: 手机 feed 风圆角卡+时尚标签，小卡像穿搭帖子
- **state_design**: selected 用黑白高对比或金色细边；warning 用红色限时角标
- **text_design**: 标题现代时尚，正文清爽无衬线
- **accent_design**: 衣架、相机、点赞、标签、抽奖券、闪光、杂志贴纸。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 柔焦城市/衣橱/社交 feed 边缘，中心干净。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 5：圆角卡、标签、相机/衣架 icon、简单滑入

### 5. Tool Background Prompt
> 生成全球潮流时尚社交工具背景，白灰与淡粉紫基调，边缘有衣橱、手机帖子、相机、衣架、时尚杂志贴纸和闪光，中央 55% 干净低纹理，无清晰文字、无假 UI、无人物主视觉。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成传统少女粉或单一换装；需保留潮流社交和多元审美
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 瞬搭
aliases: []
category: 时尚换装 / 社交 / 生活
visual_identity: 全球潮流时尚社交换装
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [fashion, social, dress-up]
misclassification_risks: 误判成传统少女粉或单一换装；需保留潮流社交和多元审美
maker_feasibility_target: "4-5"
tags: [fashion, social, dress-up, modern]
```

## 38. 梦幻消除战

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/747820
- **game_type**: 合成 / 模拟经营 / 古风茶楼
- **core_gameplay**: 合成茶点、茶楼经营、家具装修、商海与情缘叙事
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 国风茶点合成茶楼经营
- **genre_presentation**: 把合成经营视觉化为中式茶点、华庭茶楼、糕点盒、木格柜和烟火人间。
- **primary_mood**: 温润、甜美、市井、经营感
- **world_semantics**: 茶楼、芙蓉糕、玉兔点心、茶叶、糕点盒、家具、自宅、商铺
- **common_ui_material_language**: 宣纸菜单、木质柜台、瓷盘、糕点盒、绸布、铜钱
- **shape_language**: 圆润木格、糕点盒格子、卷草角花、柔和卡牌
- **palette_tendency**: 米黄/茶白作面板；木棕作边框；茶绿作辅助；桃粉/糕点色作奖励；朱红作印章/限时
- **accent_semantics**: 茶盏、点心、木格、铜钱、灯笼、菜单牌、花窗
- **background_language**: 茶楼室内/庭院边缘，中央浅纸面留白
- **misclassification_risks**: 误判成普通三消糖果或宫廷经营；需保留茶点文化和茶楼装修

### 3. Auto Game Style Brief
- **style_keywords**: 国风茶点合成茶楼经营
- **mood**: 温润、甜美、市井、经营感
- **world_semantics**: 茶楼、芙蓉糕、玉兔点心、茶叶、糕点盒、家具、自宅、商铺
- **material_language**: 宣纸菜单、木质柜台、瓷盘、糕点盒、绸布、铜钱
- **shape_language**: 圆润木格、糕点盒格子、卷草角花、柔和卡牌
- **palette_intent**: 米黄/茶白作面板；木棕作边框；茶绿作辅助；桃粉/糕点色作奖励；朱红作印章/限时
- **state_language**: selected 用茶绿/金色细边；warning 用朱红限时牌
- **accent_semantics**: 茶盏、点心、木格、铜钱、灯笼、菜单牌、花窗
- **background_language**: 茶楼室内/庭院边缘，中央浅纸面留白
- **forbidden_directions**: 误判成普通三消糖果或宫廷经营；需保留茶点文化和茶楼装修
- **maker_safe_assets**: Maker 目标 5：木格九宫格、点心 icon、纸纹

### 4. UI Translation Recommendations
- **panel_design**: 菜单式纸卡+木格边，大卡可加瓷盘/糕点盒
- **state_design**: selected 用茶绿/金色细边；warning 用朱红限时牌
- **text_design**: 标题国风温润，正文深棕清晰
- **accent_design**: 茶盏、点心、木格、铜钱、灯笼、菜单牌、花窗。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 茶楼室内/庭院边缘，中央浅纸面留白。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 5：木格九宫格、点心 icon、纸纹

### 5. Tool Background Prompt
> 生成国风茶点合成茶楼工具背景，米黄茶白与浅木棕基调，边缘有茶楼窗格、瓷盘、糕点盒、茶盏、灯笼和花窗，中央 50% 干净低纹理，无清晰文字、无假 UI。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成普通三消糖果或宫廷经营；需保留茶点文化和茶楼装修
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 梦幻消除战
aliases: []
category: 合成 / 模拟经营 / 古风茶楼
visual_identity: 国风茶点合成茶楼经营
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [merge, teahouse, chinese]
misclassification_risks: 误判成普通三消糖果或宫廷经营；需保留茶点文化和茶楼装修
maker_feasibility_target: "4-5"
tags: [merge, teahouse, chinese, cozy]
```

## 39. 一念逍遥

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/159465
- **game_type**: 修仙放置 / 水墨 RPG
- **core_gameplay**: 放置修炼、炼丹炼器、飞升、宗门和仙魔抉择
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 水墨国风放置修仙
- **genre_presentation**: 把放置修仙视觉化为云海、洞府、丹炉、灵气、仙鹤和境界突破。
- **primary_mood**: 飘逸、悠远、修行、清静
- **world_semantics**: 洞府、丹炉、飞升、宗门、灵兽、云海、法宝、境界
- **common_ui_material_language**: 宣纸、水墨、玉石、青铜丹炉、淡金云纹
- **shape_language**: 卷轴、云纹圆角、法阵圆环、印章
- **palette_tendency**: 米白/淡墨作面板；青绿作灵气；淡金作仙缘；朱砂作印章；暗紫/红用于魔修/劫难
- **accent_semantics**: 仙鹤、丹炉、符箓、法宝、云纹、玉佩
- **background_language**: 水墨云海山峦远景，中央宣纸留白
- **misclassification_risks**: 误判成冷蓝仙侠或硬核武侠；应是放置修行的淡雅水墨

### 3. Auto Game Style Brief
- **style_keywords**: 水墨国风放置修仙
- **mood**: 飘逸、悠远、修行、清静
- **world_semantics**: 洞府、丹炉、飞升、宗门、灵兽、云海、法宝、境界
- **material_language**: 宣纸、水墨、玉石、青铜丹炉、淡金云纹
- **shape_language**: 卷轴、云纹圆角、法阵圆环、印章
- **palette_intent**: 米白/淡墨作面板；青绿作灵气；淡金作仙缘；朱砂作印章；暗紫/红用于魔修/劫难
- **state_language**: selected 用淡金/青绿灵气；warning 用暗红天劫符
- **accent_semantics**: 仙鹤、丹炉、符箓、法宝、云纹、玉佩
- **background_language**: 水墨云海山峦远景，中央宣纸留白
- **forbidden_directions**: 误判成冷蓝仙侠或硬核武侠；应是放置修行的淡雅水墨
- **maker_safe_assets**: Maker 目标 4：纸纹、云纹、法阵 SVG、少量静态雾

### 4. UI Translation Recommendations
- **panel_design**: 宣纸卡+淡墨边+云纹角，大卡可加法阵淡纹
- **state_design**: selected 用淡金/青绿灵气；warning 用暗红天劫符
- **text_design**: 标题书法感，正文深墨清楚
- **accent_design**: 仙鹤、丹炉、符箓、法宝、云纹、玉佩。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 水墨云海山峦远景，中央宣纸留白。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 4：纸纹、云纹、法阵 SVG、少量静态雾

### 5. Tool Background Prompt
> 生成水墨国风放置修仙工具背景，米白宣纸和淡青墨云海，边缘有仙鹤、丹炉、法宝、云纹和淡金法阵，中央 50% 干净低纹理，无清晰文字、无假 UI、无角色。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成冷蓝仙侠或硬核武侠；应是放置修行的淡雅水墨
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 一念逍遥
aliases: []
category: 修仙放置 / 水墨 RPG
visual_identity: 水墨国风放置修仙
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [xianxia, idle, ink]
misclassification_risks: 误判成冷蓝仙侠或硬核武侠；应是放置修行的淡雅水墨
maker_feasibility_target: "4-5"
tags: [xianxia, idle, ink, cultivation]
```

## 40. 恋与深空

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/201633
- **game_type**: 女性向 / 3D 恋爱 / 科幻
- **core_gameplay**: 近未来恋爱、战斗、陪伴、深空设定和高沉浸角色互动
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 近未来深空浪漫恋爱科幻
- **genre_presentation**: 把恋爱互动视觉化为深空、星舰感、柔光玻璃、心率数据和亲密通信界面。
- **primary_mood**: 浪漫、沉浸、神秘、精致
- **world_semantics**: 深空、星轨、通讯、心率、约会、战斗搭档、记忆碎片、光粒
- **common_ui_material_language**: 柔光玻璃、星空金属、丝绸渐变、半透明通信卡
- **shape_language**: 圆角薄卡、光带、星轨弧线、轻奢细边
- **palette_tendency**: 深蓝/银白作深空底；粉紫作浪漫；冰蓝作科技；金色作珍贵；红色只作心率/警告
- **accent_semantics**: 星轨、心跳线、通讯气泡、花、记忆碎片、光点
- **background_language**: 深空/城市夜景柔焦远景，中心纯净低纹理
- **misclassification_risks**: 误判成通用粉色乙女或硬科幻；需保留浪漫与深空并重

### 3. Auto Game Style Brief
- **style_keywords**: 近未来深空浪漫恋爱科幻
- **mood**: 浪漫、沉浸、神秘、精致
- **world_semantics**: 深空、星轨、通讯、心率、约会、战斗搭档、记忆碎片、光粒
- **material_language**: 柔光玻璃、星空金属、丝绸渐变、半透明通信卡
- **shape_language**: 圆角薄卡、光带、星轨弧线、轻奢细边
- **palette_intent**: 深蓝/银白作深空底；粉紫作浪漫；冰蓝作科技；金色作珍贵；红色只作心率/警告
- **state_language**: selected 用粉紫/金色柔光；warning 用红色心率警示
- **accent_semantics**: 星轨、心跳线、通讯气泡、花、记忆碎片、光点
- **background_language**: 深空/城市夜景柔焦远景，中心纯净低纹理
- **forbidden_directions**: 误判成通用粉色乙女或硬科幻；需保留浪漫与深空并重
- **maker_safe_assets**: Maker 目标 4：玻璃卡、星轨 SVG、柔光遮罩

### 4. UI Translation Recommendations
- **panel_design**: 半透明柔光卡+细边，背景粒子必须少
- **state_design**: selected 用粉紫/金色柔光；warning 用红色心率警示
- **text_design**: 标题优雅现代，正文白/深灰清晰
- **accent_design**: 星轨、心跳线、通讯气泡、花、记忆碎片、光点。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 深空/城市夜景柔焦远景，中心纯净低纹理。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 4：玻璃卡、星轨 SVG、柔光遮罩

### 5. Tool Background Prompt
> 生成近未来深空浪漫工具背景，深蓝银白与淡粉紫基调，边缘有星轨、通讯光带、心率线、记忆碎片和柔焦城市夜景，中央 55% 干净低纹理，无清晰文字、无假 UI、无人物主视觉。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成通用粉色乙女或硬科幻；需保留浪漫与深空并重
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 恋与深空
aliases: []
category: 女性向 / 3D 恋爱 / 科幻
visual_identity: 近未来深空浪漫恋爱科幻
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [romance, sci-fi, deep-space]
misclassification_risks: 误判成通用粉色乙女或硬科幻；需保留浪漫与深空并重
maker_feasibility_target: "4-5"
tags: [romance, sci-fi, deep-space, otome]
```

## 41. 出发吧麦芬

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/222034
- **game_type**: 放置 RPG / 治愈冒险
- **core_gameplay**: 房车旅行、双人同行、放置成长、轻松社交与幻想冒险
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 治愈房车异世界放置冒险
- **genre_presentation**: 把放置 RPG 视觉化为房车旅途、伙伴同行、日式西幻、柔软云朵和轻松战斗。
- **primary_mood**: 治愈、轻松、友爱、旅行
- **world_semantics**: 房车、麦芬、营地、伙伴、云朵、地图、技能、冒险行囊
- **common_ui_material_language**: 浅木、帆布、旅行手账、圆角纸卡、软糖色徽章
- **shape_language**: 圆润、手账标签、地图虚线、软木边框
- **palette_tendency**: 暖白/奶油黄作底；草绿/天蓝作旅途；木棕作结构；金色作奖励；橙色作技能提示
- **accent_semantics**: 房车、背包、地图针、云朵、篝火、面包/麦芬
- **background_language**: 晴朗旅途/营地远景，中央云白留白
- **misclassification_risks**: 误判成硬核异世界或低龄宠物；需保留治愈房车旅行

### 3. Auto Game Style Brief
- **style_keywords**: 治愈房车异世界放置冒险
- **mood**: 治愈、轻松、友爱、旅行
- **world_semantics**: 房车、麦芬、营地、伙伴、云朵、地图、技能、冒险行囊
- **material_language**: 浅木、帆布、旅行手账、圆角纸卡、软糖色徽章
- **shape_language**: 圆润、手账标签、地图虚线、软木边框
- **palette_intent**: 暖白/奶油黄作底；草绿/天蓝作旅途；木棕作结构；金色作奖励；橙色作技能提示
- **state_language**: selected 用金色地图针/云朵边；warning 用橙色提示牌
- **accent_semantics**: 房车、背包、地图针、云朵、篝火、面包/麦芬
- **background_language**: 晴朗旅途/营地远景，中央云白留白
- **forbidden_directions**: 误判成硬核异世界或低龄宠物；需保留治愈房车旅行
- **maker_safe_assets**: Maker 目标 5：纸卡、云朵、地图线、房车 icon

### 4. UI Translation Recommendations
- **panel_design**: 手账纸卡+浅木边，大卡可加地图虚线
- **state_design**: selected 用金色地图针/云朵边；warning 用橙色提示牌
- **text_design**: 标题圆润冒险感，正文深棕清晰
- **accent_design**: 房车、背包、地图针、云朵、篝火、面包/麦芬。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 晴朗旅途/营地远景，中央云白留白。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 5：纸卡、云朵、地图线、房车 icon

### 5. Tool Background Prompt
> 生成治愈房车异世界放置冒险工具背景，暖白奶油黄与浅天空蓝基调，边缘有房车、营地、云朵、地图针、背包和小麦芬图标，中央 50% 干净低纹理，无清晰文字、无假 UI。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成硬核异世界或低龄宠物；需保留治愈房车旅行
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 出发吧麦芬
aliases: []
category: 放置 RPG / 治愈冒险
visual_identity: 治愈房车异世界放置冒险
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [idle-rpg, cozy, travel]
misclassification_risks: 误判成硬核异世界或低龄宠物；需保留治愈房车旅行
maker_feasibility_target: "4-5"
tags: [idle-rpg, cozy, travel, muffin]
```

## 42. 金铲铲之战

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/176937
- **game_type**: 自走棋 / 策略 / 英雄
- **core_gameplay**: 棋盘布阵、羁绊、装备合成、小小英雄和赛季主题
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 华丽棋盘自走棋策略竞技
- **genre_presentation**: 把自走棋视觉化为战术棋盘、装备合成、羁绊徽章、金铲铲和小小英雄收藏。
- **primary_mood**: 策略、竞技、收集、轻幻想
- **world_semantics**: 棋盘、金铲铲、装备、羁绊、商店、金币、小小英雄、传送门
- **common_ui_material_language**: 深色棋盘石板、金属边、宝石徽章、商店卡
- **shape_language**: 棋格、徽章、金边、装备槽、六边形/方格
- **palette_tendency**: 深蓝/紫作棋盘底；金色作金币和选中；宝石色作羁绊；绿色作经济；红色只作失败/敌方
- **accent_semantics**: 金铲铲、金币、装备、小小英雄脚印、羁绊徽章
- **background_language**: 棋盘/竞技场远景，边缘装备和金币，中心安全区低纹理
- **misclassification_risks**: 误判成普通 MOBA 或卡牌；核心是棋盘布阵和经济策略

### 3. Auto Game Style Brief
- **style_keywords**: 华丽棋盘自走棋策略竞技
- **mood**: 策略、竞技、收集、轻幻想
- **world_semantics**: 棋盘、金铲铲、装备、羁绊、商店、金币、小小英雄、传送门
- **material_language**: 深色棋盘石板、金属边、宝石徽章、商店卡
- **shape_language**: 棋格、徽章、金边、装备槽、六边形/方格
- **palette_intent**: 深蓝/紫作棋盘底；金色作金币和选中；宝石色作羁绊；绿色作经济；红色只作失败/敌方
- **state_language**: selected 用金色棋格框；warning 用红色连败/敌方标
- **accent_semantics**: 金铲铲、金币、装备、小小英雄脚印、羁绊徽章
- **background_language**: 棋盘/竞技场远景，边缘装备和金币，中心安全区低纹理
- **forbidden_directions**: 误判成普通 MOBA 或卡牌；核心是棋盘布阵和经济策略
- **maker_safe_assets**: Maker 目标 4：棋格贴图、金边、徽章 icon

### 4. UI Translation Recommendations
- **panel_design**: 棋盘纹理卡+金边，大卡可加羁绊徽章
- **state_design**: selected 用金色棋格框；warning 用红色连败/敌方标
- **text_design**: 标题竞技华丽，正文白/金高对比
- **accent_design**: 金铲铲、金币、装备、小小英雄脚印、羁绊徽章。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 棋盘/竞技场远景，边缘装备和金币，中心安全区低纹理。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 4：棋格贴图、金边、徽章 icon

### 5. Tool Background Prompt
> 生成华丽自走棋策略工具背景，深蓝紫棋盘与暗金基调，边缘有金铲铲、金币、装备槽、羁绊徽章和竞技场远景，中央 50% 干净低纹理，无清晰文字、无假 UI。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成普通 MOBA 或卡牌；核心是棋盘布阵和经济策略
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 金铲铲之战
aliases: []
category: 自走棋 / 策略 / 英雄
visual_identity: 华丽棋盘自走棋策略竞技
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [autobattler, strategy, board]
misclassification_risks: 误判成普通 MOBA 或卡牌；核心是棋盘布阵和经济策略
maker_feasibility_target: "4-5"
tags: [autobattler, strategy, board, competitive]
```

## 43. 光·遇

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/62448
- **game_type**: 社交冒险 / 探索
- **core_gameplay**: 飞行、烛火、牵手社交、云中王国探索
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 诗意云海光旅社交冒险
- **genre_presentation**: 把社交冒险视觉化为光、风、云海、斗篷、烛火和极简精神性空间。
- **primary_mood**: 宁静、温柔、诗意、治愈
- **world_semantics**: 云海、烛火、光翼、斗篷、牵手、神庙、风、星光
- **common_ui_material_language**: 柔光玻璃、雾面纸、云层渐变、金色光尘
- **shape_language**: 大留白、圆角、轻薄卡、柔和弧线
- **palette_tendency**: 暖白/云灰作底；金色作光和奖励；天蓝/霞粉作空间；深蓝作夜；红色极少使用
- **accent_semantics**: 烛火、光翼、星星、云朵、斗篷剪影、风线
- **background_language**: 云海/霞光远景，中央空灵留白，避免强光中心
- **misclassification_risks**: 误判成普通天空治愈或儿童绘本；需保留社交与光的仪式感

### 3. Auto Game Style Brief
- **style_keywords**: 诗意云海光旅社交冒险
- **mood**: 宁静、温柔、诗意、治愈
- **world_semantics**: 云海、烛火、光翼、斗篷、牵手、神庙、风、星光
- **material_language**: 柔光玻璃、雾面纸、云层渐变、金色光尘
- **shape_language**: 大留白、圆角、轻薄卡、柔和弧线
- **palette_intent**: 暖白/云灰作底；金色作光和奖励；天蓝/霞粉作空间；深蓝作夜；红色极少使用
- **state_language**: selected 用金色烛光环；warning 几乎不用红，必要时用柔橙
- **accent_semantics**: 烛火、光翼、星星、云朵、斗篷剪影、风线
- **background_language**: 云海/霞光远景，中央空灵留白，避免强光中心
- **forbidden_directions**: 误判成普通天空治愈或儿童绘本；需保留社交与光的仪式感
- **maker_safe_assets**: Maker 目标 4：渐变、光点、云朵遮罩，避免粒子过多

### 4. UI Translation Recommendations
- **panel_design**: 极简半透明卡+柔光边，装饰极少
- **state_design**: selected 用金色烛光环；warning 几乎不用红，必要时用柔橙
- **text_design**: 标题轻盈，正文高对比但不锐利
- **accent_design**: 烛火、光翼、星星、云朵、斗篷剪影、风线。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 云海/霞光远景，中央空灵留白，避免强光中心。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 4：渐变、光点、云朵遮罩，避免粒子过多

### 5. Tool Background Prompt
> 生成诗意云海光旅工具背景，暖白云灰与淡金霞光基调，边缘有柔和云层、烛火、星光、风线和光翼剪影，中央 55% 极简低纹理安全区，无清晰文字、无假 UI、无角色。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成普通天空治愈或儿童绘本；需保留社交与光的仪式感
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 光·遇
aliases: []
category: 社交冒险 / 探索
visual_identity: 诗意云海光旅社交冒险
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [poetic, social, cloud]
misclassification_risks: 误判成普通天空治愈或儿童绘本；需保留社交与光的仪式感
maker_feasibility_target: "4-5"
tags: [poetic, social, cloud, light]
```

## 44. 奥比岛：梦想国度

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/88544
- **game_type**: 社交模拟 / 岛屿生活
- **core_gameplay**: 小岛生活、家园装扮、社交、宠物和童话活动
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 童话玩偶岛屿社交模拟
- **genre_presentation**: 把岛屿生活视觉化为可爱小屋、童话森林、玩偶质感、梦幻活动和强社交装扮。
- **primary_mood**: 可爱、梦幻、童年、热闹
- **world_semantics**: 奥比小岛、小屋、家具、精灵、气球、花园、宠物、派对
- **common_ui_material_language**: 棉花糖色塑料、木牌、布艺、彩纸、亮面贴纸
- **shape_language**: 圆润、花边、玩偶厚块、云朵边、糖果按钮
- **palette_tendency**: 粉蓝/奶黄作底；草绿作岛屿；紫粉作梦幻；金色作奖励；红色仅限警示
- **accent_semantics**: 气球、花朵、云朵、蝴蝶结、小屋、星星、宠物脚印
- **background_language**: 童话岛屿/花园边缘，中心浅色安全区
- **misclassification_risks**: 误判成低龄儿童 UI；需做成童话社交而非幼教

### 3. Auto Game Style Brief
- **style_keywords**: 童话玩偶岛屿社交模拟
- **mood**: 可爱、梦幻、童年、热闹
- **world_semantics**: 奥比小岛、小屋、家具、精灵、气球、花园、宠物、派对
- **material_language**: 棉花糖色塑料、木牌、布艺、彩纸、亮面贴纸
- **shape_language**: 圆润、花边、玩偶厚块、云朵边、糖果按钮
- **palette_intent**: 粉蓝/奶黄作底；草绿作岛屿；紫粉作梦幻；金色作奖励；红色仅限警示
- **state_language**: selected 用金色星星/粉蓝描边；warning 用小红感叹
- **accent_semantics**: 气球、花朵、云朵、蝴蝶结、小屋、星星、宠物脚印
- **background_language**: 童话岛屿/花园边缘，中心浅色安全区
- **forbidden_directions**: 误判成低龄儿童 UI；需做成童话社交而非幼教
- **maker_safe_assets**: Maker 目标 5：圆角卡、花朵/气球 icon、简单弹跳

### 4. UI Translation Recommendations
- **panel_design**: 软糖色圆角卡+花边，小卡保持干净
- **state_design**: selected 用金色星星/粉蓝描边；warning 用小红感叹
- **text_design**: 标题圆润梦幻，正文深色高可读
- **accent_design**: 气球、花朵、云朵、蝴蝶结、小屋、星星、宠物脚印。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 童话岛屿/花园边缘，中心浅色安全区。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 5：圆角卡、花朵/气球 icon、简单弹跳

### 5. Tool Background Prompt
> 生成童话玩偶岛屿社交工具背景，粉蓝奶黄和浅草绿基调，边缘有小屋、花园、气球、云朵、蝴蝶结和星星贴纸，中央 50% 干净低纹理，无清晰文字、无假 UI、无角色。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成低龄儿童 UI；需做成童话社交而非幼教
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 奥比岛：梦想国度
aliases: []
category: 社交模拟 / 岛屿生活
visual_identity: 童话玩偶岛屿社交模拟
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [cute, island, social-sim]
misclassification_risks: 误判成低龄儿童 UI；需做成童话社交而非幼教
maker_feasibility_target: "4-5"
tags: [cute, island, social-sim, fairy-tale]
```

## 45. 苍翼：混沌效应

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/233514
- **game_type**: 动作 Roguelite / 科幻动漫
- **core_gameplay**: 高速动作、角色流派、意识空间、连招与 Roguelite 构筑
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 电蓝赛博动漫动作 Roguelite
- **genre_presentation**: 把动作 Roguelite 视觉化为高对比电光、代码故障、硬边 UI、角色数据和高速连击反馈。
- **primary_mood**: 凌厉、炫酷、高速、压迫
- **world_semantics**: 意识空间、代码、连击、技能芯片、机甲感、蓝色电弧、数据故障
- **common_ui_material_language**: 暗色玻璃、金属切片、电蓝能量、故障屏幕
- **shape_language**: 锐角、斜切、碎片化、扫描线、能量条
- **palette_tendency**: 黑/深蓝作底；电蓝作核心能量；紫色作混沌；白色作高亮；红色只作受击/危险
- **accent_semantics**: 电弧、芯片、故障块、连击数字、技能晶片
- **background_language**: 深色数据空间远景，边缘电蓝碎片，中心可读
- **misclassification_risks**: 误判成普通赛博霓虹；需要格斗动漫速度和 Roguelite 芯片

### 3. Auto Game Style Brief
- **style_keywords**: 电蓝赛博动漫动作 Roguelite
- **mood**: 凌厉、炫酷、高速、压迫
- **world_semantics**: 意识空间、代码、连击、技能芯片、机甲感、蓝色电弧、数据故障
- **material_language**: 暗色玻璃、金属切片、电蓝能量、故障屏幕
- **shape_language**: 锐角、斜切、碎片化、扫描线、能量条
- **palette_intent**: 黑/深蓝作底；电蓝作核心能量；紫色作混沌；白色作高亮；红色只作受击/危险
- **state_language**: selected 用电蓝能量边；warning 用红色故障警示
- **accent_semantics**: 电弧、芯片、故障块、连击数字、技能晶片
- **background_language**: 深色数据空间远景，边缘电蓝碎片，中心可读
- **forbidden_directions**: 误判成普通赛博霓虹；需要格斗动漫速度和 Roguelite 芯片
- **maker_safe_assets**: Maker 目标 4：切角卡、扫描线、电弧贴图、少量抖动

### 4. UI Translation Recommendations
- **panel_design**: 深色切角卡+电蓝边，特效控制在边缘
- **state_design**: selected 用电蓝能量边；warning 用红色故障警示
- **text_design**: 标题锋利科技感，正文白灰清晰
- **accent_design**: 电弧、芯片、故障块、连击数字、技能晶片。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 深色数据空间远景，边缘电蓝碎片，中心可读。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 4：切角卡、扫描线、电弧贴图、少量抖动

### 5. Tool Background Prompt
> 生成电蓝赛博动漫动作工具背景，黑深蓝数据空间，边缘有电蓝电弧、芯片、故障块、斜切碎片和连击数字抽象元素，中央 50% 干净低纹理，低对比，无清晰文字、无假 UI、无角色。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成普通赛博霓虹；需要格斗动漫速度和 Roguelite 芯片
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 苍翼：混沌效应
aliases: []
category: 动作 Roguelite / 科幻动漫
visual_identity: 电蓝赛博动漫动作 Roguelite
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [cyber, action, roguelite]
misclassification_risks: 误判成普通赛博霓虹；需要格斗动漫速度和 Roguelite 芯片
maker_feasibility_target: "4-5"
tags: [cyber, action, roguelite, anime]
```

## 46. 泰拉瑞亚

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/194610
- **game_type**: 像素沙盒 / 冒险 / 生存
- **core_gameplay**: 横版挖掘、建造、探索、Boss 战和装备收集
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 复古像素横版沙盒冒险
- **genre_presentation**: 把沙盒冒险视觉化为像素地层、物品栏、矿洞、工作台和昼夜地表探索。
- **primary_mood**: 探索、自由、复古、惊喜
- **world_semantics**: 泥土层、矿石、洞穴、火把、木屋、工作台、史莱姆、Boss 战利品
- **common_ui_material_language**: 像素木板、石块、泥土、物品栏槽、复古蓝窗
- **shape_language**: 像素直角、格子、块状边框、物品槽
- **palette_tendency**: 泥棕/草绿作自然；深蓝作夜和洞穴；木棕作面板；金/紫作稀有；红色作危险
- **accent_semantics**: 火把、矿石、镐子、史莱姆、物品槽、星星
- **background_language**: 像素地层/木屋/洞穴边缘，中心清晰块状安全区
- **misclassification_risks**: 误判成我的世界体素；它是横版像素冒险和地层挖掘

### 3. Auto Game Style Brief
- **style_keywords**: 复古像素横版沙盒冒险
- **mood**: 探索、自由、复古、惊喜
- **world_semantics**: 泥土层、矿石、洞穴、火把、木屋、工作台、史莱姆、Boss 战利品
- **material_language**: 像素木板、石块、泥土、物品栏槽、复古蓝窗
- **shape_language**: 像素直角、格子、块状边框、物品槽
- **palette_intent**: 泥棕/草绿作自然；深蓝作夜和洞穴；木棕作面板；金/紫作稀有；红色作危险
- **state_language**: selected 用金色像素框；warning 用红色 Boss/伤害
- **accent_semantics**: 火把、矿石、镐子、史莱姆、物品槽、星星
- **background_language**: 像素地层/木屋/洞穴边缘，中心清晰块状安全区
- **forbidden_directions**: 误判成我的世界体素；它是横版像素冒险和地层挖掘
- **maker_safe_assets**: Maker 目标 5：像素贴图、网格、物品 icon

### 4. UI Translation Recommendations
- **panel_design**: 像素木板/石砖面板，小卡像物品槽
- **state_design**: selected 用金色像素框；warning 用红色 Boss/伤害
- **text_design**: 标题像素体，正文若小需改用清晰字体
- **accent_design**: 火把、矿石、镐子、史莱姆、物品槽、星星。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 像素地层/木屋/洞穴边缘，中心清晰块状安全区。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 5：像素贴图、网格、物品 icon

### 5. Tool Background Prompt
> 生成复古像素横版沙盒工具背景，泥土层、草地和洞穴像素远景，边缘有火把、矿石、木屋、镐子和物品槽，中央 50% 干净低纹理块面，无清晰文字、无假 UI。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成我的世界体素；它是横版像素冒险和地层挖掘
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 泰拉瑞亚
aliases: []
category: 像素沙盒 / 冒险 / 生存
visual_identity: 复古像素横版沙盒冒险
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [pixel, sandbox, side-scroller]
misclassification_risks: 误判成我的世界体素；它是横版像素冒险和地层挖掘
maker_feasibility_target: "4-5"
tags: [pixel, sandbox, side-scroller, adventure]
```

## 47. 凹凸世界：彩虹收藏家

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/749006
- **game_type**: 三消 RPG / IP 收藏 / 赛博吃谷
- **core_gameplay**: 三消冒险、参赛者信息与周边收藏、盲盒和 DIY 收藏板
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 赛博吃谷三消收藏
- **genre_presentation**: 把三消和 IP 收藏视觉化为虚拟谷子展柜、盲盒、彩虹膜工艺、元力战斗和几何 IP 视觉。
- **primary_mood**: 轻快、收藏癖、潮流、热血
- **world_semantics**: 谷子、盲盒、收藏图册、参赛者、元力、彩窗、反光、DIY 展板
- **common_ui_material_language**: 亮面亚克力、彩虹膜、白瓷、银葱、透明展柜、卡牌纸
- **shape_language**: 几何切面、展示格、圆角盲盒、彩虹折射边
- **palette_tendency**: 白/浅灰作展柜底；彩虹膜高光作稀有；黑色/亮色几何作 IP 对比；金色作限定；红色少用
- **accent_semantics**: 盲盒、徽章、亚克力牌、彩虹反光、收藏格、元力符号
- **background_language**: 虚拟收藏展柜边缘，中央留出清爽展示区
- **misclassification_risks**: 误判成普通三消糖果或单纯二次元卡牌；需保留赛博吃谷和收藏工艺

### 3. Auto Game Style Brief
- **style_keywords**: 赛博吃谷三消收藏
- **mood**: 轻快、收藏癖、潮流、热血
- **world_semantics**: 谷子、盲盒、收藏图册、参赛者、元力、彩窗、反光、DIY 展板
- **material_language**: 亮面亚克力、彩虹膜、白瓷、银葱、透明展柜、卡牌纸
- **shape_language**: 几何切面、展示格、圆角盲盒、彩虹折射边
- **palette_intent**: 白/浅灰作展柜底；彩虹膜高光作稀有；黑色/亮色几何作 IP 对比；金色作限定；红色少用
- **state_language**: selected 用彩虹膜高光；warning 用红色库存/限时小角标
- **accent_semantics**: 盲盒、徽章、亚克力牌、彩虹反光、收藏格、元力符号
- **background_language**: 虚拟收藏展柜边缘，中央留出清爽展示区
- **forbidden_directions**: 误判成普通三消糖果或单纯二次元卡牌；需保留赛博吃谷和收藏工艺
- **maker_safe_assets**: Maker 目标 4：展示格、虹彩贴图、盲盒 icon

### 4. UI Translation Recommendations
- **panel_design**: 展柜格卡+虹彩边，小卡像收藏品槽
- **state_design**: selected 用彩虹膜高光；warning 用红色库存/限时小角标
- **text_design**: 标题可潮流几何，正文黑灰清晰
- **accent_design**: 盲盒、徽章、亚克力牌、彩虹反光、收藏格、元力符号。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 虚拟收藏展柜边缘，中央留出清爽展示区。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 4：展示格、虹彩贴图、盲盒 icon

### 5. Tool Background Prompt
> 生成赛博吃谷三消收藏工具背景，白灰展柜与淡彩虹膜高光，边缘有盲盒、亚克力徽章、收藏格、彩窗反光和元力几何符号，中央 50% 干净低纹理，无清晰文字、无假 UI、无角色。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成普通三消糖果或单纯二次元卡牌；需保留赛博吃谷和收藏工艺
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 凹凸世界：彩虹收藏家
aliases: []
category: 三消 RPG / IP 收藏 / 赛博吃谷
visual_identity: 赛博吃谷三消收藏
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [match-3, collection, merch]
misclassification_risks: 误判成普通三消糖果或单纯二次元卡牌；需保留赛博吃谷和收藏工艺
maker_feasibility_target: "4-5"
tags: [match-3, collection, merch, cyber]
```

## 48. 前线模拟战

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/753312
- **game_type**: 现代战争模拟 / 射击
- **core_gameplay**: AI 敌人、多模式、经典武器、真实弹道后坐力和团队战术对抗
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 轻体量现代战争模拟靶场战术
- **genre_presentation**: 把战争模拟视觉化为真实枪械、弹道参数、战术地图、背包仓库和低成本但清晰的军用 HUD。
- **primary_mood**: 紧张、实用、粗粝、战术
- **world_semantics**: 经典武器、弹药、护甲、矿洞撤离点、仓库、流浪商人、AI 敌人
- **common_ui_material_language**: 军绿终端、粗糙金属、橡胶、仓库格、纸质任务单
- **shape_language**: 硬边、网格、装备槽、粗线框、切角
- **palette_tendency**: 军绿/灰黑作底；土黄作任务；白灰作参数；红色作受伤/危险；蓝色少量作系统
- **accent_semantics**: 弹匣、准星、护甲、撤离箭头、仓库锁、矿洞标记
- **background_language**: 低对比仓库/战术地图/靶场边缘，中心清晰
- **misclassification_risks**: 误判成 AAA 战争大片或赛博；应保持轻量模拟和实用工具感

### 3. Auto Game Style Brief
- **style_keywords**: 轻体量现代战争模拟靶场战术
- **mood**: 紧张、实用、粗粝、战术
- **world_semantics**: 经典武器、弹药、护甲、矿洞撤离点、仓库、流浪商人、AI 敌人
- **material_language**: 军绿终端、粗糙金属、橡胶、仓库格、纸质任务单
- **shape_language**: 硬边、网格、装备槽、粗线框、切角
- **palette_intent**: 军绿/灰黑作底；土黄作任务；白灰作参数；红色作受伤/危险；蓝色少量作系统
- **state_language**: selected 用土黄战术边；warning 用红色伤害/撤离倒计时
- **accent_semantics**: 弹匣、准星、护甲、撤离箭头、仓库锁、矿洞标记
- **background_language**: 低对比仓库/战术地图/靶场边缘，中心清晰
- **forbidden_directions**: 误判成 AAA 战争大片或赛博；应保持轻量模拟和实用工具感
- **maker_safe_assets**: Maker 目标 5：网格、装备槽、准星、简单进度条

### 4. UI Translation Recommendations
- **panel_design**: 硬边装备卡+仓库格，大卡可加任务纸
- **state_design**: selected 用土黄战术边；warning 用红色伤害/撤离倒计时
- **text_design**: 标题硬朗，正文和数字清楚
- **accent_design**: 弹匣、准星、护甲、撤离箭头、仓库锁、矿洞标记。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 低对比仓库/战术地图/靶场边缘，中心清晰。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 5：网格、装备槽、准星、简单进度条

### 5. Tool Background Prompt
> 生成轻体量现代战争模拟工具背景，军绿灰黑和土黄低饱和基调，边缘有仓库格、经典武器轮廓、弹匣、护甲、撤离箭头和战术地图线，中央 50% 干净低纹理，无清晰文字、无假 UI。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成 AAA 战争大片或赛博；应保持轻量模拟和实用工具感
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 前线模拟战
aliases: []
category: 现代战争模拟 / 射击
visual_identity: 轻体量现代战争模拟靶场战术
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [war-sim, shooter, tactical]
misclassification_risks: 误判成 AAA 战争大片或赛博；应保持轻量模拟和实用工具感
maker_feasibility_target: "4-5"
tags: [war-sim, shooter, tactical, hud]
```

## 49. 境·界 刀鸣

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/374914
- **game_type**: 动作 / 动漫 IP / 格斗
- **core_gameplay**: BLEACH 正版授权、剧情体验、拼刀对决、卍解、极速攻防和角色连携
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 黑白魂界刀鸣热血动作
- **genre_presentation**: 把动作手游视觉化为斩魄刀、灵压、黑白死神服、墨线斩击和卍解爆发。
- **primary_mood**: 热血、锋利、肃杀、浪漫
- **world_semantics**: 尸魂界、斩魄刀、卍解、灵压、守护、拼刀、黑崎一护式魂力
- **common_ui_material_language**: 黑白纸墨、刀刃金属、灵压光、暗色玻璃、和风纹
- **shape_language**: 锐角斩击、墨刷边、切角卡、速度线
- **palette_tendency**: 黑白作主色；蓝白作灵压；橙色作主角热血点；紫/红作敌方或危险；金色少量作稀有
- **accent_semantics**: 刀痕、灵压火焰、墨线、队章、符纸、斩击弧
- **background_language**: 黑白魂界/夜空远景，边缘斩击线，中心干净
- **misclassification_risks**: 误判成普通和风武士；必须保留 BLEACH 的黑白死神与灵压

### 3. Auto Game Style Brief
- **style_keywords**: 黑白魂界刀鸣热血动作
- **mood**: 热血、锋利、肃杀、浪漫
- **world_semantics**: 尸魂界、斩魄刀、卍解、灵压、守护、拼刀、黑崎一护式魂力
- **material_language**: 黑白纸墨、刀刃金属、灵压光、暗色玻璃、和风纹
- **shape_language**: 锐角斩击、墨刷边、切角卡、速度线
- **palette_intent**: 黑白作主色；蓝白作灵压；橙色作主角热血点；紫/红作敌方或危险；金色少量作稀有
- **state_language**: selected 用蓝白灵压光；warning 用红紫敌意，不作普通强调
- **accent_semantics**: 刀痕、灵压火焰、墨线、队章、符纸、斩击弧
- **background_language**: 黑白魂界/夜空远景，边缘斩击线，中心干净
- **forbidden_directions**: 误判成普通和风武士；必须保留 BLEACH 的黑白死神与灵压
- **maker_safe_assets**: Maker 目标 4：斩击 SVG、墨刷贴图、灵压光边

### 4. UI Translation Recommendations
- **panel_design**: 暗色切角卡+墨刷边+刀痕角标
- **state_design**: selected 用蓝白灵压光；warning 用红紫敌意，不作普通强调
- **text_design**: 标题锋利动漫感，正文白/黑高对比
- **accent_design**: 刀痕、灵压火焰、墨线、队章、符纸、斩击弧。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 黑白魂界/夜空远景，边缘斩击线，中心干净。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 4：斩击 SVG、墨刷贴图、灵压光边

### 5. Tool Background Prompt
> 生成黑白魂界刀鸣动作工具背景，黑白灰与蓝白灵压基调，边缘有斩魄刀刀痕、墨线、队章、符纸和斩击弧，中央 50% 干净低纹理，无角色大图、无清晰文字、无假 UI。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成普通和风武士；必须保留 BLEACH 的黑白死神与灵压
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 境·界 刀鸣
aliases: []
category: 动作 / 动漫 IP / 格斗
visual_identity: 黑白魂界刀鸣热血动作
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [bleach, sword, anime-action]
misclassification_risks: 误判成普通和风武士；必须保留 BLEACH 的黑白死神与灵压
maker_feasibility_target: "4-5"
tags: [bleach, sword, anime-action, soul]
```

## 50. 无限暖暖

### 1. Text Research Summary
- **sources_checked**: https://www.taptap.cn/app/247283
- **game_type**: 换装 / 开放世界 / 冒险
- **core_gameplay**: 开放世界探索、能力套装、拍照、轻冒险和时装收集
- **confidence**: high

### 2. Game Style Understanding
- **recognized_visual_identity**: 童话织物开放世界换装冒险
- **genre_presentation**: 把开放世界换装视觉化为布料、花朵、阳光、奇想大陆、能力服装和柔软的梦幻旅行。
- **primary_mood**: 梦幻、温柔、自由、精致
- **world_semantics**: 奇想大陆、服装能力、花朵、蝴蝶、相机、缎带、旅行、织物
- **common_ui_material_language**: 丝绸、蕾丝、柔光玻璃、纸卡、花纹布料、珍珠
- **shape_language**: 柔圆、花瓣边、缎带曲线、轻薄层叠
- **palette_tendency**: 暖白/浅粉作底；草绿/天空蓝作旅行；金色作高级；薰衣草紫作梦幻；红色仅作少量提示
- **accent_semantics**: 缎带、花瓣、蝴蝶、衣架、相机、纽扣、蕾丝
- **background_language**: 童话草地/衣橱/花园远景，边缘织物花朵，中心留白
- **misclassification_risks**: 误判成普通粉色换装或儿童童话；需保留开放世界旅行和能力服装

### 3. Auto Game Style Brief
- **style_keywords**: 童话织物开放世界换装冒险
- **mood**: 梦幻、温柔、自由、精致
- **world_semantics**: 奇想大陆、服装能力、花朵、蝴蝶、相机、缎带、旅行、织物
- **material_language**: 丝绸、蕾丝、柔光玻璃、纸卡、花纹布料、珍珠
- **shape_language**: 柔圆、花瓣边、缎带曲线、轻薄层叠
- **palette_intent**: 暖白/浅粉作底；草绿/天空蓝作旅行；金色作高级；薰衣草紫作梦幻；红色仅作少量提示
- **state_language**: selected 用金色花瓣/缎带边；warning 用柔红小提示
- **accent_semantics**: 缎带、花瓣、蝴蝶、衣架、相机、纽扣、蕾丝
- **background_language**: 童话草地/衣橱/花园远景，边缘织物花朵，中心留白
- **forbidden_directions**: 误判成普通粉色换装或儿童童话；需保留开放世界旅行和能力服装
- **maker_safe_assets**: Maker 目标 4：圆角卡、花瓣/缎带贴图、轻渐变

### 4. UI Translation Recommendations
- **panel_design**: 柔光纸卡+蕾丝/缎带边，小卡保留干净
- **state_design**: selected 用金色花瓣/缎带边；warning 用柔红小提示
- **text_design**: 标题优雅圆润，正文深灰清晰
- **accent_design**: 缎带、花瓣、蝴蝶、衣架、相机、纽扣、蕾丝。装饰应具有功能或世界观语义，避免每张卡都堆强装饰。
- **background_design**: 童话草地/衣橱/花园远景，边缘织物花朵，中心留白。背景弱于 UI，UI 安全区低纹理、低对比、无强视觉中心。
- **maker_feasibility**: Maker 目标 4：圆角卡、花瓣/缎带贴图、轻渐变

### 5. Tool Background Prompt
> 生成童话织物开放世界换装工具背景，暖白浅粉与淡草绿天空蓝基调，边缘有花园远景、缎带、花瓣、蝴蝶、衣架、相机和柔软布料纹理，中央 55% 干净低纹理，无角色、无清晰文字、无假 UI。

### 6. Quality Gate
- **check_result**: pass with risk note — 误判成普通粉色换装或儿童童话；需保留开放世界旅行和能力服装
- **fix_if_failed**: 若产出图过像完整插画，降低远景细节和对比，移除角色主视觉、清晰文字、假按钮与中心强光。

### 7. GitHub Metadata
```yaml
game_or_style_name: 无限暖暖
aliases: []
category: 换装 / 开放世界 / 冒险
visual_identity: 童话织物开放世界换装冒险
source_confidence: high
last_updated: 2026-05-13
recommended_archetypes: [dress-up, open-world, fairy-tale]
misclassification_risks: 误判成普通粉色换装或儿童童话；需保留开放世界旅行和能力服装
maker_feasibility_target: "4-5"
tags: [dress-up, open-world, fairy-tale, fabric]
```

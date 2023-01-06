# ONMYOJI ARENA WIKI DATA

Endpoints from https://www.onmyojiarena.us/index.html and http://moba.163.com/index.html.

## Shikigami data

Below are all the relevant data for each shikigami. Feel free to explore what I left out (plenty of them) by using these endpoints.

### English Endpoint(NA/EU/SEA)
```
https://comp-sync.webapp.163.com/g78na_hero/free_convey?lang=en
```
### Chinese Endpoint (HK/MAINLAND)
You most likely don't need this one, but felt like including it just in case someone needs it.
```
https://comp-sync.webapp.163.com/g78_hero/free_convey
```

### Shikigami Basic Information

|Key|Key Translation|Value Type|Sample Value|Value Translation|
|-------------|---------------|----------|------------|-----------------|
|式神名称|Shikigami Name|String|Hiyoribou|
|式神方头像|Shikigami Avatar|String|gui2/res/head_fang/1067.png|
|式神全身像|Shikigami 2D Art|String|gui/res/hero_quan2/1011.png|
|式神标签|Specialty|String|Burst/Charge
|推荐分路|Lane|String|上|Top Lane
|"|"|"|中|Mid Lane
|"|"|"|野|Jungle
|"|"|"|辅|Bottom Lane (Support Position)
|"|"|"|下|Bottom Lane (Marksman Position)
|式神定位|Shikigami Roles|Array|["忍", "侍"] (>/ 2)|["Ninja", "Samurai"]
|"|"|"|["射"]|["Marksman"]
|"|"|"|["守"]|["Tank"]
|"|"|"|["巫"]|["Mage"]
|"|"|"|["祝"]|["Support"]
|cv名字|Voice Actors|Array|["Akira Ishida", "Di Wei", "Yuri Lowenthal", "남도형"]

### Shikigami Score
|Key|Key Translation|Value Type|Sample Value|Value Translation|
|-------------|---------------|----------|------------|-----------------|
|评分|Shikigami Scores|Object|
|输出|DPS|Number|1|D
|控制|CC|Number|2|C
|生存|Sustain|Number|3|B
|增益|Buffs|Number|4|A
|敏捷|Agility|Number|5|S

### Shikigami Stats
|Key|Key Translation|Value Type|Sample Value|Unit|Formula|
|---|---------------|----------|------------|----|-------|
|式神基础属性| Base Stats|Object
|式神属性成长|Growth Stats (Scaling)|Object
|式神基础属性.物理伤害|Base Attack Damage|Number|87
|式神属性成长.物理伤害|Attack Damage Scaling|Number|4.5|+X/Lvl
|式神基础属性.攻击速度|Base Attack Speed Coefficient (?)|Number|0.68
|式神基础属性.攻速加成|Base Attack Speed Scaling|Number|0.29
||Actual Base Attack Speed|Number|0.87|atks/s|0.68*(1+0.29)
|式神属性成长.攻速加成|Base Attack Speed Scaling|Number|0.0007|+X/Lvl
|式神基础属性.魔法上限|Base Mana Point|Number|300|mp or pts
|式神属性成长.魔法上限|Mana Point Scaling|Number|40|mp/Lvl or pts/Lvl
|式神基础属性.魔法回复|Base Mana Regeneration|Number|10|mp/s or pts/s
|式神基础属性.魔抗|Base Magic Armor|Number|64|
|式神属性成长.魔抗|Magic Armor Scaling|Number|3|
|式神基础属性.生命值|Base Health Point|Number|865|hp
|式神属性成长.生命值|Base Health Point|Number|163|+Xhp/Lvl
|式神基础属性.生命恢复|Base HP Regeneration|Number|14|+Xhp/s
|式神属性成长.生命恢复|Base HP Regeneration|Number|0.82|+Xhp/s/Lvl
|式神基础属性.护甲|Base Physical Armor|Number|54|
|式神属性成长.护甲|Physical Armor Scaling|Number|6.2|
|式神基础属性.移动速度|Base Movement Speed|Number|33.5|yards/m(?)|335
||Base Movement Speed|Number|34|yards/m(?)|340

### Shikigami Recommended Builds
|Key|Key Translation|Value Type|Sample Value|
|---|---------------|----------|------------|
|推荐装备|Recommended Builds|Object
|推荐装备-默认方案1-说明|Default Build 1 Name|String| "Support, Survivability"
|推荐装备-默认方案1|Default Build 1|Array|["Fashionable Trinket", "Takemikazuchi Boots", "Dream Vestiges", "Moonlight Meditation", "Gold Hachiman Do", "Glittering Dream", "Gates of Amanoiwato", "Yata no Kagami"]
|推荐装备-默认方案2-说明|Default Build 2 Name|String| "Survivability"
|推荐装备-默认方案2|Default Build 2|Array|(same type of content as default build 1)
|推荐装备-默认方案3-说明|Default Build 3 Name|String| "Support, Harass"
|推荐装备-默认方案3|Default Build 3|Array|(same type of content as default build 1)

### Shikigami Skills
|Key|Key Translation|Value Type|Sample Value|
|---|---------------|----------|------------|
|式神技能|Shikigami Skills|Object
|天生被动|Passive Ability|Object
|一技能|Ability 1|Object
|二技能|Ability 2|Object
|三技能|Ability 3|Object
|四技能|Ultimate Ability|Object
|图标路径|Ability Icon|String|gui/res/skill/1117000.png
|技能成长|Ability Value Scaling (includes cooldown and mp cost)|Array|
|冷却|Ability Cooldown|Array|[8, 7, 7, 6, 6]
|消耗|Ability Mana Cost|Array|[40, 50, 60, 70, 80]
|技能名称|Ability Name|String|Pray for Sunshine
|技能描述|Ability Description|String|"Passive effect: While Hiyoribou's sunshine doll is following an allied shikigami, it will provide them with 20#c0095cc(+2*Current Level) #n  Armor and Magic Resist while also assisting the target with basic attacks. Once the sunshine doll is 1200 yards away from Hiyoribou, it will no longer follow the allied shikigami."

## Shikigami Items
```
https://comp-sync.webapp.163.com/g78na_equip/free_convey?lang=en
```
Included are all the shop items along with a few that don't usually show up inside the shop.
### Item Object keys
|Key|Key Translation|Value Type|Sample Value|
|---|---------------|----------|------------|
|装备类型|Item Type|Array|["Weapon", "Magic"]
|图标路径|Item Icon|String|"gui/res/equip/111.png"
|装备名称|Item Name|String|"Kusarigama"
|装备等级|Weapon Level|String|"Advanced"
|装备属性|Item Attributes|Array|["+90 Ability Power", "+300 MP", "+50% MP Regen", "+10% Cooldown Reduction"]
|装备主动技能|Active Ability|String|"#OActive - Fluorescence#n: Restores 40#c0095cc(+30*Current Level) #n  HP and 30#c0095cc(+15*Current Level) #n  MP for nearby allied shikigami over the next 4 seconds. (CD: 60 seconds)."|
|装备被动技能|Passive Abilities|Array|"#ONether Arrow#n: Basic attacks deal 30#c0095cc(+2\*Current Level) #n  extra magic damage to target. Every time after using 2 basic attacks or abilities, the next basic attack will trigger a bonus basic attack effect."|
|装备价格|Item Price|Number|1650
|装备额外描述|Unique Description (mostly jungler items)|String|"#r#ODemonbane#n: Upgrade the Subdue ability to Ice Subdue."

## Onmyodos and Spells
I haven't used any of these yet.
### Onmyodos [EN]
```
https://comp-sync.webapp.163.com/g78na_talent/free_convey?lang=en
```
### Onmyodos [CN]
```
https://comp-sync.webapp.163.com/g78_talent/free_convey
```
### Spells [EN]
```
https://comp-sync.webapp.163.com/g78na_mantra/free_convey?lang=en
```
### Spells [CN]
```
https://comp-sync.webapp.163.com/g78_mantra/free_convey
```

## Image Dictionary
### EN Image Dictionary Endpoint
 Contains image links for abilities, shikigami 2D art and avatars, as well as an incomplete set of item image links (The CN endpoint has the complete set).
```
https://comp-sync.webapp.163.com/g78na_pics/api?lang=en
```
### CN Image Dictionary Endpoint
The response also returns image links for avatar frames, spells, onmyodos, most skins.
```
https://comp-sync.webapp.163.com/g78_pics/api
```
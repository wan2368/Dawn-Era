
[core]
class: CustomUnitMetadata
price: 0
maxHp: 100
mass: 20000
armourMinDamageToKeep: 0
ignoreInUnitCapCalculation:true
canNotBeDamaged:true
transportSlotsNeeded: 99999
techLevel: 1
buildSpeed: 1s
radius: 32
isBuilding: false
isBio: false
softCollisionOnAll: 2
showInEditor: false
displayText:大型靶

[graphics]
total_frames: 1

image:        turret_base.png
image_wreak:  NONE
image_turret: NONE
image_shadow: NONE
icon_zoomed_out_neverShow: true
rotate_with_direction:false
imageScale: 2

[attack]
canAttack: false
canAttackFlyingUnits: false
canAttackLandUnits:   false
canAttackUnderwaterUnits: false
maxAttackRange: 0
[movement]

moveSpeed: 3
moveAccelerationSpeed: 0.05
moveDecelerationSpeed: 0.05
reverseSpeedPercentage: 1
maxTurnSpeed: 9999
moveSlidingMode:true
moveIgnoringBody:true

[action_删除]
price: 0
text_zh:删除靶子
description_zh:再次点击\n确认删除
pos: 99
buildSpeed: 0
displayType: none
deleteSelf:true


[action_变小]
price: 0
text_zh:变小
description_zh:  
pos: 100
buildSpeed: 0
displayType: none
alwaysSinglePress:true

[action_激光]
price: 0
text_zh:激光
description_zh:  
pos: 101
buildSpeed: 0
displayType: none
alwaysSinglePress:true

[action_计伤]
price: 0
text_zh:计伤
description_zh:  
pos: 102
buildSpeed: 0
displayType: none
alwaysSinglePress:true

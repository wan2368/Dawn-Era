
[core]
class: CustomUnitMetadata
price: 0
maxHp: 10000000
mass: 10000
ignoreInUnitCapCalculation:true
transportSlotsNeeded: 99999
techLevel: 1
buildSpeed: 1s
radius: 16
isBuilding: false
isBio: false
softCollisionOnAll: 2
showInEditor: false
disableDeathOnZeroHp:true

energyMax:240
energyRegen:-4
isUnrepairableUnit: true
autoTriggerCooldownTime_allowDangerousHighCPU:true
autoTriggerCooldownTime:0.001s

[graphics]
total_frames: 1

image:        turret_base.png
image_wreak:  NONE
image_turret: NONE
image_shadow: NONE
icon_zoomed_out_neverShow: true
rotate_with_direction:false
showEnergyBar:false
showHealthBar:false

[attack]
canAttack: false
canAttackFlyingUnits: false
canAttackLandUnits:   false
canAttackUnderwaterUnits: false
maxAttackRange: 0
[movement]

moveSpeed: 2
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
pos: 30
buildSpeed: 0
displayType: none
deleteSelf:true

[hiddenAction_hf]
price: 0
autoTrigger: if self.hp==0
addResources: hp=100000000
buildSpeed: 0

[hiddenAction_hfnl]
price: 0
autoTrigger: if self.energy==0
addResources: energy=240
buildSpeed: 0

[action_cz]
price:0
addResources: hp=100000000
buildSpeed: 0
displayType: action
pos:31
text_zh:重置累计
description_zh:再次点击\n确认重置

[action_累计]
displayType:infoOnly
text:累计伤害\n%{self.maxhp-self.hp}
pos: 50
buildSpeed:0s
isVisible:true
isActive: false








[resource_计时]
hidden:true
displayName: 
[resource_受伤前]
hidden:true
displayName: 
[resource_受伤后]
hidden:true
displayName: 
[resource_计算]
hidden:true
displayName: 
displayRoundedDown:true

[hiddenAction_计时]
price: 0
autoTrigger:  if self.energy<=7
addResources: 计时=1

[hiddenAction_受伤前]
price: 0
autoTrigger: if self.energy==240
setResourcesWithLogic:受伤前=self.hp

[hiddenAction_受伤后]
price: 0
autoTrigger: if self.energy<=120
setResourcesWithLogic:受伤后=self.hp

[hiddenAction_计算]
price: 0
autoTrigger: if self.resource.计时==3 and self.hp<10000000
setResourcesWithLogic:计算=self.resource.受伤前-self.resource.受伤后
addResources: 计时=-3

[hiddenAction_fz]
price: 0
autoTrigger: if self.resource.计时==3
addResources: 计时=-3

[action_每秒伤害]

text:每秒伤害\n%{self.resource.计算}
displayType:infoOnly
pos: 51
buildSpeed:0s
isVisible:true
isActive: false


[action_变大]
price: 0
text_zh:变大
description_zh:  
pos: 100
buildSpeed: 0
displayType: none
alwaysSinglePress:true

[action_变小]
price: 0
text_zh:变小
description_zh:  
pos: 101
buildSpeed: 0
displayType: none
alwaysSinglePress:true

[action_激光]
price: 0
text_zh:激光
description_zh:  
pos: 102
buildSpeed: 0
displayType: none
alwaysSinglePress:true

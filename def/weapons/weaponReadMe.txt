Mods ReadMe:

>> In this section of the readMe I express the changes made within the def files of Quake 4
The weapon changes are meant to reflect the weapons in Left 4 Dead <<

player.def:

changed the default weapon from weapon_blaster to weapon_gauntlet
changed pm_jumpheight to 100
changed pm_stepsize to 40
changed pm_speed from 160 to 300
changed pm_walkspeed from 80 to 100
changed pm_normalheight from 74 to 68
changed pm_normalviewheight from 68 to 64

blaster.def:

changed chargeTime from .8 to .01 
changed chargeDelay from .1 to .01
changed fireRate from .15 to .001
changed spread from .2 to 5

machinegun.def:

changed inv_start_ammo_machinegun from 50 to 100
changed spread from 2 to 5
changed clipSize from 50 to 100
changed lowAmmo from 20 to 50
changed damage in entityDef damage_machinefun from 15 to 20
changed damage in damage_machinegun_zoom from 20 to 24
changed damage_flesh in damage_machinegun_zoom from 24 to 28

(to resemble more of a melee weapon in Left 4 Dead) gauntlet.def:

changed blade_spinslow from 90 0 0 to 200 0 0 
changed blade_accel from .25 to .5
changed range from 48 to 80
changed damage from 50 to 80
changed knockback from 50 to 80

>>Enemies drop weapons onDeath<<

AI.cpp:

removed the comments on half of the void idAI: :OnDeath function

if( rVal < 25 ){	// Half of guys drop nothing?
			spawnArgs.Set( "def_dropsItem1", "weapon_blaster" ); 
//changed it to weapon_blaster so that the player has a chance to pick up weapons
		}else if( rVal < 50 ){
		spawnArgs.Set( "def_dropsItem1", "weapon_machinegun" ); 
//made it weapon_machinegun that can drop
		
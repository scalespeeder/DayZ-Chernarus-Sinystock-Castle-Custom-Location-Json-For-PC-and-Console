DayZ Chernarus Sinystok Castle For Console and PC json Mod Instructions & Terms Of Use

Spawns a Castle & related structures at  1210.76 / 12313.61 which is North West of Sinystok on Chernarus.

Limited Testing on PC Chernarus Local Server DAYZ Version 1.16 Apr 2021.

Created by @scalespeeder. Please report bugs & errors to scalespeeder@gmail.com with screenshots.

If you'd like to edit my Bunker, simply load "sinystok-castle-editor.dze" into DayZ Editor.

Many Thanks To Inclement Dab for his amazing DayZ Editor that makes this all possible: https://steamcommunity.com/sharedfiles/filedetails/?id=2250764298

TERMS OF USE
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS
OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN
AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH
THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Using these modded json files and instructions could break the functioning of your DAYZ server, requiring a reinstall that would wipe
all player progress.

Using these modded files neccessitates increased regular restarts to prevent server crashing.

It is suggested you thoroughly test your server after applying these files to ensure proper
functioning of your server.

I always recomend you validate your files at: https://www.xmlvalidation.com/ and https://jsonformatter.curiousconcept.com/

Instructions:

Click the "Code" button and "Download Zip" on the Github Repository and extract the files on your local PC for access.

Stop your server.

Ensure your DayZ Server has activated the cfggameplay.json. For console users on Nitrado Servers, go to "General Settings" on your server and tick "Enable cfggameplay.json".

On PC Servers add the following line to your serverDZ.cfg:

enableCfgGameplayFile = 1;

(On some PC servers, including Nitrado, the serverDZ.cfg is "hidden", so you need to enable "expert mode" in settings,
then go to "expert settings", which is the serverDZ.cfg. Stop the server before making changes this way.)

Upload "sinystok-castle.json" from the extracted files to inside the "custom" folder of the mission directory on your server.
(If you haven't got a "custom" folder, create one.)

Open the cfggameplay.json file in the correct mission file for your server and look for the "objectSpawnersArr" line.

This file tells your server to access your custom file.

Edit it to look like this: 

	"objectSpawnersArr": ["custom/sinystok-castle.json"]	
	
If you already are calling custom jsons to spawn items or buildings, seperate the files like this:

	"objectSpawnersArr": ["custom/sinystok-castle.json","custom/anotherfile.json","custom/differentfile.json"]
	
Save your changes & upload if you need to.

Next we add loot to the structures by adding the following code snippet to the top of your mapgrouppos.xml file, after <map> 

	<!--Sinystok Castle Loot-->
	<group name="Land_Castle_Bergfrit" pos="1202.349976 382.048004 12304.000000" rpy="0.000000 0.000000 35.135292" a="54.8647"/>
	<group name="Land_Castle_Wall1_20" pos="1214.300049 383.309998 12315.799805" rpy="0.000000 0.000000 123.040977" a="-33.041"/>
	<group name="Land_Castle_Stairs_nolc" pos="1212.650024 383.032990 12317.500000" rpy="0.000000 0.000000 125.153992" a="-35.154"/>
	<group name="Land_Castle_Wall2_Corner1" pos="1218.520020 381.694000 12324.700195" rpy="0.000000 0.000000 31.205206" a="58.7948"/>
	<group name="Land_Castle_Wall1_20_nolc" pos="1211.780029 383.325989 12331.599609" rpy="0.000000 0.000000 35.632996" a="54.367"/>
	<group name="Land_Castle_Wall1_20_nolc" pos="1195.260010 383.252991 12343.400391" rpy="0.000000 0.000000 35.632996" a="54.367"/>
	<group name="Land_Castle_Gate" pos="1186.290039 383.438995 12338.900391" rpy="0.000000 0.000000 125.751984" a="-35.752"/>
	<group name="Land_Castle_Wall1_20" pos="1183.109985 383.673004 12321.500000" rpy="0.000000 0.000000 -58.252804" a="148.253"/>
	<group name="Land_Castle_Wall1_20_nolc" pos="1186.939941 383.756989 12308.099609" rpy="0.000000 0.000000 -145.837006" a="-124.163"/>
	<group name="Land_Castle_Stairs_nolc" pos="1197.800049 383.696014 12337.099609" rpy="0.000000 0.000000 -147.802994" a="-122.197"/>
	<group name="Land_Castle_Stairs_nolc" pos="1185.880005 382.891998 12320.400391" rpy="0.000000 0.000000 -60.322895" a="150.323"/>
	<group name="Land_Mil_Fortified_Nest_Small" pos="1182.052734 381.126251 12349.640625" rpy="-0.000000 -0.000000 172.933502" a="-82.9335"/>
	<group name="Land_Mil_Fortified_Nest_Small" pos="1175.196167 380.770630 12340.052734" rpy="-0.000000 -0.000000 98.108948" a="-8.10895"/>
	<group name="Land_wreck_truck01_aban1_green" pos="1176.699951 379.053986 12328.299805" rpy="-5.999999 0.000000 123.426979" a="-33.427"/>
	<group name="Land_wreck_truck01_aban1_green" pos="1173.069946 379.122986 12325.400391" rpy="0.000000 0.000000 138.557968" a="-48.558"/>
	<group name="Land_wreck_truck01_aban1_green" pos="1171.339966 378.927002 12321.400391" rpy="-9.499999 0.000000 125.517967" a="-35.518"/>
	<group name="Land_Misc_Well_Pump_Blue" pos="1202.616455 379.109222 12300.466797" rpy="-0.000000 -0.000000 -60.960533" a="150.961"/>
	<group name="Land_Misc_Toilet_Mobile" pos="1207.307617 379.998718 12310.145508" rpy="-0.000000 -0.000000 -141.141815" a="-128.858"/>
	<group name="Land_Misc_Toilet_Mobile" pos="1206.246948 380.036530 12310.994141" rpy="-0.000000 -0.000000 -141.677261" a="-128.323"/>
	<group name="Land_Roadblock_Table" pos="1199.250000 379.597992 12302.799805" rpy="0.000000 0.000000 35.097996" a="54.902"/>
	<group name="Land_Roadblock_Table" pos="1201.120361 379.588806 12301.363281" rpy="-0.000000 -0.000000 33.155933" a="56.8441"/>
	<group name="Land_Mil_Tent_Big1_1" pos="1188.030029 390.498993 12342.700195" rpy="0.000000 0.000000 35.999996" a="54"/>
	<group name="Land_Mil_Fortified_Nest_Small" pos="1198.660034 380.704010 12330.400391" rpy="0.000000 0.000000 123.712982" a="-33.713"/>
	<group name="Land_Mil_Tent_Big1_2" pos="1188.891724 378.947235 12313.900391" rpy="-0.000000 -0.000000 -147.852051" a="-122.148"/>
	<group name="Land_Roadblock_Table" pos="1200.550049 391.122009 12302.099609" rpy="0.000000 0.000000 39.999996" a="50"/>
	<group name="Land_Roadblock_WoodenCrate" pos="1205.180054 391.049011 12307.500000" rpy="0.000000 0.000000 114.427002" a="-24.427"/>
	<group name="Land_Roadblock_WoodenCrate" pos="1206.569946 391.109009 12305.900391" rpy="0.000000 0.000000 175.926987" a="-85.927"/>
	<group name="Land_Misc_Polytunnel" pos="1215.153076 381.285217 12325.473633" rpy="-0.000000 -0.000000 34.356880" a="55.6431"/>
	<group name="Land_Mil_Fortified_Nest_Small" pos="1129.102661 380.269867 12300.130859" rpy="-0.000000 -0.000000 31.213469" a="58.7865"/>
	<group name="Land_Medical_Tent_Big" pos="1147.859985 379.501007 12314.400391" rpy="0.000000 0.000000 117.800987" a="-27.801"/>
	<group name="Land_Wreck_Ikarus" pos="1153.108398 380.557587 12334.166016" rpy="-0.000000 -0.000000 0.000000" a="90"/>
	<group name="Land_Wreck_Lada_Green" pos="1120.310059 379.368988 12287.900391" rpy="0.000000 0.000000 -139.425980" a="-130.574"/>
	<group name="Land_Wreck_Lada_Red" pos="1114.599976 378.875000 12284.500000" rpy="0.000000 -6.500000 -103.053993" a="-166.946"/>
	<group name="Land_Wreck_Volha_Grey" pos="1109.189941 378.225006 12282.599609" rpy="0.500000 -10.500000 -126.600990" a="-143.399"/>
	<group name="Land_Wreck_hb02_aban2_black" pos="1103.530029 377.644989 12280.400391" rpy="0.000000 -2.400000 -101.511993" a="-168.488"/>
	<group name="Land_Wreck_Uaz" pos="1270.381714 387.432800 12547.916016" rpy="-0.000000 -0.000000 -152.463943" a="-117.536"/>
	<group name="Land_Dead_MassGrave" pos="1275.791870 387.079926 12557.940430" rpy="-0.000000 -0.000000 0.000000" a="90"/>
	<group name="Land_wreck_truck01_aban2_green" pos="1264.864624 386.559570 12550.012695" rpy="-0.000000 -0.000000 50.594139" a="39.4059"/>
	<!--End Of Sinystok Castle Loot-->
	
	
Save your changes & upload if you need to.

Restart your server and the new structures will appear immediatly, and then they will slowly stock with loot.

Thanks, Rob.
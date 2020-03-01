			
			Column token:
			---------------------------------------------------------------------------
			A   = Active
			I   = Init   (not changeable)
			R   = Reverse
			S   = Send not zero values (useful for rotary switches and pushbuttons)
			T   = Test
			LP  = Left padding
			dM  = dimming mode: 0 == off
			dT  = dimming time interval [sec.]
			dV  = dimming value
			Max = max value (range 0.0 - 1.0 only LED driver 3)
			
			For rotary switches, please check R and S for all positions.
			
			If you check one of these fields: 
			
			A  = Active
			R  = Reverse
			T  = Test
			
			Please select another field. Then the action behind the checkbox is 
			performed.
			

			Export.lua:
			---------------------------------------------------------------------------
			Package example: "File=A-10C:163=1.0:171=1.0:179=1.0:47=1.0:586=1.0:"
			The delimiter is ':'
			Switch/Load a new profile from data package ('File=A-10C:')
			The parameter 'A-10C' comes from selfData.Name. The file A-10C.xml will be 
			loaded.

	
			Log:
			---------------------------------------------------------------------------
			Modul == 00, Connector == 00 -> Port A  ... Arcaze USB
			Modul == 00, Connector == 01 -> Port B  ...    -"-
			Modul >= 01, Connector == 00 -> Port C  ... LED-Driver
			Modul >= 01, Connector == 01 -> Port D  ...    -"-
			Modul >= 01, Connector == 02 -> Port E  ...    -"-
	
			All values in HEX; Pin numbers in Dez;

	
			Tab 'Configuration'
			---------------------------------------------------------------------------
			Please, uncheck the checkbox 'log all actions', if you are ready with your 
			tests and configurations.
			

			Tab 'Display', 'LEDs', 'Switches' and 'Encoders'
			---------------------------------------------------------------------------
			Both checkboxes 'Active' and 'Init' must checked to get new values from a 
			record.
			
	
			Tab 'LEDs'
			---------------------------------------------------------------------------
			Dimming:
	
			dM = dimming mode: 0 == off
			dT = dimming time interval [sec.]
			dV = dimming value
	                Trype = ID or Special. Normally it is always ID.
			Format = decimal or float4. Normally it is decimal. For dimming it is float4.
			
			For activation of automatic dimming: value > 0.5; dM != 0
			Real dimming is only possible with LED-Driver 3, but for other LEDs you get 
			a automatic blinking.
			
			One more thing: Please use only LED-Driver 2 or LED-Driver 3 on a Arcaze.
                        
			Tab 'Displays'
			---------------------------------------------------------------------------
			RadioDevice: Specifies the radio device to be queried. Under ID the Device ID 
			of the radio must be specified.
			Under Format the frequency format must be specified, e.g. MHz for megaherz.
			
			ListIndication: Specifies that values from displays are to be queried. 
			Under ID the Indication ID for the query must be specified. 
			Under Format the name of the return value must be specified.
			
			Special: If data about the ExportScript module specific extensions should be queried. 
			Under ID the corresponding ID from the extension file must be specified.
	
			Tab 'Masterdata'
			---------------------------------------------------------------------------
			Table 'Device IDs' and 'Device IDs and Button IDs';
	
			Please look at the files device.lua and clickabledata.lua of your DCS-Modul. 
			There are all infos you need:
			"... \Eagle Dynamics\DCS World\Mods\aircrafts\A-10C\Cockpit\Scripts\ ..."

			For more help look at:
	                https://github.com/s-d-a/DCS-ExportScripts/wiki
                   

			

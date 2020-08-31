function run(input, parameters) {
	const app = Application.currentApplication();
	app.includeStandardAdditions = true;
 	const se = Application("System Events");
	const frontmost = se.processes.whose({frontmost: true})[0];
	const bundleId = frontmost.bundleIdentifier();
	if(bundleId === 'com.microsoft.VSCode') {
		se.keystroke('f', {
    		using: ['shift down', 'option down']
		});
	} else if (bundleId === 'com.sublimetext.3') {
		//se.keystroke('');
	} else if (bundleId === 'com.apple.dt.Xcode') {
		se.keystroke('i', {
    		using: 'control down'
		});
	} else if (bundleId === 'com.google.android.studio') {
		se.keystroke('l', {
    		using: ['option down', 'command down']
		});
	} else {
		for(var i = 0; i < bundleId.length; i++){
			se.keystroke(bundleId[i]);
		}
	}
	
	//app.displayDialog(bundleId);
	return input;
}

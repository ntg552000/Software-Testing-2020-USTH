Ex8.3.3
Complete and run the tests to satisfy CACC for the Thermostat class.

curTemp < desiredTemp - thresholdDiff 63 69 5
!(curTemp < desiredTemp - thresholdDiff) 66 69 5
desiredTemp = programmedSettings [Monday].setDesiredTemp (Morning, 69)
dayOfWeek = Monday
timeOfDay = 8:00
Override
Override T
!Override F
curTemp overTemp thresholdDiff
curTemp < overTemp - thresholdDiff 63 70 5
!(curTemp < overTemp - thresholdDiff) 66 70 5
timeSinceLastRun minLag
timeSinceLastRun.greaterThan (minLag) 12 10
!(timeSinceLastRun.greaterThan (minLag)) 8 10












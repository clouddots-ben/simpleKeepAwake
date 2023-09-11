# simpleKeepAwake
A script to run in a PowerShell window to keep a machine awake. It presses the F15 key at a random interval between 30 seconds and 200 seconds.

# Operation
Open a console window in PowerShell or Windows Terminal. Copy and Paste the code seen below and press enter. The computer will be kept awake until you press ctrl+c or close the PowerShell window. It will still run if you minimize the window.

while (1) {
  $RNDSleep = Get-Random -Minimum 30 -Maximum 200
  $wsh.SendKeys('+{F15}')
  Start-Sleep -Seconds $RNDSleep
}

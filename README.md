# restore5
Func restore()
	Local $startticks = _timetoticks(@HOUR, @MIN, @SEC)
	Do
		Sleep(50)
		$adsoff = _imagesearch("restore.BMP", 1, $x, $y, 1)
		Local $startticks2 = _timetoticks(@HOUR, @MIN, @SEC)
		Local $timewait = $startticks2 - $startticks
	Until $adsoff = 1 OR $timewait > 3000
	$adsoff = _imagesearch("restore.BMP", 1, $x, $y, 1)
	If $adsoff = 1 Then MouseClick("", $x, $y)
	Sleep(500)
EndFunc

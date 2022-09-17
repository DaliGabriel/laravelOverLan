# laravelOverLan
Simple powerShell script to run laravel serve over the LAN

Open your power shell profile to add the code:

```
notepad.exe $PROFILE
```
now paste this code

```
function serve{
	cd this\is\your\work\directory
	$ip = Get-NetIPAddress -AddressFamily IPv4 | Select IPAddress -First 1
	php artisan serve --host $ip.IPAddress
}
```

now close the power shell terminal and type "serve" for start laravel serve over LAN

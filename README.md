# Openwrt-radio-check
 Checks if OpenWRT 5Ghz is still working and restarts it if neccessary
 
 Simply upload the script to your router, set it to excutable (chmod 755), and set a cronjob (*/15 * * * * /root/wifi_check.sh) on it for e.g. 15 minutes.
 
 The script will check if the channel used by radio0 will match the channel configured. So with DFS it will detect a fallback to channel 36 and also if wifi is not available. Then it will restart radio0 to get it working again. This is neccessary with OpenWRT as the version today will not switch back to DFS channel automatically and sometimes it simply hangs.

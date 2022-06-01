# 13.1.2
    code_sheep:x:1001:1001::/home/code_sheep:/bin/bash

1. **code_sheep**: account name
2. **x**: password (invisible) 
3. **1001** of one: /etc/passwd had recorded
4. **1001** of two: /home/code_sheep had recorded
5. **::/home/code_sheep**: home directory
6. **/bin/bash** shell

## /etc/shadow
    code_sheep:$6$GSzlOlm5$XxtZ3wCWA8FJwVf18zO.NMHD0U/xCopR.cz. xqVTdjAG5UnzZKen/ajkvuMUHjLdNa5yuO3EVv8b0CbCrtHBi.:19112:0:99999:7:::

- **:19112:** $(( $(date --date="2022/4/29" +%s)/86400 + 1  )) 
- password setted date
    
    86400 is seconds of day  
- **:0:** number of day that the password cannot be changed

- **:99999:** password expire time

- **:7:** will be warning days before password expire time

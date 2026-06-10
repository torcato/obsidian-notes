
**IP**: 185.136.120.131
use wire guard vpn

```sql
CREATE DATABASE raglab
CHARACTER SET utf8mb4
COLLATE utf8mb4_unicode_ci;

CREATE USER 'raglab'@'localhost' IDENTIFIED BY 'password';
 
GRANT ALL PRIVILEGES
ON raglab.*
TO 'raglab'@'localhost';

CREATE USER 'raglab_readonly'@'localhost' IDENTIFIED BY 'password';

GRANT SELECT
ON raglab.*
TO 'raglab_readonly'@'localhost';
```

location:  /opt/ai_chatbot

Generate passwords:
```bash
tr -dc 'A-Za-z0-9!?%=' < /dev/urandom | head -c 15
```
dev.sports.local
webmaster/logic123

mysqldump  --default-character-set=utf8 --complete-insert --flush-logs --add-drop-database --add-drop-table --create-options --quick --lock-tables --quote-names --user=root --password=root --result-file=legatuslocaldb_180724.sql legatusdb

mysql -uroot -proot -e "drop database if exists crltdb"
mysql -uroot -proot -e "create database if not exists crltdb"
mysql -uroot -proot -e "source crltdb180612.sql" crltdb
# Error Architecture

Contents

# Error Code Reference

Notes:*

Errors groups by subsystem.
Each subsystem has a range of errors that start on a 1000.
Error codes are all negative, to make it easy to test for an error condition from a returning function in most cases.
Error codes shown here for MySQL and Linux Operating system are the same error codes used by the vendors.

General Error Codes

Error

Explanation

Success

Operation successfully completed

Alias
SUCCESS

General
Code
0
­10000 UNKNOWN Unknown Error %s
%s
­10001 FATAL
%s
­10002 ERROR
­10003 WARN
%s
%s
­10004 INFO
%s
­10005 DEBUG
­10006 TRACE
%s
Operating System Error Codes

Fatal
Error
Warn
Information
Debug
Trace

Operating System
Code
Alias
­1
­2
­3
­4
­5
­6
­7
­8
­9
­10
­11
­12
­13
­14
­15
­16
­17
­18
­19
­20
­21
­22
­23
­24
­25
­26
­27
­28
­29
­30
­31
­32
­33
­34
­35
­36
­37
­38
­39
­40
­42
­43
­44
­45
­46
­47
­48
­49
­50
­51
­52
­53
­54
­55
­56
­57
­59
­60
­61
­62

EPERM
ENOENT
ESRCH
EINTR
EIO
ENXIO
E2BIG
ENOEXEC
EBADF
ECHILD
EAGAIN
ENOMEM
EACCES
EFAULT
ENOTBLK
EBUSY
EEXIST
EXDEV
ENODEV
ENOTDIR
EISDIR
EINVAL
ENFILE
EMFILE
ENOTTY
ETXTBSY
EFBIG
ENOSPC
ESPIPE
EROFS
EMLINK
EPIPE
EDOM
ERANGE
EDEADLK
ENAMETOOLONG
ENOLCK
ENOSYS
ENOTEMPTY
ELOOP
ENOMSG
EIDRM
ECHRNG
EL2NSYNC
EL3HLT
EL3RST
ELNRNG
EUNATCH
ENOCSI
EL2HLT
EBADE
EBADR
EXFULL
ENOANO
EBADRQC
EBADSLT
EBFONT
ENOSTR
ENODATA
ETIME

Error Architecture ­ 

Error

Explanation

Operation not permitted
No such file or directory
No such process
Interrupted system call
I/O error
No such device or address
Argument list too long
Exec format error
Bad file number
No child processes
Try again
Out of memory
Permission denied
Bad address
Block device required
Device or resource busy
File exists
Cross­device link
No such device
Not a directory
Is a directory
Invalid argument
File table overflow
Too many open files
Not a typewriter
Text file busy
File too large
No space left on device
Illegal seek
Read­only file system
Too many links
Broken pipe
Math argument out of domain of func
Math result not representable
Resource deadlock would occur
File name too long
No record locks available
Function not implemented
Directory not empty
Too many symbolic links encountered
No message of desired type
Identifier removed
Channel number out of range
Level 2 not synchronized
Level 3 halted
Level 3 reset
Link number out of range
Protocol driver not attached
No CSI structure available
Level 2 halted
Invalid exchange
Invalid request descriptor
Exchange full
No anode
Invalid request code
Invalid slot
Bad font file format
Device not a stream
No data available
Timer expired

Error Architecture ­ 

Out of streams resources
ENOSR
Machine is not on the network
ENONET
Package not installed
ENOPKG
Object is remote
EREMOTE
Link has been severed
ENOLINK
Advertise error
EADV
Srmount error
ESRMNT
Communication error on send
ECOMM
Protocol error
EPROTO
Multihop attempted
EMULTIHOP
RFS specific error
EDOTDOT
Not a data message
EBADMSG
Value too large for defined data type
EOVERFLOW
Name not unique on network
ENOTUNIQ
File descriptor in bad state
EBADFD
Remote address changed
EREMCHG
Can not access a needed shared library
ELIBACC
Accessing a corrupted shared library
ELIBBAD
.lib section in a.out corrupted
ELIBSCN
Attempting to link in too many shared libraries
ELIBMAX
Cannot exec a shared library directly
ELIBEXEC
Illegal byte sequence
EILSEQ
Interrupted system call should be restarted
ERESTART
Streams pipe error
ESTRPIPE
Too many users
EUSERS
Socket operation on non­socket
ENOTSOCK
Destination address required
EDESTADDRREQ
Message too long
EMSGSIZE
Protocol wrong type for socket
EPROTOTYPE
ENOPROTOOPT
Protocol not available
EPROTONOSUPPORT Protocol not supported
ESOCKTNOSUPPORT Socket type not supported
EOPNOTSUPP
EPFNOSUPPORT
EAFNOSUPPORT
EADDRINUSE
EADDRNOTAVAIL

­63
­64
­65
­66
­67
­68
­69
­70
­71
­72
­73
­74
­75
­76
­77
­78
­79
­80
­81
­82
­83
­84
­85
­86
­87
­88
­89
­90
­91
­92
­93
­94
­95
­96
­97
­98
­99
­100 ENETDOWN
­101 ENETUNREACH
­102 ENETRESET
­103 ECONNABORTED
­104 ECONNRESET
­105 ENOBUFS
­106 EISCONN
­107 ENOTCONN
­108 ESHUTDOWN
­109 ETOOMANYREFS
­110 ETIMEDOUT
­111 ECONNREFUSED
­112 EHOSTDOWN
­113 EHOSTUNREACH
­114 EALREADY
­115 EINPROGRESS
­116 ESTALE
­117 EUCLEAN
­118 ENOTNAM
­119 ENAVAIL
­120 EISNAM
­121 EREMOTEIO
­122 EDQUOT
­123 ENOMEDIUM
­124 EMEDIUMTYPE
­125 ECANCELED

Operation not supported on transport endpoint
Protocol family not supported
Address family not supported by protocol
Address already in use
Cannot assign requested address
Network is down
Network is unreachable
Network dropped connection because of reset
Software caused connection abort
Connection reset by peer
No buffer space available
Transport endpoint is already connected
Transport endpoint is not connected
Cannot send after transport endpoint shutdown
Too many references: cannot splice
Connection timed out
Connection refused
Host is down
No route to host
Operation already in progress
Operation now in progress
Stale NFS file handle
Structure needs cleaning
Not a XENIX named type file
No XENIX semaphores available
Is a named type file
Remote I/O error
Quota exceeded
No medium found
Wrong medium type
Operation Canceled

Error Architecture ­ 

Required key not available
Key has expired
Key has been revoked
Key was rejected by service
Owner died

­126 ENOKEY
­127 EKEYEXPIRED
­128 EKEYREVOKED
­129 EKEYREJECTED
­130 EOWNERDEAD
­131 ENOTRECOVERABLE State not recoverable
MySQL Error Codes

Error Architecture ­ 

Alias

Error

Explanation

MySQL
Code
­1002 ER_NO

­1003 ER_YES

NO

YES

Used in the construction of other messages.
Used in the construction of other messages. Extended EXPLAIN format generates
Note messages. ER_YES is used in the Code column for these messages in subsequent
SHOW WARNINGS output.
Possible causes: Permissions problem for source .frm file; destination .frm file already
exists but is not writeable.

Drop the database first if you really want to replace an existing database, or add an IF
NOT EXISTS clause to the CREATE DATABASE statement if to retain an existing
database without having the statement produce an error.

Returned by InnoDB for attempts to access InnoDB INFORMATION_SCHEMA
tables when InnoDB is unavailable.

­1004 ER_CANT_CREATE_FILE

­1005 ER_CANT_CREATE_TABLE
­1006 ER_CANT_CREATE_DB

­1007 ER_DB_CREATE_EXISTS

­1008 ER_DB_DROP_EXISTS

­1009 ER_DB_DROP_DELETE

­1010 ER_DB_DROP_RMDIR

­1011 ER_CANT_DELETE_FILE

Can't create file '%s' (errno: %d). Occurs for failure
to copy an .frm file to a new location, durin
Can't create table '%s' (errno: %d)
Can't create database '%s' (errno: %d)

Can't create database '%s'; database exists. An
attempt to create a database failed because the data

Can't drop database '%s'; database doesn't exist
Error dropping database (can't delete '%s',
(errno: %d)
Error dropping database (can't rmdir '%s',
(errno: %d)
Error on delete of '%s' (errno: %d)

­1012 ER_CANT_FIND_SYSTEM_

Can't read record in system table

­1013 ER_CANT_GET_STAT
­1014 ER_CANT_GET_WD
­1015 ER_CANT_LOCK
­1016 ER_CANT_OPEN_FILE
­1017 ER_FILE_NOT_FOUND
­1018 ER_CANT_READ_DIR
­1019 ER_CANT_SET_WD
­1020 ER_CHECKREAD

­1021 ER_DISK_FULL

­1022 ER_DUP_KEY
­1023 ER_ERROR_ON_CLOSE
­1024 ER_ERROR_ON_READ
­1025 ER_ERROR_ON_RENAME
­1026 ER_ERROR_ON_WRITE
­1027 ER_FILE_USED
­1028 ER_FILSORT_ABORT
­1029 ER_FORM_NOT_FOUND

Can't get status of '%s' (errno: %d)
Can't get working directory (errno: %d)
Can't lock file (errno: %d)
Can't open file: '%s' (errno: %d)
Can't find file: '%s' (errno: %d)
Can't read dir of '%s' (errno: %d)
Can't change dir to '%s' (errno: %d)
Record has changed since last read in table '%s'
Disk full (%s); waiting for someone to free some
space...
Can't write; duplicate key in table '%s'
Error on close of '%s' (errno: %d)
Error reading file '%s' (errno: %d)
Error on rename of '%s' to '%s' (errno: %d)
Error writing file '%s' (errno: %d)
'%s' is locked against change
Sort aborted
View '%s' doesn't exist for '%s'

­1030 ER_GET_ERRNO

Got error %d from storage engine

Check the %d value to see what the OS error means. For example, 28 indicates that
you have run out of disk space.

­1031 ER_ILLEGAL_HA
­1032 ER_KEY_NOT_FOUND
­1033 ER_NOT_FORM_FILE
­1034 ER_NOT_KEYFILE
­1035 ER_OLD_KEYFILE
­1036 ER_OPEN_AS_READONLY

Table storage engine for '%s' doesn't have this option
Can't find record in '%s'
Incorrect information in file: '%s'
Incorrect key file for table '%s'; try to repair it
Old key file for table '%s'; repair it!
Table '%s' is read only
Out of memory; restart server and try again
(needed %d bytes

­1039 ER_UNEXPECTED_EOF

­1040 ER_CON_COUNT_ERROR

­1041 ER_OUT_OF_RESOURCES

­1037 ER_OUTOFMEMORY
­1038 ER_OUT_OF_SORTMEMORY Out of sort memory, consider increasing server sort

­1042 ER_BAD_HOST_ERROR
­1043 ER_HANDSHAKE_ERROR
­1044 ER_DBACCESS_DENIED_E

buffer size
Unexpected EOF found when reading file '%s'
(errno: %d)
Too many connections
Out of memory; check if mysqld or some other
process uses all available memory; if not, you may
have
Can't get hostname for your address
Bad handshake
Access denied for user '%s'@'%s' to database '%s'
Access denied for user '%s'@'%s' (using
password: %s
­1046 ER_NO_DB_ERROR
No database selected
­1047 ER_UNKNOWN_COM_ERROR Unknown command
­1048 ER_BAD_NULL_ERROR
­1049 ER_BAD_DB_ERROR
­1050 ER_TABLE_EXISTS_ERRO

Column '%s' cannot be null
Unknown database '%s'
Table '%s' already exists

­1045 ER_ACCESS_DENIED_ERR

­1051 ER_BAD_TABLE_ERROR
­1052 ER_NON_UNIQ_ERROR
­1053 ER_SERVER_SHUTDOWN
­1054 ER_BAD_FIELD_ERROR
­1055 ER_WRONG_FIELD_WITH_
­1056 ER_WRONG_GROUP_FIELD

­1057 ER_WRONG_SUM_SELECT

Error Architecture ­ 

%s = column name. %s = location of column (for example, "field list")

Unknown table '%s'
Column '%s' in %s is ambiguous
Server shutdown in progress
Unknown column '%s' in '%s'
'%s' isn't in GROUP BY
Can't group on '%s'
Statement has sum functions and columns in same
statement

­1058 ER_WRONG_VALUE_COUNT Column count doesn't match value count
­1059 ER_TOO_LONG_IDENT
­1060 ER_DUP_FIELDNAME
­1061 ER_DUP_KEYNAME

Identifier name '%s' is too long
Duplicate column name '%s'
Duplicate key name '%s'

­1062 ER_DUP_ENTRY

Duplicate entry '%s' for key %d

­1063 ER_WRONG_FIELD_SPEC
­1064 ER_PARSE_ERROR
­1065 ER_EMPTY_QUERY
­1066 ER_NONUNIQ_TABLE
­1067 ER_INVALID_DEFAULT
­1068 ER_MULTIPLE_PRI_KEY
­1069 ER_TOO_MANY_KEYS
­1070 ER_TOO_MANY_KEY_PART

­1071 ER_TOO_LONG_KEY

Incorrect column specifier for column '%s'
%s near '%s' at line %d
Query was empty
Not unique table/alias: '%s'
Invalid default value for '%s'
Multiple primary key defined
Too many keys specified; max %d keys allowed
Too many key parts specified; max %d parts allowed
Specified key was too long; max key length is %d
bytes

­1072 ER_KEY_COLUMN_DOES_N Key column '%s' doesn't exist in table

The message returned with this error uses the format string for
ER_DUP_ENTRY_WITH_KEY_NAME.

­1073 ER_BLOB_USED_AS_KEY

­1074 ER_TOO_BIG_FIELDLENG

­1075 ER_WRONG_AUTO_KEY

­1076 ER_READY

­1077 ER_NORMAL_SHUTDOWN
­1078 ER_GOT_SIGNAL
­1079 ER_SHUTDOWN_COMPLETE %s: Shutdown complete
­1080 ER_FORCING_CLOSE
­1081 ER_IPSOCK_ERROR

­1082 ER_NO_SUCH_INDEX

BLOB column '%s' can't be used in key specification
with the used table type
Column length too big for column '%s' (max = %lu);
use BLOB or TEXT instead
Incorrect table definition; there can be only one auto
column and it must be defined as a key
%s: ready for connections. Version: '%s' socket: '%s'
port: %d
%s: Normal shutdown
%s: Got signal %d. Aborting!

%s: Forcing close of thread %ld user: '%s'
Can't create IP socket
Table '%s' has no index like the one used in CREATE
INDEX; recreate the table
Field separator argument is not what is expected;
check the manual

­1089 ER_WRONG_SUB_KEY

­1090 ER_CANT_REMOVE_ALL_F

­1085 ER_TEXTFILE_NOT_READ

­1086 ER_FILE_EXISTS_ERROR

­1087 ER_LOAD_INFO

­1088 ER_ALTER_INFO

­1083 ER_WRONG_FIELD_TERMI
­1084 ER_BLOBS_AND_NO_TERM You can't use fixed rowlength with BLOBs; please
use 'fields terminated by'
The file '%s' must be in the database directory or be
readable by all
File '%s' already exists
Records: %ld Deleted: %ld Skipped: %ld
Warnings: %ld
Records: %ld Duplicates: %ld
Incorrect prefix key; the used key part isn't a string,
the used length is longer than the key part,
You can't delete all columns with ALTER TABLE;
use DROP TABLE instead
Can't DROP '%s'; check that column/key exists
Records: %ld Duplicates: %ld Warnings: %ld
You can't specify target table '%s' for update in
FROM clause
Unknown thread id: %lu
You are not owner of thread %lu
No tables used
Too many strings for column %s and SET
Can't generate a unique log­filename %s.(1­999
Table '%s' was locked with a READ lock and can't be
updated
Table '%s' was not locked with LOCK TABLES
BLOB/TEXT column '%s' can't have a default value

­1094 ER_NO_SUCH_THREAD
­1095 ER_KILL_DENIED_ERROR
­1096 ER_NO_TABLES_USED
­1097 ER_TOO_BIG_SET
­1098 ER_NO_UNIQUE_LOGFILE

­1100 ER_TABLE_NOT_LOCKED
­1101 ER_BLOB_CANT_HAVE_DE

­1091 ER_CANT_DROP_FIELD_O
­1092 ER_INSERT_INFO

­1093 ER_UPDATE_TABLE_USED

­1099 ER_TABLE_NOT_LOCKED_

Error Architecture ­ 

Incorrect database name '%s'
Incorrect table name '%s'
The SELECT would examine more than
MAX_JOIN_SIZE rows; check your WHERE and
use SET SQL_BIG_SELECTS=
Unknown error

­1102 ER_WRONG_DB_NAME
­1103 ER_WRONG_TABLE_NAME

­1104 ER_TOO_BIG_SELECT

­1105 ER_UNKNOWN_ERROR
­1106 ER_UNKNOWN_PROCEDURE Unknown procedure '%s'
­1107 ER_WRONG_PARAMCOUNT_ Incorrect parameter count to procedure '%s'
­1108 ER_WRONG_PARAMETERS_
­1109 ER_UNKNOWN_TABLE
­1110 ER_FIELD_SPECIFIED_T
­1111 ER_INVALID_GROUP_FUN

Incorrect parameters to procedure '%s'
Unknown table '%s' in %s
Column '%s' specified twice
Invalid use of group function
Table '%s' uses an extension that doesn't exist in this
MySQL version
A table must have at least 1 column
The table '%s' is full

­1113 ER_TABLE_MUST_HAVE_C
­1114 ER_RECORD_FILE_FULL
­1115 ER_UNKNOWN_CHARACTER Unknown character set: '%s'

­1112 ER_UNSUPPORTED_EXTEN

­1116 ER_TOO_MANY_TABLES

­1117 ER_TOO_MANY_FIELDS

­1118 ER_TOO_BIG_ROWSIZE

­1119 ER_STACK_OVERRUN

­1120 ER_WRONG_OUTER_JOIN

­1121 ER_NULL_COLUMN_IN_IN

­1122 ER_CANT_FIND_UDF
­1123 ER_CANT_INITIALIZE_U
­1124 ER_UDF_NO_PATHS
­1125 ER_UDF_EXISTS
­1126 ER_CANT_OPEN_LIBRARY
­1127 ER_CANT_FIND_DL_ENTR
­1128 ER_FUNCTION_NOT_DEFI

­1129 ER_HOST_IS_BLOCKED

­1130 ER_HOST_NOT_PRIVILEG

­1131 ER_PASSWORD_ANONYMOU

­1132 ER_PASSWORD_NOT_ALLO

Too many tables; MySQL can only use %d tables in
a join
Too many columns
Row size too large. The maximum row size for the
used table type, not counting BLOBs, is %ld. You ha
Thread stack overrun: Used: %ld of a %ld stack. Use
'mysqld ­­thread_stack=#' to specify a bigger st
Cross dependency found in OUTER JOIN; examine
your ON conditions
Table handler doesn't support NULL in given index.
Please change column '%s' to be NOT NULL or use
a
Can't load function '%s'
Can't initialize function '%s'; %s
No paths allowed for shared library
Function '%s' already exists
Can't open shared library '%s' (errno: %d %s
Can't find symbol '%s' in library
Function '%s' is not defined
Host '%s' is blocked because of many connection
errors; unblock with 'mysqladmin flush­hosts'
Host '%s' is not allowed to connect to this MySQL
server
You are using MySQL as an anonymous user and
anonymous users are not allowed to change
passwords
You must have privileges to update tables in the
mysql database to be able to change passwords for o

­1133 ER_PASSWORD_NO_MATCH Can't find any matching row in the user table
­1134 ER_UPDATE_INFO

Rows matched: %ld Changed: %ld Warnings: %ld
Can't create a new thread (errno %d); if you are not
out of available memory, you can consult the ma

­1135 ER_CANT_CREATE_THREA

­1140 ER_MIX_OF_GROUP_FUNC

­1136 ER_WRONG_VALUE_COUNT Column count doesn't match value count at row %ld
­1137 ER_CANT_REOPEN_TABLE
­1138 ER_INVALID_USE_OF_NU
­1139 ER_REGEXP_ERROR

Can't reopen table: '%s'
Invalid use of NULL value
Got error '%s' from regexp
Mixing of GROUP columns
(MIN(),MAX(),COUNT(),...) with no GROUP
columns is illegal if there is no GR
There is no such grant defined for user '%s' on host
'%s'
­1142 ER_TABLEACCESS_DENIE
%s command denied to user '%s'@'%s' for table '%s'
­1143 ER_COLUMNACCESS_DENI %s command denied to user '%s'@'%s' for column
'%s' in table '%s'
Illegal GRANT/REVOKE command; please consult
the manual to see which privileges can be used

­1141 ER_NONEXISTING_GRANT

­1144 ER_ILLEGAL_GRANT_FOR

­1145 ER_GRANT_WRONG_HOST_ The host or user argument to GRANT is too long
­1146 ER_NO_SUCH_TABLE

­1147 ER_NONEXISTING_TABLE
­1148 ER_NOT_ALLOWED_COMMA The used command is not allowed with this MySQL

Table '%s.%s' doesn't exist
There is no such grant defined for user '%s' on host
'%s' on table '%s'

version

­1149 ER_SYNTAX_ERROR

Error Architecture ­ 

You have an error in your SQL syntax; check the
manual that corresponds to your MySQL server
version

­1150 ER_DELAYED_CANT_CHAN Delayed insert thread couldn't get requested lock for
­1151 ER_TOO_MANY_DELAYED_
­1152 ER_ABORTING_CONNECTI
­1153 ER_NET_PACKET_TOO_LA
­1154 ER_NET_READ_ERROR_FR
­1155 ER_NET_FCNTL_ERROR
­1156 ER_NET_PACKETS_OUT_O
­1157 ER_NET_UNCOMPRESS_ER
­1158 ER_NET_READ_ERROR
­1159 ER_NET_READ_INTERRUP
­1160 ER_NET_ERROR_ON_WRIT
­1161 ER_NET_WRITE_INTERRU

table %s
Too many delayed threads in use
Aborted connection %ld to db: '%s' user: '%s' (%s
Got a packet bigger than 'max_allowed_packet' bytes
Got a read error from the connection pipe
Got an error from fcntl(
Got packets out of order
Couldn't uncompress communication packet
Got an error reading communication packets
Got timeout reading communication packets
Got an error writing communication packets
Got timeout writing communication packets
Result string is longer than 'max_allowed_packet'
bytes
The used table type doesn't support BLOB/TEXT
columns
The used table type doesn't support
AUTO_INCREMENT columns
INSERT DELAYED can't be used with table '%s'
because it is locked with LOCK TABLES

­1162 ER_TOO_LONG_STRING

­1163 ER_TABLE_CANT_HANDLE

­1164 ER_TABLE_CANT_HANDLE

­1165 ER_DELAYED_INSERT_TA

­1166 ER_WRONG_COLUMN_NAME Incorrect column name '%s'
­1167 ER_WRONG_KEY_COLUMN The used storage engine can't index column '%s'

­1168 ER_WRONG_MRG_TABLE

­1169 ER_DUP_UNIQUE

­1170 ER_BLOB_KEY_WITHOUT_

­1171 ER_PRIMARY_CANT_HAVE

­1172 ER_TOO_MANY_ROWS
­1173 ER_REQUIRES_PRIMARY_

­1174 ER_NO_RAID_COMPILED

­1175 ER_UPDATE_WITHOUT_KE

­1176 ER_KEY_DOES_NOT_EXIT
­1177 ER_CHECK_NO_SUCH_TAB
­1178 ER_CHECK_NOT_IMPLEME

­1179 ER_CANT_DO_THIS_DURI

Unable to open underlying table which is differently
defined or of non­MyISAM type or doesn't exist
Can't write, because of unique constraint, to table
'%s'
BLOB/TEXT column '%s' used in key specification
without a key length
All parts of a PRIMARY KEY must be NOT NULL;
if you need NULL in a key, use UNIQUE instead
Result consisted of more than one row
This table type requires a primary key
This version of MySQL is not compiled with RAID
support
You are using safe update mode and you tried to
update a table without a WHERE that uses a KEY
colum
Key '%s' doesn't exist in table '%s'
Can't open table
The storage engine for the table doesn't support %s
You are not allowed to execute this command in a
transaction

Got error %d during ROLLBACK
Got error %d during FLUSH_LOGS
Got error %d during CHECKPOINT

'%s' (%s

­1180 ER_ERROR_DURING_COMM Got error %d during COMMIT
­1181 ER_ERROR_DURING_ROLL
­1182 ER_ERROR_DURING_FLUS
­1183 ER_ERROR_DURING_CHEC
­1184 ER_NEW_ABORTING_CONN Aborted connection %ld to db: '%s' user: '%s' host:
­1185 ER_DUMP_NOT_IMPLEMEN The storage engine for the table does not support
­1186 ER_FLUSH_MASTER_BINL
­1187 ER_INDEX_REBUILD
­1188 ER_MASTER
­1189 ER_MASTER_NET_READ
­1190 ER_MASTER_NET_WRITE

binary table dump
Binlog closed, cannot RESET MASTER
Failed rebuilding the index of dumped table '%s'
Error from master: '%s'
Net error reading from master
Net error writing to master
Can't find FULLTEXT index matching the column
list
Can't execute the given command because you have
active locked tables or an active transaction

­1191 ER_FT_MATCHING_KEY_N

­1192 ER_LOCK_OR_ACTIVE_TR

­1193 ER_UNKNOWN_SYSTEM_VA Unknown system variable '%s'

­1194 ER_CRASHED_ON_USAGE

­1195 ER_CRASHED_ON_REPAIR

Table '%s' is marked as crashed and should be
repaired
Table '%s' is marked as crashed and last (automatic?)
repair failed

Error Architecture ­ 

­1202 ER_SLAVE_THREAD
­1203 ER_TOO_MANY_USER_CON User %s already has more than
­1204 ER_SET_CONSTANTS_ONL

­1196 ER_WARNING_NOT_COMPL

­1197 ER_TRANS_CACHE_FULL

­1198 ER_SLAVE_MUST_STOP

­1199 ER_SLAVE_NOT_RUNNING

­1200 ER_BAD_SLAVE

­1201 ER_MASTER_INFO

­1205 ER_LOCK_WAIT_TIMEOUT

­1206 ER_LOCK_TABLE_FULL

­1207 ER_READ_ONLY_TRANSAC

­1208 ER_DROP_DB_WITH_READ

­1209 ER_CREATE_DB_WITH_RE

­1210 ER_WRONG_ARGUMENTS
­1211 ER_NO_PERMISSION_TO_

­1212 ER_UNION_TABLES_IN_D

­1213 ER_LOCK_DEADLOCK

­1214 ER_TABLE_CANT_HANDLE

Some non­transactional changed tables couldn't be
rolled back
Multi­statement transaction required more than
'max_binlog_cache_size' bytes of storage; increase th
This operation cannot be performed with a running
slave; run STOP SLAVE first
This operation requires a running slave; configure
slave and do START SLAVE
The server is not configured as slave; fix in config
file or with CHANGE MASTER TO
Could not initialize master info structure; more error
messages can be found in the MySQL error log
Could not create slave thread; check system
resources

'max_user_connections' active connections
You may only use constant expressions with SET
Lock wait timeout exceeded; try restarting
transaction
The total number of locks exceeds the lock table size
Update locks cannot be acquired during a READ
UNCOMMITTED transaction
DROP DATABASE not allowed while thread is
holding global read lock
CREATE DATABASE not allowed while thread is
holding global read lock
Incorrect arguments to %s
'%s'@'%s' is not allowed to create new users
Incorrect table definition; all MERGE tables must be
in the same database
Deadlock found when trying to get lock; try
restarting transaction
The used table type doesn't support FULLTEXT
indexes
Cannot add foreign key constraint

­1217 ER_ROW_IS_REFERENCED

­1215 ER_CANNOT_ADD_FOREIG
­1216 ER_NO_REFERENCED_ROW Cannot add or update a child row: a foreign key

constraint fails
Cannot delete or update a parent row: a foreign key
constraint fails
Error connecting to master: %s
Error running query on master: %s
Error when executing command %s: %s
Incorrect usage of %s and %s

­1218 ER_CONNECT_TO_MASTER
­1219 ER_QUERY_ON_MASTER
­1220 ER_ERROR_WHEN_EXECUT
­1221 ER_WRONG_USAGE
­1222 ER_WRONG_NUMBER_OF_C The used SELECT statements have a different

number of columns
Can't execute the query because you have a
conflicting read lock

­1223 ER_CANT_UPDATE_WITH_
­1224 ER_MIXING_NOT_ALLOWE Mixing of transactional and non­transactional tables
­1225 ER_DUP_ARGUMENT

­1226 ER_USER_LIMIT_REACHE

­1227 ER_SPECIFIC_ACCESS_D

­1228 ER_LOCAL_VARIABLE

­1229 ER_GLOBAL_VARIABLE

­1236 ER_MASTER_FATAL_ERRO

­1237 ER_SLAVE_IGNORED_TAB

­1238 ER_INCORRECT_GLOBAL_
­1239 ER_WRONG_FK_DEF

is disabled
Option '%s' used twice in statement
User '%s' has exceeded the '%s' resource (current
value: %ld
Access denied; you need (at least one of) the %s
privilege(s) for this operation
Variable '%s' is a SESSION variable and can't be
used with SET GLOBAL
Variable '%s' is a GLOBAL variable and should be
set with SET GLOBAL
Variable '%s' doesn't have a default value

Incorrect argument type to variable '%s'
Variable '%s' can only be set, not read
Incorrect usage/placement of '%s'
This version of MySQL doesn't yet support '%s'
Got fatal error %d from master when reading data
from binary log: '%s'
Slave SQL thread ignored the query because of
replicate­*­table rules
Variable '%s' is a %s variable
Incorrect foreign key definition for '%s': %s

­1230 ER_NO_DEFAULT
­1231 ER_WRONG_VALUE_FOR_V Variable '%s' can't be set to the value of '%s'
­1232 ER_WRONG_TYPE_FOR_VA
­1233 ER_VAR_CANT_BE_READ
­1234 ER_CANT_USE_OPTION_H
­1235 ER_NOT_SUPPORTED_YET

Error Architecture ­ 

Key reference and table reference don't match
Operand should contain %d column(s)

­1240 ER_KEY_REF_DO_NOT_MA
­1241 ER_OPERAND_COLUMNS
­1242 ER_SUBQUERY_NO_1_ROW Subquery returns more than 1 row
­1243 ER_UNKNOWN_STMT_HAND Unknown prepared statement handler (%.*s) given
­1244 ER_CORRUPT_HELP_DB
­1245 ER_CYCLIC_REFERENCE
­1246 ER_AUTO_CONVERT
­1247 ER_ILLEGAL_REFERENCE
­1248 ER_DERIVED_MUST_HAVE
­1249 ER_SELECT_REDUCED

to %s
Help database is corrupt or does not exist
Cyclic reference on subqueries
Converting column '%s' from %s to %s
Reference '%s' not supported (%s
Every derived table must have its own alias
Select %u was reduced during optimization
Table '%s' from one of the SELECTs cannot be used
in %s
Client does not support authentication protocol
requested by server; consider upgrading MySQL
client
All parts of a SPATIAL index must be NOT NULL
COLLATION '%s' is not valid for CHARACTER
SET '%s'
Slave is already running
Slave already has been stopped

­1250 ER_TABLENAME_NOT_ALL

­1251 ER_NOT_SUPPORTED_AUT

­1252 ER_SPATIAL_CANT_HAVE

­1253 ER_COLLATION_CHARSET

­1254 ER_SLAVE_WAS_RUNNING
­1255 ER_SLAVE_WAS_NOT_RUN
­1256 ER_TOO_BIG_FOR_UNCOM Uncompressed data size too large; the maximum size
­1257 ER_ZLIB_Z_MEM_ERROR

­1258 ER_ZLIB_Z_BUF_ERROR

is %d (probably, length of uncompressed data was
ZLIB: Not enough memory
ZLIB: Not enough room in the output buffer
(probably, length of uncompressed data was
corrupted
ZLIB: Input data corrupted
Row %u was cut by GROUP_CONCAT(

­1259 ER_ZLIB_Z_DATA_ERROR
­1260 ER_CUT_VALUE_GROUP_C
­1261 ER_WARN_TOO_FEW_RECO Row %ld doesn't contain data for all columns
­1262 ER_WARN_TOO_MANY_REC Row %ld was truncated; it contained more data than
­1263 ER_WARN_NULL_TO_NOTN Column set to default value; NULL supplied to NOT
­1264 ER_WARN_DATA_OUT_OF_
­1265 WARN_DATA_TRUNCATED
­1266 ER_WARN_USING_OTHER_

there were input columns

NULL column '%s' at row %ld
Out of range value for column '%s' at row %ld
Data truncated for column '%s' at row %ld
Using storage engine %s for table '%s'
Illegal mix of collations (%s,%s) and (%s,%s) for
operation '%s'
Cannot drop one or more of the requested users
Can't revoke all privileges for one or more of the
requested users
Illegal mix of collations (%s,%s), (%s,%s), (%s,%s)
for operation '%s'
Illegal mix of collations for operation '%s'
Variable '%s' is not a variable component (can't be
used as XXXX.variable_name

­1267 ER_CANT_AGGREGATE_2C

­1268 ER_DROP_USER

­1269 ER_REVOKE_GRANTS

­1270 ER_CANT_AGGREGATE_3C

­1271 ER_CANT_AGGREGATE_NC

­1272 ER_VARIABLE_IS_NOT_S

­1273 ER_UNKNOWN_COLLATION Unknown collation: '%s'

­1274 ER_SLAVE_IGNORED_SSL

­1275 ER_SERVER_IS_IN_SECU

­1276 ER_WARN_FIELD_RESOLV

­1277 ER_BAD_SLAVE_UNTIL_C

­1278 ER_MISSING_SKIP_SLAV

­1279 ER_UNTIL_COND_IGNORE

SSL parameters in CHANGE MASTER are ignored
because this MySQL slave was compiled without
SSL suppor
Server is running in ­­secure­auth mode, but
'%s'@'%s' has a password in the old format; please
chan
Field or reference '%s%s%s%s%s' of SELECT #%d
was resolved in SELECT #%d
Incorrect parameter or combination of parameters for
START SLAVE UNTIL
It is recommended to use ­­skip­slave­start when
doing step­by­step replication with START SLAVE
UNT
SQL thread is not to be started so UNTIL options are
ignored

­1280 ER_WRONG_NAME_FOR_IN Incorrect index name '%s'
­1281 ER_WRONG_NAME_FOR_CA Incorrect catalog name '%s'

­1282 ER_WARN_QC_RESIZE

­1283 ER_BAD_FT_COLUMN
­1284 ER_UNKNOWN_KEY_CACHE Unknown key cache '%s'

Query cache failed to set size %lu; new query cache
size is %lu
Column '%s' cannot be part of FULLTEXT index

­1285 ER_WARN_HOSTNAME_WON MySQL is started in ­­skip­name­resolve mode; you

Error Architecture ­ 

must restart it without this switch for this grant

­1286 ER_UNKNOWN_STORAGE_E Unknown storage engine '%s'

­1287 ER_WARN_DEPRECATED_S

­1288 ER_NON_UPDATABLE_TAB

­1289 ER_FEATURE_DISABLED

­1290 ER_OPTION_PREVENTS_S

'%s' is deprecated and will be removed in a future
release. Please use %s instead
The target table %s of the %s is not updatable
The '%s' feature is disabled; you need MySQL built
with '%s' to have it working
The MySQL server is running with the %s option so
it cannot execute this statement
Column '%s' has duplicated value '%s' in %s

­1291 ER_DUPLICATED_VALUE_
­1292 ER_TRUNCATED_WRONG_V Truncated incorrect %s value: '%s'

­1294 ER_INVALID_ON_UPDATE

­1293 ER_TOO_MUCH_AUTO_TIM

Incorrect table definition; there can be only one
TIMESTAMP column with
CURRENT_TIMESTAMP in DEFAULT
Invalid ON UPDATE clause for '%s' column
This command is not supported in the prepared
statement protocol yet
Got error %d '%s' from %s
­1296 ER_GET_ERRMSG
­1297 ER_GET_TEMPORARY_ERR
Got temporary error %d '%s' from %s
­1298 ER_UNKNOWN_TIME_ZONE Unknown or incorrect time zone: '%s'

­1295 ER_UNSUPPORTED_PS

­1299 ER_WARN_INVALID_TIME

Invalid TIMESTAMP value in column '%s' at
row %ld
Invalid %s character string: '%s'

­1300 ER_INVALID_CHARACTER
­1301 ER_WARN_ALLOWED_PACK Result of %s() was larger than max_allowed_packet
­1302 ER_CONFLICTING_DECLA
­1303 ER_SP_NO_RECURSIVE_C
­1304 ER_SP_ALREADY_EXISTS
­1305 ER_SP_DOES_NOT_EXIST
­1306 ER_SP_DROP_FAILED
­1307 ER_SP_STORE_FAILED
­1308 ER_SP_LILABEL_MISMAT
­1309 ER_SP_LABEL_REDEFINE
­1310 ER_SP_LABEL_MISMATCH
­1311 ER_SP_UNINIT_VAR

­1312 ER_SP_BADSELECT

­1313 ER_SP_BADRETURN
­1314 ER_SP_BADSTATEMENT

­1315 ER_UPDATE_LOG_DEPREC

­1316 ER_UPDATE_LOG_DEPREC

­1317 ER_QUERY_INTERRUPTED

­1318 ER_SP_WRONG_NO_OF_AR

(%ld) ­ truncated
Conflicting declarations: '%s%s' and '%s%s'
Can't create a %s from within another stored routine
%s %s already exists
%s %s does not exist
Failed to DROP %s %s
Failed to CREATE %s %s
%s with no matching label: %s
Redefining label %s
End­label %s without match
Referring to uninitialized variable %s
PROCEDURE %s can't return a result set in the
given context
RETURN is only allowed in a FUNCTION
%s is not allowed in stored procedures
The update log is deprecated and replaced by the
binary log; SET SQL_LOG_UPDATE has been
ignored. Th
The update log is deprecated and replaced by the
binary log; SET SQL_LOG_UPDATE has been
translated
Query execution was interrupted
Incorrect number of arguments for %s %s;
expected %u, got %u
Undefined CONDITION: %s
No RETURN found in FUNCTION %s
FUNCTION %s ended without RETURN
Cursor statement must be a SELECT
Cursor SELECT must not have INTO
Undefined CURSOR: %s
Cursor is already open
Cursor is not open
Undeclared variable: %s
Incorrect number of FETCH variables
No data ­ zero rows fetched, selected, or processed
Duplicate parameter: %s
Duplicate variable: %s
Duplicate condition: %s
Duplicate cursor: %s
Failed to ALTER %s %s
Subquery value not supported

­1319 ER_SP_COND_MISMATCH
­1320 ER_SP_NORETURN
­1321 ER_SP_NORETURNEND
­1322 ER_SP_BAD_CURSOR_QUE
­1323 ER_SP_BAD_CURSOR_SEL
­1324 ER_SP_CURSOR_MISMATC
­1325 ER_SP_CURSOR_ALREADY
­1326 ER_SP_CURSOR_NOT_OPE
­1327 ER_SP_UNDECLARED_VAR
­1328 ER_SP_WRONG_NO_OF_FE
­1329 ER_SP_FETCH_NO_DATA
­1330 ER_SP_DUP_PARAM
­1331 ER_SP_DUP_VAR
­1332 ER_SP_DUP_COND
­1333 ER_SP_DUP_CURS
­1334 ER_SP_CANT_ALTER
­1335 ER_SP_SUBSELECT_NYI
­1336 ER_STMT_NOT_ALLOWED_ %s is not allowed in stored function or trigger

Error Architecture ­ 

­1337 ER_SP_VARCOND_AFTER_

­1338 ER_SP_CURSOR_AFTER_H
­1339 ER_SP_CASE_NOT_FOUND
­1340 ER_FPARSER_TOO_BIG_F
­1341 ER_FPARSER_BAD_HEADE
­1342 ER_FPARSER_EOF_IN_CO
­1343 ER_FPARSER_ERROR_IN_

­1344 ER_FPARSER_EOF_IN_UN

­1345 ER_VIEW_NO_EXPLAIN

­1346 ER_FRM_UNKNOWN_TYPE
­1347 ER_WRONG_OBJECT
­1348 ER_NONUPDATEABLE_COL

­1349 ER_VIEW_SELECT_DERIV

­1350 ER_VIEW_SELECT_CLAUS
­1351 ER_VIEW_SELECT_VARIA
­1352 ER_VIEW_SELECT_TMPTA

­1353 ER_VIEW_WRONG_LIST

Variable or condition declaration after cursor or
handler declaration
Cursor declaration after handler declaration
Case not found for CASE statement
Configuration file '%s' is too big
Malformed file type header in file '%s'
Unexpected end of file while parsing comment '%s'
Error while parsing parameter '%s' (line: '%s'
Unexpected end of file while skipping unknown
parameter '%s'
EXPLAIN/SHOW can not be issued; lacking
privileges for underlying table
File '%s' has unknown type '%s' in its header
'%s.%s' is not %s
Column '%s' is not updatable
View's SELECT contains a subquery in the FROM
clause
View's SELECT contains a '%s' clause
View's SELECT contains a variable or parameter
View's SELECT refers to a temporary table '%s'
View's SELECT and view's field list have different
column counts
View merge algorithm can't be used here for now
(assumed undefined algorithm

­1354 ER_WARN_VIEW_MERGE
­1355 ER_WARN_VIEW_WITHOUT View being updated does not have complete key of

­1356 ER_VIEW_INVALID

­1357 ER_SP_NO_DROP_SP

underlying table in it
View '%s.%s' references invalid table(s) or column(s)
or function(s) or definer/invoker of view lack
Can't drop or alter a %s from within another stored
routine
GOTO is not allowed in a stored procedure handler
Trigger already exists
Trigger does not exist
Trigger's '%s' is view or temporary table
Updating of %s row is not allowed in %strigger
There is no %s row in %s trigger
Field '%s' doesn't have a default value
Division by 0

­1358 ER_SP_GOTO_IN_HNDLR
­1359 ER_TRG_ALREADY_EXIST
­1360 ER_TRG_DOES_NOT_EXIS
­1361 ER_TRG_ON_VIEW_OR_TE
­1362 ER_TRG_CANT_CHANGE_R
­1363 ER_TRG_NO_SUCH_ROW_I
­1364 ER_NO_DEFAULT_FOR_FI
­1365 ER_DIVISION_BY_ZERO
­1366 ER_TRUNCATED_WRONG_V Incorrect %s value: '%s' for column '%s' at row %ld
­1367 ER_ILLEGAL_VALUE_FOR
­1368 ER_VIEW_NONUPD_CHECK CHECK OPTION on non­updatable view '%s.%s'
­1369 ER_VIEW_CHECK_FAILED

­1370 ER_PROCACCESS_DENIED

­1371 ER_RELAY_LOG_FAIL

­1372 ER_PASSWD_LENGTH

­1373 ER_UNKNOWN_TARGET_BI
­1374 ER_IO_ERR_LOG_INDEX_
­1375 ER_BINLOG_PURGE_PROH
­1376 ER_FSEEK_FAIL
­1377 ER_BINLOG_PURGE_FATA
­1378 ER_LOG_IN_USE
­1379 ER_LOG_PURGE_UNKNOWN Unknown error during log purge
­1380 ER_RELAY_LOG_INIT
­1381 ER_NO_BINARY_LOGGING

Illegal %s '%s' value found during parsing

CHECK OPTION failed '%s.%s'
%s command denied to user '%s'@'%s' for routine
'%s'
Failed purging old relay logs: %s
Password hash should be a %d­digit hexadecimal
number
Target log not found in binlog index
I/O error reading log index file
Server configuration does not permit binlog purge
Failed on fseek(
Fatal error during log purge
A purgeable log is in use, will not purge

Failed initializing relay log position: %s
You are not using binary logging
The '%s' syntax is reserved for purposes internal to
the MySQL server
WSAStartup Failed
Can't handle procedures with different groups yet
Select must have a group with this procedure
Can't use ORDER clause with this procedure
Binary logging and replication forbid changing the
global server %s
Can't map file: %s, errno: %d
Wrong magic in %s

­1382 ER_RESERVED_SYNTAX

­1383 ER_WSAS_FAILED
­1384 ER_DIFF_GROUPS_PROC
­1385 ER_NO_GROUP_FOR_PROC
­1386 ER_ORDER_WITH_PROC

­1387 ER_LOGGING_PROHIBIT_

­1388 ER_NO_FILE_MAPPING
­1389 ER_WRONG_MAGIC

Error Architecture ­ 

­1390 ER_PS_MANY_PARAM
­1391 ER_KEY_PART_0
­1392 ER_VIEW_CHECKSUM

­1393 ER_VIEW_MULTIUPDATE

­1394 ER_VIEW_NO_INSERT_FI

­1395 ER_VIEW_DELETE_MERGE
­1396 ER_CANNOT_USER
­1397 ER_XAER_NOTA

­1398 ER_XAER_INVAL

­1399 ER_XAER_RMFAIL

­1400 ER_XAER_OUTSIDE

­1401 ER_XAER_RMERR

­1402 ER_XA_RBROLLBACK

­1403 ER_NONEXISTING_PROC_

­1404 ER_PROC_AUTO_GRANT_F

­1405 ER_PROC_AUTO_REVOKE_
­1406 ER_DATA_TOO_LONG
­1407 ER_SP_BAD_SQLSTATE

­1408 ER_STARTUP

­1409 ER_LOAD_FROM_FIXED_S

­1410 ER_CANT_CREATE_USER_
­1411 ER_WRONG_VALUE_FOR_T
­1412 ER_TABLE_DEF_CHANGED
­1413 ER_SP_DUP_HANDLER

­1414 ER_SP_NOT_VAR_ARG

­1415 ER_SP_NO_RETSET

­1416 ER_CANT_CREATE_GEOME

­1417 ER_FAILED_ROUTINE_BR

­1418 ER_BINLOG_UNSAFE_ROU

­1419 ER_BINLOG_CREATE_ROU

­1420 ER_EXEC_STMT_WITH_OP

Prepared statement contains too many placeholders
Key part '%s' length cannot be 0
View text checksum failed
Can not modify more than one base table through a
join view '%s.%s'
Can not insert into join view '%s.%s' without fields
list
Can not delete from join view '%s.%s'
Operation %s failed for %s
XAER_NOTA: Unknown XID
XAER_INVAL: Invalid arguments (or unsupported
command
XAER_RMFAIL: The command cannot be executed
when global transaction is in the %s state
XAER_OUTSIDE: Some work is done outside
global transaction
XAER_RMERR: Fatal error occurred in the
transaction branch ­ check your data for consistency
XA_RBROLLBACK: Transaction branch was rolled
back
There is no such grant defined for user '%s' on host
'%s' on routine '%s'
Failed to grant EXECUTE and ALTER ROUTINE
privileges
Failed to revoke all privileges to dropped routine
Data too long for column '%s' at row %ld
Bad SQLSTATE: '%s'
%s: ready for connections. Version: '%s' socket: '%s'
port: %d %s
Can't load value from file with fixed size rows to
variable
You are not allowed to create a user with GRANT
Incorrect %s value: '%s' for function %s
Table definition has changed, please retry transaction
Duplicate handler declared in the same block
OUT or INOUT argument %d for routine %s is not a
variable or NEW pseudo­variable in BEFORE trigger
Not allowed to return a result set from a %s
Cannot get geometry object from data you send to
the GEOMETRY field
A routine failed and has neither NO SQL nor
READS SQL DATA in its declaration and binary
logging is
This function has none of DETERMINISTIC, NO
SQL, or READS SQL DATA in its declaration and
binary log
You do not have the SUPER privilege and binary
logging is enabled (you *might* want to use the less
You can't execute a prepared statement which has an
open cursor associated with it. Reset the statem
The statement (%lu) has no open cursor.

­1423 ER_NO_DEFAULT_FOR_VI

­1421 ER_STMT_HAS_NO_OPEN_
­1422 ER_COMMIT_NOT_ALLOWE Explicit or implicit commit is not allowed in stored
function or trigger.
Field of view '%s.%s' underlying table doesn't have a
default value
Recursive stored functions and triggers are not
allowed.
Too big scale %d specified for column '%s'.
Maximum is %lu.
Too big precision %d specified for column '%s'.
Maximum is %lu.
For float(M,D), double(M,D) or decimal(M,D), M
must be >= D (column '%s'),

­1427 ER_M_BIGGER_THAN_D
­1428 ER_WRONG_LOCK_OF_SYS You can't combine write­locking of system tables
­1429 ER_CONNECT_TO_FOREIG

with other tables or lock types
Unable to connect to foreign data source: %s
There was a problem processing the query on the
foreign data source. Data source error: %s
The foreign data source you are trying to reference
does not exist. Data source error: %s

­1424 ER_SP_NO_RECURSION

­1425 ER_TOO_BIG_SCALE

­1426 ER_TOO_BIG_PRECISION

­1430 ER_QUERY_ON_FOREIGN_

­1431 ER_FOREIGN_DATA_SOUR

­1432 ER_FOREIGN_DATA_STRI

­1433 ER_FOREIGN_DATA_STRI

­1434 ER_CANT_CREATE_FEDER

­1435 ER_TRG_IN_WRONG_SCHE

­1436 ER_STACK_OVERRUN_NEE

­1437 ER_TOO_LONG_BODY
­1438 ER_WARN_CANT_DROP_DE

­1439 ER_TOO_BIG_DISPLAYWI

­1440 ER_XAER_DUPID
­1441 ER_DATETIME_FUNCTION

­1442 ER_CANT_UPDATE_USED_

­1443 ER_VIEW_PREVENT_UPDA

­1444 ER_PS_NO_RECURSION

­1445 ER_SP_CANT_SET_AUTOC

Error Architecture ­ 

Can't create federated table. The data source
connection string '%s' is not in the correct format
The data source connection string '%s' is not in the
correct format
Can't create federated table. Foreign data src
error: %s
Trigger in wrong schema
Thread stack overrun: %ld bytes used of a %ld byte
stack, and %ld bytes needed. Use 'mysqld ­­thread
Routine body for '%s' is too long
Cannot drop default keycache
Display width out of range for column '%s' (max
= %lu
XAER_DUPID: The XID already exists
Datetime function: %s field overflow
Can't update table '%s' in stored function/trigger
because it is already used by statement which inv
The definition of table '%s' prevents operation %s on
table '%s'.
The prepared statement contains a stored routine call
that refers to that same statement. It's not a
Not allowed to set autocommit from a stored function
or trigger

­1446 ER_MALFORMED_DEFINER Definer is not fully qualified

­1447 ER_VIEW_FRM_NO_USER

­1448 ER_VIEW_OTHER_USER

­1449 ER_NO_SUCH_USER

­1450 ER_FORBID_SCHEMA_CHA

View '%s'.'%s' has no definer information (old table
format). Current user is used as definer. Pleas
You need the SUPER privilege for creation view
with '%s'@'%s' definer
The user specified as a definer ('%s'@'%s') does not
exist
Changing schema from '%s' to '%s' is not allowed.
Cannot delete or update a parent row: a foreign key
constraint fails (%s

constraint fails (%s

­1456 ER_SP_RECURSION_LIMI

­1454 ER_TRG_NO_DEFINER

­1455 ER_OLD_FILE_FORMAT

­1457 ER_SP_PROC_TABLE_COR

­1458 ER_SP_WRONG_NAME

­1459 ER_TABLE_NEEDS_UPGRA

­1460 ER_SP_NO_AGGREGATE

­1461 ER_MAX_PREPARED_STMT

­1451 ER_ROW_IS_REFERENCED
­1452 ER_NO_REFERENCED_ROW Cannot add or update a child row: a foreign key
­1453 ER_SP_BAD_VAR_SHADOW Variable '%s' must be quoted with `...`, or renamed
No definer attribute for trigger '%s'.'%s'. The trigger
will be activated under the authorization of
'%s' has an old format, you should re­create the '%s'
object(s
Recursive limit %d (as set by the
max_sp_recursion_depth variable) was exceeded for
routine %s
Failed to load routine %s. The table mysql.proc is
missing, corrupt, or contains bad data (internal
Incorrect routine name '%s'
Table upgrade required. Please do "REPAIR TABLE
`%s`" or dump/reload to fix it!
AGGREGATE is not supported for stored functions
Can't create more than max_prepared_stmt_count
statements (current value: %lu
`%s`.`%s` contains view recursion
Non­grouping field '%s' is used in %s clause
The used table type doesn't support SPATIAL
indexes
Triggers can not be created on system tables
Leading spaces are removed from name '%s'
Failed to read auto­increment value from storage
engine
user name
host name
String '%s' is too long for %s (should be no longer
than %d
­1471 ER_NON_INSERTABLE_TA
The target table %s of the %s is not insertable­into
­1472 ER_ADMIN_WRONG_MRG_T Table '%s' is differently defined or of non­MyISAM
­1473 ER_TOO_HIGH_LEVEL_OF
­1474 ER_NAME_BECOMES_EMPT Name '%s' has become '
­1475 ER_AMBIGUOUS_FIELD_T

­1465 ER_NO_TRIGGERS_ON_SY
­1466 ER_REMOVED_SPACES

­1462 ER_VIEW_RECURSIVE
­1463 ER_NON_GROUPING_FIEL

type or doesn't exist
Too high level of nesting for select

­1464 ER_TABLE_CANT_HANDLE

­1467 ER_AUTOINC_READ_FAIL

­1468 ER_USERNAME
­1469 ER_HOSTNAME

­1470 ER_WRONG_STRING_LENG

First character of the FIELDS TERMINATED string
is ambiguous; please use non­optional and non­

Error Architecture ­ 

ER_WRONG_EXPR_IN_PARTITION_FUNC_ERROR.

­1476 ER_FOREIGN_SERVER_EX

­1477 ER_FOREIGN_SERVER_DO

­1478 ER_ILLEGAL_HA_CREATE

­1479 ER_PARTITION_REQUIRE

­1480 ER_PARTITION_WRONG_V

­1481 ER_PARTITION_MAXVALU

­1482 ER_PARTITION_SUBPART

­1483 ER_PARTITION_SUBPART

­1484 ER_PARTITION_WRONG_N

­1485 ER_PARTITION_WRONG_N

­1486 ER_CONST_EXPR_IN_PAR

­1487 ER_NO_CONST_EXPR_IN_

­1488 ER_FIELD_NOT_FOUND_P

­1489 ER_LIST_OF_FIELDS_ON

­1490 ER_INCONSISTENT_PART

­1491 ER_PARTITION_FUNC_NO
­1492 ER_PARTITIONS_MUST_B

­1493 ER_RANGE_NOT_INCREAS

­1494 ER_INCONSISTENT_TYPE

­1495 ER_MULTIPLE_DEF_CONS

­1496 ER_PARTITION_ENTRY_E

­1497 ER_MIX_HANDLER_ERROR

­1498 ER_PARTITION_NOT_DEF

­1499 ER_TOO_MANY_PARTITIO

­1500 ER_SUBPARTITION_ERRO

­1501 ER_CANT_CREATE_HANDL
­1502 ER_BLOB_FIELD_IN_PAR

­1503 ER_UNIQUE_KEY_NEED_A

­1504 ER_NO_PARTS_ERROR

­1505 ER_PARTITION_MGMT_ON

­1506 ER_FOREIGN_KEY_ON_PA

­1507 ER_DROP_PARTITION_NO

­1508 ER_DROP_LAST_PARTITI

­1509 ER_COALESCE_ONLY_ON_

­1510 ER_REORG_HASH_ONLY_O

­1511 ER_REORG_NO_PARAM_ER

­1512 ER_ONLY_ON_RANGE_LIS

­1513 ER_ADD_PARTITION_SUB

­1514 ER_ADD_PARTITION_NO_

empty
The foreign server, %s, you are trying to create
already exists.
The foreign server name you are trying to reference
does not exist. Data source error: %s
Table storage engine '%s' does not support the create
option '%s'
Syntax error: %s PARTITIONING requires definition
of VALUES %s for each partition
Only %s PARTITIONING can use VALUES %s in
partition definition
MAXVALUE can only be used in last partition
definition
Subpartitions can only be hash partitions and by key
Must define subpartitions on all partitions if on one
partition
Wrong number of partitions defined, mismatch with
previous setting
Wrong number of subpartitions defined, mismatch
with previous setting

Constant/Random expression in (sub)partitioning
function is not allowed

Expression in RANGE/LIST VALUES must be
constant
Field in list of fields for partition function not found
in table
List of fields is only allowed in KEY partitions
The partition info in the frm file is not consistent
with what can be written into the frm file
The %s function returns the wrong type
For %s partitions each partition must be defined
VALUES LESS THAN value must be strictly
increasing for each partition
VALUES value must be of same type as partition
function
Multiple definition of same constant in list
partitioning
Partitioning can not be used stand­alone in query
The mix of handlers in the partitions is not allowed in
this version of MySQL
For the partitioned engine it is necessary to define
all %s
Too many partitions (including subpartitions) were
defined
It is only possible to mix RANGE/LIST partitioning
with HASH/KEY partitioning for subpartitioning
Failed to create specific handler file
A BLOB field is not allowed in partition function
A %s must include all columns in the table's
partitioning function
Number of %s = 0 is not an allowed value
Partition management on a not partitioned table is not
possible
Foreign key clause is not yet supported in
conjunction with partitioning
Error in list of partitions to %s
Cannot remove all partitions, use DROP TABLE
instead
COALESCE PARTITION can only be used on
HASH/KEY partitions
REORGANIZE PARTITION can only be used to
reorganize partitions not to change their numbers
REORGANIZE PARTITION without parameters can
only be used on auto­partitioned tables using HASH
PARTI
%s PARTITION can only be used on RANGE/LIST
partitions
Trying to Add partition(s) with wrong number of
subpartitions
At least one partition must be added

At least one partition must be coalesced
­1515 ER_COALESCE_PARTITIO
More partitions to reorganize than there are partitions
­1516 ER_REORG_PARTITION_N
Duplicate partition name %s
­1517 ER_SAME_NAME_PARTITI
­1518 ER_NO_BINLOG_ERROR
It is not allowed to shut off binlog on this command
­1519 ER_CONSECUTIVE_REORG When reorganizing a set of partitions they must be in

Error Architecture ­ 

­1520 ER_REORG_OUTSIDE_RAN

­1521 ER_PARTITION_FUNCTIO

­1522 ER_PART_STATE_ERROR

­1523 ER_LIMITED_PART_RANG

­1524 ER_PLUGIN_IS_NOT_LOA
­1525 ER_WRONG_VALUE
­1526 ER_NO_PARTITION_FOR_
­1527 ER_FILEGROUP_OPTION_
­1528 ER_CREATE_FILEGROUP_
­1529 ER_DROP_FILEGROUP_FA

consecutive order
Reorganize of range partitions cannot change total
ranges except for last partition where it can ext
Partition function not supported in this version for
this handler
Partition state cannot be defined from
CREATE/ALTER TABLE
The %s handler only supports 32 bit integers in
VALUES
Plugin '%s' is not loaded
Incorrect %s value: '%s'
Table has no partition for value %s
It is not allowed to specify %s more than once
Failed to create %s
Failed to drop %s
The handler doesn't support autoextend of
tablespaces

­1532 ER_SIZE_OVERFLOW_ERR

­1530 ER_TABLESPACE_AUTO_E
­1531 ER_WRONG_SIZE_NUMBER A size parameter was incorrectly specified, either
number or on the form 10M
The size number was correct but we don't allow the
digit part to be more than 2 billion
Failed to alter: %s

­1533 ER_ALTER_FILEGROUP_F
­1534 ER_BINLOG_ROW_LOGGIN Writing one row to the row­based binary log failed
­1535 ER_BINLOG_ROW_WRONG_ Table definition on master and slave does not

­1547 ER_COL_COUNT_DOESNT_
­1548 ER_CANNOT_LOAD_FROM_ Cannot load from mysql.%s. The table is probably
­1549 ER_EVENT_CANNOT_DELE
­1550 ER_EVENT_COMPILE_ERR
­1551 ER_EVENT_SAME_NAME
­1552 ER_EVENT_DATA_TOO_LO

­1536 ER_BINLOG_ROW_RBR_TO

­1537 ER_EVENT_ALREADY_EXI

­1538 ER_EVENT_STORE_FAILE

­1539 ER_EVENT_DOES_NOT_EX
­1540 ER_EVENT_CANT_ALTER
­1541 ER_EVENT_DROP_FAILED
­1542 ER_EVENT_INTERVAL_NO
­1543 ER_EVENT_ENDS_BEFORE

­1544 ER_EVENT_EXEC_TIME_I

­1545 ER_EVENT_OPEN_TABLE_
­1546 ER_EVENT_NEITHER_M_E

­1553 ER_DROP_INDEX_FK

­1554 ER_WARN_DEPRECATED_S

­1555 ER_CANT_WRITE_LOCK_L

­1556 ER_CANT_LOCK_LOG_TAB

­1557 ER_FOREIGN_DUPLICATE

­1558 ER_COL_COUNT_DOESNT_

­1559 ER_TEMP_TABLE_PREVEN

­1560 ER_STORED_FUNCTION_P

match: %s
Slave running with ­­log­slave­updates must use row­
based binary logging to be able to replicate row
Event '%s' already exists
Failed to store event %s. Error code %d from storage
engine.
Unknown event '%s'
Failed to alter event '%s'
Failed to drop %s
INTERVAL is either not positive or too big
ENDS is either invalid or before STARTS
Event execution time is in the past. Event has been
disabled
Failed to open mysql.event
No datetime expression provided
Column count of mysql.%s is wrong. Expected %d,
found %d. The table is probably corrupted

corrupted
Failed to delete the event from mysql.event
Error during compilation of event's body
Same old and new event name
Data for column '%s' too long
Cannot drop index '%s': needed in a foreign key
constraint
The syntax '%s' is deprecated and will be removed in
MySQL %s. Please use %s instead
You can't write­lock a log table. Only read access is
possible
You can't use locks with log tables.
Upholding foreign key constraints for table '%s',
entry '%s', key %d would lead to a duplicate entry
Column count of mysql.%s is wrong. Expected %d,
found %d. Created with MySQL %d, now
running %d. Ple
Cannot switch out of the row­based binary log format
when the session has open temporary tables
Cannot change the binary logging format inside a
stored function or trigger
The NDB cluster engine does not support changing

­1561 ER_NDB_CANT_SWITCH_B

Error Architecture ­ 

­1562 ER_PARTITION_NO_TEMP
­1563 ER_PARTITION_CONST_D
­1564 ER_PARTITION_FUNCTIO
­1565 ER_DDL_LOG_ERROR

­1566 ER_NULL_IN_VALUES_LE

­1567 ER_WRONG_PARTITION_N

­1568 ER_CANT_CHANGE_TX_IS

­1569 ER_DUP_ENTRY_AUTOINC

­1570 ER_EVENT_MODIFY_QUEU

­1571 ER_EVENT_SET_VAR_ERR

­1572 ER_PARTITION_MERGE_E
­1573 ER_CANT_ACTIVATE_LOG
­1574 ER_RBR_NOT_AVAILABLE
­1575 ER_BASE64_DECODE_ERR

­1576 ER_EVENT_RECURSION_F

­1577 ER_EVENTS_DB_ERROR

­1578 ER_ONLY_INTEGERS_ALL
­1579 ER_UNSUPORTED_LOG_EN
­1580 ER_BAD_LOG_STATEMENT

the binlog format on the fly yet
Cannot create temporary table with partitions
Partition constant is out of partition function domain
This partition function is not allowed
Error in DDL log
Not allowed to use NULL value in VALUES LESS
THAN
Incorrect partition name
Transaction isolation level can't be changed while a
transaction is in progress
ALTER TABLE causes auto_increment
resequencing, resulting in duplicate entry '%s' for key
'%s'
Internal scheduler error %d
Error during starting/stopping of the scheduler. Error
code %u
Engine cannot be used in partitioned tables
Cannot activate '%s' log
The server was not built with row­based replication
Decoding of base64 string failed
Recursion of EVENT DDL statements is forbidden
when body is present
Cannot proceed because system tables used by Event
Scheduler were found damaged at server start
Only integers allowed as number here
This storage engine cannot be used for log tables"
You cannot '%s' a log table if logging is enabled
Cannot rename '%s'. When logging enabled, rename
to/from log table must rename two tables: the log t

­1581 ER_CANT_RENAME_LOG_T
­1582 ER_WRONG_PARAMCOUNT_ Incorrect parameter count in the call to native

To address this issue, try running mysql_upgrade.

The format string for this error is also used with ER_DUP_ENTRY.

­1585 ER_NATIVE_FCT_NAME_C

­1586 ER_DUP_ENTRY_WITH_KE

­1587 ER_BINLOG_PURGE_EMFI

­1588 ER_EVENT_CANNOT_CREA

­1589 ER_EVENT_CANNOT_ALTE

­1584 ER_WRONG_PARAMETERS_

­1583 ER_WRONG_PARAMETERS_

­1590 ER_SLAVE_INCIDENT
­1591 ER_NO_PARTITION_FOR_

function '%s'
Incorrect parameters in the call to native function
'%s'
Incorrect parameters in the call to stored function
'%s'
This function '%s' has the same name as a native
function
Duplicate entry '%s' for key '%s'
Too many files opened, please execute the command
again
Event execution time is in the past and ON
COMPLETION NOT PRESERVE is set. The event
was dropped imm
Event execution time is in the past and ON
COMPLETION NOT PRESERVE is set. The event
was dropped imm
The incident %s occured on the master. %s
Table has no partition for some existing values
Unsafe statement written to the binary log using
statement format since BINLOG_FORMAT =
STATEMENT. %
Fatal error: %s
­1593 ER_SLAVE_FATAL_ERROR
­1594 ER_SLAVE_RELAY_LOG_R
Relay log read failure: %s
­1595 ER_SLAVE_RELAY_LOG_W Relay log write failure: %s
­1596 ER_SLAVE_CREATE_EVEN
­1597 ER_SLAVE_MASTER_COM_ Master command %s failed: %s
Binary logging not possible. %s
­1598 ER_BINLOG_LOGGING_IM
­1599 ER_VIEW_NO_CREATION_
View `%s`.`%s` has no creation context
Creation context of view %s.%s is invalid
­1600 ER_VIEW_INVALID_CREA
Creation context of stored routine %s.%s is invalid
­1601 ER_SR_INVALID_CREATI
Corrupted TRG file for table `%s`.`%s`
­1602 ER_TRG_CORRUPTED_FIL
­1603 ER_TRG_NO_CREATION_C
Triggers for table `%s`.`%s` have no creation context
Trigger creation context of table `%s`.`%s` is invalid
­1604 ER_TRG_INVALID_CREAT
Creation context of event `%s`.`%s` is invalid
­1605 ER_EVENT_INVALID_CRE
Cannot open table for trigger `%s`.`%s`
­1606 ER_TRG_CANT_OPEN_TAB
­1607 ER_CANT_CREATE_SROUT
Cannot create stored routine `%s`. Check warnings

­1592 ER_BINLOG_UNSAFE_STA

Failed to create %s

­1608 ER_NEVER_USED

Ambiguous slave modes combination. %s

­1609 ER_NO_FORMAT_DESCRIP

­1610 ER_SLAVE_CORRUPT_EVE
­1611 ER_LOAD_DATA_INVALID
­1612 ER_LOG_PURGE_NO_FILE

­1613 ER_XA_RBTIMEOUT

­1614 ER_XA_RBDEADLOCK

­1615 ER_NEED_REPREPARE
­1616 ER_DELAYED_NOT_SUPPO
­1617 WARN_NO_MASTER_INFO
­1618 WARN_OPTION_IGNORED
­1619 WARN_PLUGIN_DELETE_B
­1620 WARN_PLUGIN_BUSY

­1621 ER_VARIABLE_IS_READO

­1622 ER_WARN_ENGINE_TRANS

­1623 ER_SLAVE_HEARTBEAT_F

­1624 ER_SLAVE_HEARTBEAT_V

­1625 ER_NDB_REPLICATION_S
­1626 ER_CONFLICT_FN_PARSE
­1627 ER_EXCEPTIONS_WRITE_
­1628 ER_TOO_LONG_TABLE_CO
­1629 ER_TOO_LONG_FIELD_CO

­1630 ER_FUNC_INEXISTENT_N

Error Architecture ­ 

The BINLOG statement of type `%s` was not
preceded by a format description BINLOG
statement.
Corrupted replication event was detected
Invalid column reference (%s) in LOAD DATA
Being purged log %s was not found
XA_RBTIMEOUT: Transaction branch was rolled
back: took too long
XA_RBDEADLOCK: Transaction branch was rolled
back: deadlock was detected
Prepared statement needs to be re­prepared
DELAYED option not supported for table '%s'
The master info structure does not exist
<%s> option ignored
Built­in plugins cannot be deleted
Plugin is busy and will be uninstalled on shutdown
%s variable '%s' is read­only. Use SET %s to assign
the value
Storage engine %s does not support rollback for this
statement. Transaction rolled back and must be
Unexpected master's heartbeat data: %s
The requested value for the heartbeat period is either
negative or exceeds the maximum allowed (%s s
Bad schema for mysql.ndb_replication table. %s
Error in parsing conflict function. %s
Write to exceptions table failed. %s"
Comment for table '%s' is too long (max = %lu
Comment for field '%s' is too long (max = %lu
FUNCTION %s does not exist. Check the 'Function
Name Parsing and Resolution' section in the
Referenc
Database
Table
Partition
Subpartition
Temporary
Renamed

­1631 ER_DATABASE_NAME
­1632 ER_TABLE_NAME
­1633 ER_PARTITION_NAME
­1634 ER_SUBPARTITION_NAME
­1635 ER_TEMPORARY_NAME
­1636 ER_RENAMED_NAME
­1637 ER_TOO_MANY_CONCURRE Too many active concurrent transactions

­1638 WARN_NON_ASCII_SEPAR

­1639 ER_DEBUG_SYNC_TIMEOU
­1640 ER_DEBUG_SYNC_HIT_LI
­1641 ER_DUP_SIGNAL_SET
­1642 ER_SIGNAL_WARN
­1643 ER_SIGNAL_NOT_FOUND
­1644 ER_SIGNAL_EXCEPTION
­1645 ER_RESIGNAL_WITHOUT_

­1646 ER_SIGNAL_BAD_CONDIT

Non­ASCII separator arguments are not fully
supported
debug sync point wait timed out
debug sync point hit limit reached
Duplicate condition information item '%s'
Unhandled user­defined warning condition
Unhandled user­defined not found condition
Unhandled user­defined exception condition
RESIGNAL when handler not active
SIGNAL/RESIGNAL can only use a CONDITION
defined with SQLSTATE

­1650 ER_SLAVE_IGNORE_SERV

­1647 WARN_COND_ITEM_TRUNC Data truncated for condition item '%s'
Data too long for condition item '%s'
­1648 ER_COND_ITEM_TOO_LON
­1649 ER_UNKNOWN_LOCALE
Unknown locale: '%s'
The requested server id %d clashes with the slave
startup option ­­replicate­same­server­id
Query cache is disabled; restart the server with
query_cache_type=1 to enable it
Duplicate partition field name '%s'
Inconsistency in usage of column lists for
partitioning

­1651 ER_QUERY_CACHE_DISAB

­1652 ER_SAME_NAME_PARTITI

­1653 ER_PARTITION_COLUMN_

­1654 ER_WRONG_TYPE_COLUMN Partition column values of incorrect type
­1655 ER_TOO_MANY_PARTITIO
­1656 ER_MAXVALUE_IN_VALUE

­1657 ER_TOO_MANY_VALUES_E

­1658 ER_ROW_SINGLE_PARTIT

­1659 ER_FIELD_TYPE_NOT_AL

Too many fields in '%s'
Cannot use MAXVALUE as value in VALUES IN
Cannot have more than one value for this type of %s
partitioning
Row expressions in VALUES IN only allowed for
multi­field column partitioning
Field '%s' is of a not allowed type for this type of

Error Architecture ­ 

­1660 ER_PARTITION_FIELDS_

­1661 ER_BINLOG_ROW_ENGINE

­1662 ER_BINLOG_ROW_MODE_A

­1663 ER_BINLOG_UNSAFE_AND

­1664 ER_BINLOG_ROW_INJECT

­1665 ER_BINLOG_STMT_MODE_

­1666 ER_BINLOG_ROW_INJECT

­1667 ER_BINLOG_MULTIPLE_E

­1668 ER_BINLOG_UNSAFE_LIM

­1669 ER_BINLOG_UNSAFE_INS

­1670 ER_BINLOG_UNSAFE_SYS

­1671 ER_BINLOG_UNSAFE_AUT

­1672 ER_BINLOG_UNSAFE_UDF

­1673 ER_BINLOG_UNSAFE_SYS

­1674 ER_BINLOG_UNSAFE_SYS

­1675 ER_BINLOG_UNSAFE_NON

­1676 ER_MESSAGE_AND_STATE

­1677 ER_SLAVE_CONVERSION_

­1678 ER_SLAVE_CANT_CREATE

­1679 ER_INSIDE_TRANSACTIO

­1680 ER_PATH_LENGTH

­1681 ER_WARN_DEPRECATED_S

­1682 ER_WRONG_NATIVE_TABL
­1683 ER_WRONG_PERFSCHEMA_

­1684 ER_WARN_I_S_SKIPPED_

­1685 ER_INSIDE_TRANSACTIO

­1686 ER_STORED_FUNCTION_P

­1687 ER_SPATIAL_MUST_HAVE

­1688 ER_TOO_LONG_INDEX_CO

­1689 ER_LOCK_ABORTED

­1690 ER_DATA_OUT_OF_RANGE

ER_BINLOG_MULTIPLE_ENGINES_AND_SELF_LOGGING_ENGINE was

partitioning
The total length of the partitioning fields is too large
Cannot execute statement: impossible to write to
Cannot execute statement: impossible to write to
binary log since BINLOG_FORMAT = ROW and at
least o
Cannot execute statement: impossible to write to
binary log since statement is unsafe, storage engin
Cannot execute statement: impossible to write to
binary log since statement is in row format and at
Cannot execute statement: impossible to write to
binary log since BINLOG_FORMAT =
STATEMENT and at l
Cannot execute statement: impossible to write to
Cannot execute statement: impossible to write to
binary log since more than one engine is involved a
The statement is unsafe because it uses a LIMIT
clause. This is unsafe because the set of rows inclu
The statement is unsafe because it uses INSERT
DELAYED. This is unsafe because the times when
rows a
The statement is unsafe because it uses the general
log, slow query log, or performance_schema table
Statement is unsafe because it invokes a trigger or a
stored function that inserts into an AUTO_INCR
Statement is unsafe because it uses a UDF which
may not return the same value on the slave.
Statement is unsafe because it uses a system variable
that may have a different value on the slave.
Statement is unsafe because it uses a system function
that may return a different value on the slave
Statement is unsafe because it accesses a non­
transactional table after accessing a transactional ta
%s Statement: %s
Column %d of table '%s.%s' cannot be converted
from type '%s' to type '%s'
Can't create conversion table for table '%s.%s'
Cannot modify @@session.binlog_format inside a
transaction
The path specified for %s is too long.
'%s' is deprecated and will be removed in a future
release.
Native table '%s'.'%s' has the wrong structure
Invalid performance_schema usage.
Table '%s'.'%s' was skipped since its definition is
being modified by concurrent DDL statement
Cannot modify
@@session.binlog_direct_non_transactional_updates
inside a transaction
Cannot change the binlog direct flag inside a stored
function or trigger
A SPATIAL index may only contain a geometrical
type column
Comment for index '%s' is too long (max = %lu
Wait on a lock was aborted due to a pending
exclusive lock
%s value is out of range in '%s'
A variable of a non­integer based type in LIMIT
clause

ER_INSIDE_TRANSACTION_PREVENTS_SWITCH_BINLOG_FORMAT was

ER_INSIDE_TRANSACTION_PREVENTS_SWITCH_BINLOG_DIRECT was

ER_STORED_FUNCTION_PREVENTS_SWITCH_BINLOG_DIRECT was added

­1693 ER_BINLOG_UNSAFE_MIX

­1691 ER_WRONG_SPVAR_TYPE_
­1692 ER_BINLOG_UNSAFE_MUL Mixing self­logging and non­self­logging engines in
a statement is unsafe.
Statement accesses nontransactional table as well as
transactional or temporary table, and writes to
Cannot modify @@session.sql_log_bin inside a
transaction
Cannot change the sql_log_bin inside a stored
function or trigger
Failed to read from the .par file

ER_INSIDE_TRANSACTION_PREVENTS_SWITCH_SQL_LOG_BIN was added
ER_STORED_FUNCTION_PREVENTS_SWITCH_SQL_LOG_BIN was added in

ER_BINLOG_UNSAFE_MULTIPLE_ENGINES_AND_SELF_LOGGING_ENGINE

­1696 ER_FAILED_READ_FROM_
­1697 ER_VALUES_IS_NOT_INT

­1695 ER_STORED_FUNCTION_P

­1694 ER_INSIDE_TRANSACTIO

­1710 ER_ERROR_IN_TRIGGER_
­1711 ER_ERROR_IN_UNKNOWN_ Unknown trigger has an error in its body: '%s'
­1712 ER_INDEX_CORRUPT
­1713 ER_UNDO_RECORD_TOO_B Undo log record is too big.

Index %s is corrupted

­1698 ER_ACCESS_DENIED_NO_

­1699 ER_SET_PASSWORD_AUTH

­1700 ER_GRANT_PLUGIN_USER

­1701 ER_TRUNCATE_ILLEGAL_

­1702 ER_PLUGIN_IS_PERMANE

­1703 ER_SLAVE_HEARTBEAT_V

­1704 ER_SLAVE_HEARTBEAT_V

­1705 ER_STMT_CACHE_FULL

­1706 ER_MULTI_UPDATE_KEY_

­1707 ER_TABLE_NEEDS_REBUI

­1708 WARN_OPTION_BELOW_LI

­1709 ER_INDEX_COLUMN_TOO_

­1714 ER_BINLOG_UNSAFE_INS

­1715 ER_BINLOG_UNSAFE_INS

­1716 ER_BINLOG_UNSAFE_REP

­1717 ER_BINLOG_UNSAFE_CRE

­1718 ER_BINLOG_UNSAFE_CRE

­1719 ER_BINLOG_UNSAFE_UPD

­1720 ER_PLUGIN_NO_UNINSTA

­1721 ER_PLUGIN_NO_INSTALL

­1722 ER_BINLOG_UNSAFE_WRI

­1723 ER_BINLOG_UNSAFE_CRE

­1724 ER_BINLOG_UNSAFE_INS

­1725 ER_TABLE_IN_FK_CHECK

­1726 ER_UNSUPPORTED_ENGIN

­1727 ER_BINLOG_UNSAFE_AUT

­2000 CR_UNKNOWN_ERROR
­2001 CR_SOCKET_CREATE_ERR

­2002 CR_CONNECTION_ERROR

Access denied for user '%s'@'%s'
SET PASSWORD has no significance for users
authenticating via plugins
GRANT with IDENTIFIED WITH is illegal because
the user %­.*s already exists
Cannot truncate a table referenced in a foreign key
constraint (%s
Plugin '%s' is force_plus_permanent and can not be
unloaded
The requested value for the heartbeat period is less
than 1 millisecond. The value is reset to 0, me
The requested value for the heartbeat period exceeds
the value of 'slave_net_timeout' seconds. A sen
Multi­row statements required more than
'max_binlog_stmt_cache_size' bytes of storage;
increase this
Primary key/partition key update is not allowed since
the table is updated both as '%s' and '%s'.
Table rebuild required. Please do "ALTER TABLE
`%s` FORCE" or dump/reload to fix it!
The value of '%s' should be no less than the value of
'%s'
Index column size too large. The maximum column
size is %lu bytes.
Trigger '%s' has an error in its body: '%s'

INSERT IGNORE... SELECT is unsafe because the
order in which rows are retrieved by the SELECT
determ
INSERT... SELECT... ON DUPLICATE KEY
UPDATE is unsafe because the order in which rows
are retrieved
REPLACE... SELECT is unsafe because the order in
which rows are retrieved by the SELECT determines
w
CREATE... IGNORE SELECT is unsafe because the
order in which rows are retrieved by the SELECT
determ
CREATE... REPLACE SELECT is unsafe because
the order in which rows are retrieved by the SELECT
deter
UPDATE IGNORE is unsafe because the order in
which rows are updated determines which (if any)
rows a
Plugin '%s' is marked as not dynamically
uninstallable. You have to stop the server to uninstall
it.
Plugin '%s' is marked as not dynamically installable.
You have to stop the server to install it.
Statements writing to a table with an auto­increment
column after selecting from another table are u
CREATE TABLE... SELECT... on a table with an
auto­increment column is unsafe because the order in
wh
INSERT... ON DUPLICATE KEY UPDATE on a
table with more than one UNIQUE KEY is unsafe
Table is being used in foreign key check.
Storage engine '%s' does not support system tables.
[%s.%s]
INSERT into autoincrement field which is not the
first part in the composed primary key is unsafe.
Unknown MySQL error
Can't create UNIX socket,'%d'
Can't connect to local MySQL server through socket
'%s','%d'
Can't connect to MySQL server on '%s','%d'
Can't create TCP/IP socket,'%d'
Unknown MySQL server host '%s','%d'

Error Architecture ­ 

­2003 CR_CONN_HOST_ERROR
­2004 CR_IPSOCK_ERROR
­2005 CR_UNKNOWN_HOST
­2006 CR_SERVER_GONE_ERROR MySQL server has gone away
­2007 CR_VERSION_ERROR

Protocol mismatch; server version = %d, client

Error Architecture ­ 

­2018 CR_NAMEDPIPESETSTATE

version = %d
MySQL client ran out of memory
Wrong host info
Localhost via UNIX socket
%s via TCP/IP
Error in server handshake
Lost connection to MySQL server during query

­2008 CR_OUT_OF_MEMORY
­2009 CR_WRONG_HOST_INFO
­2010 CR_LOCALHOST_CONNECT
­2011 CR_TCP_CONNECTION
­2012 CR_SERVER_HANDSHAKE_
­2013 CR_SERVER_LOST
­2014 CR_COMMANDS_OUT_OF_S Commands out of sync; you can't run this command
­2015 CR_NAMEDPIPE_CONNECT
­2016 CR_NAMEDPIPEWAIT_ERR
­2017 CR_NAMEDPIPEOPEN_ERR

now
Named pipe: %s
Can't wait for named pipe to host: %s pipe: %s,'%lu'
Can't open named pipe to host: %s pipe: %s,'%lu'
Can't set state of named pipe to host: %s
pipe: %s,'%lu'
Can't initialize character set %s,'path: %s'
­2019 CR_CANT_READ_CHARSET
Got packet bigger than 'max_allowed_packet' bytes
­2020 CR_NET_PACKET_TOO_LA
Embedded server
­2021 CR_EMBEDDED_CONNECTI
Error on SHOW SLAVE STATUS:
­2022 CR_PROBE_SLAVE_STATU
Error on SHOW SLAVE HOSTS:
­2023 CR_PROBE_SLAVE_HOSTS
­2024 CR_PROBE_SLAVE_CONNE
Error connecting to slave:
­2025 CR_PROBE_MASTER_CONN Error connecting to master:
­2026 CR_SSL_CONNECTION_ER
SSL connection error: %s
Malformed packet
­2027 CR_MALFORMED_PACKET
This client library is licensed only for use with
MySQL servers having '%s' license
Invalid use of null pointer
Statement not prepared
No data supplied for parameters in prepared
statement
Data truncated
No parameters exist in the statement
Invalid parameter number
Can't send long data for non­string/non­binary data
types,'parameter: %d'

­2032 CR_DATA_TRUNCATED
­2033 CR_NO_PARAMETERS_EXI
­2034 CR_INVALID_PARAMETER

­2029 CR_NULL_POINTER
­2030 CR_NO_PREPARE_STMT

­2031 CR_PARAMS_NOT_BOUND

­2035 CR_INVALID_BUFFER_US

­2028 CR_WRONG_LICENSE

­2036 CR_UNSUPPORTED_PARAM Using unsupported buffer type: %d,'parameter: %d'
­2037 CR_SHARED_MEMORY_CON Shared memory: %s
­2038 CR_SHARED_MEMORY_CON Can't open shared memory; client could not create
­2039 CR_SHARED_MEMORY_CON Can't open shared memory; no answer event received
­2040 CR_SHARED_MEMORY_CON Can't open shared memory; server could not allocate
­2041 CR_SHARED_MEMORY_CON Can't open shared memory; server could not get

request event,'%lu'

file mapping,'%lu'

from server,'%lu'

pointer to file mapping,'%lu'
Can't open shared memory; client could not allocate
file mapping,'%lu'

pointer to file mapping,'%lu'

­2042 CR_SHARED_MEMORY_FIL
­2043 CR_SHARED_MEMORY_MAP Can't open shared memory; client could not get
­2044 CR_SHARED_MEMORY_EVE Can't open shared memory; client could not
­2045 CR_SHARED_MEMORY_CON Can't open shared memory; no answer from
­2046 CR_SHARED_MEMORY_CON Can't open shared memory; cannot send request
­2047 CR_CONN_UNKNOW_PROTO Wrong or unknown protocol
­2048 CR_INVALID_CONN_HAND

create %s event,'%lu'

event to server,'%lu'

server,'%lu'

­2049 CR_SECURE_AUTH

­2050 CR_FETCH_CANCELED

­2051 CR_NO_DATA
­2052 CR_NO_STMT_METADATA

­2053 CR_NO_RESULT_SET

­2054 CR_NOT_IMPLEMENTED

­2055 CR_SERVER_LOST_EXTEN

Invalid connection handle
protocol refused, client option 'secure_auth' enable
Row retrieval was canceled by mysql_stmt_close()
call
Attempt to read column without prior row fetch
Prepared statement contains no metadata
Attempt to read a row while there is no result set
associated with the statement
This feature is not implemented yet
Lost connection to MySQL server at '%s', system
error: %d
Statement closed indirectly because of a

­2056 CR_STMT_CLOSED

Error Architecture ­ 

preceeding %s() call

­2057 CR_NEW_STMT_METADATA The number of columns in the result set differs from
the number of bound buffers. You must reset the
­2058 CR_ALREADY_CONNECTED This handle is already connected. Use a separate
handle for each connection.
­2059 CR_AUTH_PLUGIN_CANNO
Authentication plugin '%s' cannot be loaded: %s
Notify Error Codes

Notify
Code

Alias

Error

Explanation

­3000 NOTIFY_IGNORED

Notification for this event is ignored

­3001 NOTIFY_DISABLED
­3002 NOTIFY_INCOMPLETE

­3003 NOTIFY_NON_EXIST

­3004 NOTIFY_NO_MESSAGE

­3005 NOTIFY_NO_SUBJECT

­3006 NOTIFY_NO_TEMPLATE

­3007 NOTIFY_NO_DICTIONARY

­3008 NOTIFY_NO_GROUPMEMBE

­3009 NOTIFY_UNSUPPORTED_M

Notification type is disabled
Notification config is incomplete
Notification type indicated does not
exist
Notification config does not contain a
message
Notification config does not contain a
subject
Notification config does not contain a
template
Notification's substitution tag
dictionary does not exist
No members in notificant groups
found even though this event
exclusively signals members in a
group.
This notification medium is not
currently supported.

­3010 NOTIFY_ENTITY

Entity does not exists

­3011 NOTIFY_EVENT_NOT_NOTIFY Event type is not for notification
Login Error Codes

Notification for this event is ignored. This is most likely because the eventtype is
not defined in the table #_inno_system_picklist_event_types, because an event was
published that sis not need any notification processing.
The Notification type exists but it is disabled.
The subject line, the message content or the notificant details are missing.

The Notification type does not exist in the notification configuration.

The indicated Entity Id in the event does not exist in the substitution­tag data, as
determined by the substitution­tag data dictionary.
Event type is not for notification

Login
Code

Alias

­3100 LOGIN_GENERAL

­3101 LOGIN_INPROCESS_FAIL

­3102 LOGIN_DOMAIN_BAN

­3103 LOGIN_PLAN_NONEXIST

­3104 LOGIN_PLAN_EXISTS

­3105 LOGIN_SUBSCRIPTION_ID_INVALID

­3106 LOGIN_USER_DETAILS

­3107 LOGIN_USER_NONEXIST

Error Architecture ­ 

Error

General problem
with Registration,
Login, Password
Recovery,
Subscriptions
Registration
process failed

Registration
Banned Domain

Subscription Plan
does not exist
A different
subscription plan
for this
organizaton
already exists
Subcription Id
does not belong to
an existing
Organization
Insufficient details
provided.
User does not
exist

Explanation

General problem with Registration, Login, Password Recovery, Subscriptions. Call an
Exorcist.

Something went wrong while the user tried to register. See other error messages in log
for further information.
User tried to register with email from a banned domain. If the user seems plausible,
contact the user and ask for a corporate email address. See list of blacklisted domains in
table mtchi_inno_login_blacklisted_domains.
A user/organization tried to subscribe to a subscription plan that does does not exist or
has been deactivated.

On creation of a new subscription for a user in an organization, it was discovered that a
different subscription plan for this organizaton already exists.

Subcription that is being extended or upgraded does not actually exist at all.

Insufficient details provided. If this is to create a user then at a minimum a full name and
and email is required.

This indicated user does not exist. The user may previously have been removed.

On creating a new user, this user has been found to already exist. Check if the user is not
suspended before proceeding. It is also likely that the user has changed companies and
somehow managed to keep the same email address ­ which is why we prefer corporate
email address in preference to GMAIL and YAHOO and other personal email addresses.

No subscription exists for this user or organization

A Subscription already exists for the user and the organization.

A subscription plan with these attributes is invalid. Are all the required attributes
present?

­3108 LOGIN_USER_EXISTS

User already exists

­3109 LOGIN_SUBSCRIPTION_NONEXIST

­3110 LOGIN_SUBSCRIPTION_EXIST

­3111 LOGIN_SUBSCRIPTION_PLAN_INVALID

­3112 LOGIN_SUBSCRIPTION_PLAN_EXPIRED

­3113 LOGIN_SUBSCRIPTION_FAIL

­3114 LOGIN_SUBSCRIPTION_DATES

­3115 LOGIN_SUBSCRIPTION_DETAILS

­3116 LOGIN_SUBSCRIPTION_INSERT

­3117 LOGIN_GROUPID_INVALID

­3118 LOGIN_SUBSCRIPTION_SUPERCEEDED

­3119 LOGIN_SUSPENDED

­3120 LOGIN_NOT_SUSPENDED

­3121 LOGIN_CANCELLED

­3122 LOGIN_NOT_CANCELLED

­3123 LOGIN_TRASHED

­3124 LOGIN_NOT_TRASHED

­3125 LOGIN_SUBSCRIPTION_ACTIVE

No subscription
exists for this user
or organization
Subscription
already exists
Subscription plan
invalid
Existing
Subscription plan
expired
Failed to create a
subscription
Subscription begin
date must be
before end date
Insufficient details
to create
subscription
Failed to insert
into the the
subscription table
User­Group Id
associated with
this subscription
plan is invalid.
Subscription has
since been
superseded by
another
subscription
User is already
suspended
User is not
suspended
User is cancelled User is cancelled
User is not
cancelled
User is already
trashed
User is not trashed User is not trashed
Subscription plans
is still active

User is already suspended

User is not suspended

User is not cancelled

User is already trashed

Existing Subscription plan expired

Failed to create a subscription

Subscription being date must be before end date

Insufficient details to create subscription

Failed to insert into the the subscription table

User­Group Id associated with this subscription plan is invalid.

Subscription has since been superseded by another subscription

­3126 LOGIN_SUBSCRIPTION_PLAN_NOSELECT This subscription

plan is not

This subscription plan is not selectable, either because the use­case can not select it, or
because it is disabled.

The subscription plans is still active.

Error Architecture ­ 

­3127 LOGIN_NOT_REJECTED

­3128 LOGIN_CONFIRMED

­3129 LOGIN_NOT_CONFIRMED

­3130 LOGIN_ACTIVATIONKEY

­3131 LOGIN_ALREADY_APPROVED

­3132 LOGIN_USER_REJETCED

­3133 LOGIN_SUBSCRIPTION_RESTARTED

­3134 LOGIN_GROUP

Organization Error Codes

selectable
User is not
rejected
User already
confirmed email
User has not
confirmed their
email yet.
Activation Key
does not exist
User has already
been approved
User is already
rejected
Subscription has
alsready been
restarted
User group does
not exist

User is not rejected

User already confirmed email

User has not confirmed email yet

Activation Key does not exist

User has already been approved

User is already rejected

Subscription has alsready been restarted

User group does not exist

Organization
Code

Alias

­3200 ORG_GENERAL

­3201 ORG_ID_NONEXIST

­3202 ORG_NAME_NONEXIST

­3203 ORG_USER_ID_NONEXIST

­3204 ORG_EXISTS

­3205 ORG_MULTIPLE_SIMILAR_NAMES

­3206 ORG_DETAILS

­3207 ORG_USER_NONCONTAIN

­3208 ORG_NO_USERS

­3209 ORG_NO_SUBSCRIPTION

­3210 ORG_TYPE

­3211 ORG_LOGO_FILE

­3212 ORG_COLOURS

Geospatial Error Codes

Error

General error with
Organization
Organization for given
ID not found
Organization for given
name not found
Organization for given
User ID not found
An organization of this
name already exists
Organization search
for name has more
than one match
Insufficient details to
find organization
User Id does not
belong in this
organization
This organization
contains no valid
members
Organization does not
have a subscription
Organization Type
does not exist
Invalid Organization
Logo file
Organizations
Corporate Colours are
not defined

Explanation

General error with Organization

Organization for given ID not found

Organization for given name not found

Organization for given User ID not found

An organization of this name and other matching details already exists

Organization search for name has more than one match

Insufficient details to find organization

User Id does not belong in this organization

This organization contains no valid members. This will prevent amongst other the creation of
a subscription for the organization, since a primary member in the organization need to be
accountable for the subscription.

Organization does not have a subscription

Organization Type does not exist

An invalid Organization Logo file was provided. It may only be a .png file and should be in
lower case.

Organizations Corporate Colours are not defined

Geospatial
Code
Alias
­3300 GEO_GENERAL
­3301 GEO_REGION_NONEXIST
­3302 GEO_COUNTRY_NONEXIST Could not determine country
Innovation Error Codes

Error
General Geospatial Error
Could not determine geographical region Could not determine geographical region

General Geospatial Error

Explanation

Could not determine country

Innovation
Code

Alias

­3400 INNO_GENERAL

Error Architecture ­ 

Error

General Error in the Innovation
namespace

General Error in the Innovation namespace

Explanation

­3401 INNO_ENTRY_INCOMPLETE Innovation Entry incomplete

Innovation Entry incomplete. Some critical data fields are missing.

­3402 INNO_USER_NOORG

­3403 INNO_NONEXIST

User is not associated with this
innovation
Innovation does not exist

­3404 INNO_STATE

Innovation state is invalid

User is not associated with this innovation

Innovation does not exist
The requested state for this innovation is invalid, probably because the state does
not exist.

Challenge Error Codes

Challenge
Code

Error Architecture ­ 

Alias

Error

Explanation

­3500 CHALLENGE_GENERAL

­3501 CHALLENGE_ENTRY_INCOMPLETE

­3502 CHALLENGE_ENTRY_MULTICAT

­3503 CHALLENGE_ENTRY_GROUP

­3504 CHALLENGE_CATEGORY_UNKNOWN

­3505 CHALLENGE_EVENT_UNKNOWN

­3506 CHALLENGE_JUDGES_TOOFEW

­3507 CHALLENGE_INCOMPLETE

­3508 CHALLENGE_PHASE

The user or assigned actor does not belong to one of the user groups that are allowed to enter
a challenge.

General Challenge Error

General Challenge
Error
Entry incomplete Entry incomplete
No multiple
categories allowed An innovation can not be entered into multiple entry catergories.
User does not
belong to the
correct group
Challenge
Category is
unknown
Challenge Event
is unknown
Insufficient judges
available
Challenge Event
Incomplete

The configuration for the challenge Event Incomplete.

An invalid Challenge Category Id was specified

Challenge Event is unknown

Insufficient judges available

Challenge phases
ambiguity

Either the phase does not belong to the indicated challenge, a null was provided for the
phase, the indicate phase Id simply does not exist, or the phase does exist but does have the
required attributes to be used in the current context.

Minimum quorum settings for this challenge have not been met.

No entries for this challenge event

Judge has enough entries assigned

Judge has entry assigned already

­3515 CHALLENGE_CLOSED

­3510 CHALLENGE_QUORATE

­3509 CHALLENGE_ENTRIES_NONE

No entries for this
challenge event
Not quorate for
scoring
Judge has entry
­3512 CHALLENGE_ENTRY_ASSIGNED
assigned already
­3513 CHALLENGE_ENOUGH_SCORESHEETS Judge has enough
entries assigned
­3514 CHALLENGE_NONSCORE_CATEGORY Judge does not
score this category Judge does not score this category
Challenge is
closed.
Challenge Article
does not exist
Organization for
challenge does not
exist
Category Error
Actor User Id
Error
Actor already
assigned
Actor does not
exist

­3520 CHALLENGE_ACTOR_ASSIENGED

­3519 CHALLENGE_ACTOR_NOTEXIST

­3517 CHALLENGE_ORGANIZATION

­3518 CHALLENGE_CATAGORY

­3516 CHALLENGE_ARTICLE

Organization for challenge does not exist

­3525 CHALLENGE_ENTRY_EDIT

The selected challenge entry does not exist

­3521 CHALLENGE_ACTOR_NOTEXIST
­3522 CHALLENGE_ACTORROLE_NOTEXIST Actor­Role does
not exist
Challenge Entry
­3523 CHALLENGE_ENTRY_NOTEXIST
does not exist
­3524 CHALLENGE_ENTRY_DISQUALIFIED This entry has
been disqualified This entry has been disqualified for whatever reasons.
Insufficient user
access to edit a
challenge entry
This Challenge
Event is now
closed
This Challenge
Entry is unkown
Invalid UNIX
Timezone
Friendly URL to
challenge entry is
missing

Friendly URL to the challenge entry is missing

­3527 CHALLENGE_ENTRY_UNKNOWN

­3526 CHALLENGE_EVENT_CLOSED

This Challenge Entry could not be found.

­3529 CHALLENGE_ENTRY_URL

­3528 CHALLENGE_TIMEZONE

This Challenge Event is now closed

Invalid Timezone provided. See the UNIX timezones that we use in table
mtchi_inno_geo_timezones, which are more than adequate to cover the world.

Challenge is closed. There are certain things that you can't do with a closed challenge, such
as attempting to add a phase to it.

And Article Id referred to in the Challenge configuration does not exist.

Insufficient or conflicting details for this category, or the category does not exist.

The user specified to perform for this phase of a challege does not exist, or is disabled.

The user has already been assigned to this role in this phase

The challenge actor either does not exist or could not be created

The role for this challenge actor either does not exist or could not be created

You attempted to edit a challenge entry but you do not have suffucient user access for this.

Event Error Codes

General Error in the Event Namespace General Error in the Event Namespace

Alias

Error

Event
Code
­3600 EVENT_GENERAL
­3601 EVENT_INCOMPLETE Entry incomplete
­3602 EVENT_TYPE
­3603 EVENT_INSERT
­3604 EVNET_DISABLED
­3605 EVENT_NOTIFYABLE Event type is not notifiable
Config Error Codes

Unknown Event Type
Failed to insert into event table
Event type is disabled

Error Architecture ­ 

Explanation

Entry incomplete
Unknown Event Type
Failed to insert into event table
Event type is disabled
Event type is not notifiable

Explanation

Alias

Error

Config
Code
­3700 CONFIG_GENERAL
­3701 CONFIG_PARAMETER Parameter does not exist
­3702 CONFIG_VALUE
­3703 CONFIG_GROUP
­3704 CONFIG_READONLY This is a read­only parameter
Content Error Codes

General error with configuration General error with configuration

Parameter does not exist
Impossible value for parameter
Impossible value for parameter
This is a grouping of parameters This is a grouping of parameters

This is a read­only parameter and can not be set

General issue with site content handling

Explanation

Alias

Content
Code
­3800 CONTENT_GENERAL General issue with site content
­3801 CONTENT_ARTICLE

handling
Invalid Article Provided

Error

­3802 CONTENT_CATEGORY Invalid Category Provided

­3803 CONTENT_TITLE
­3804 CONTENT_INSERT
­3805 CONTENT_UPDATE
­3806 CONTENT_ACL
System Error Codes

The supplied Article Id does not exist, or no article matching the given criteria could be found.
The supplied article­category Id does not exist, or no article­category matching the given criteria
could be found.
Invalid Title provided. Either it was null or too long.
Could not add new content
Could not update content

Invalid Title
Could not add new content
Could not update content
Access View Level does not exist Access View Level does not exist

System
Code

Alias

Error

Explanation

­4000 SYSTEM_ERROR
­4001 SYSTEM_JOOMLA_CONTENT Error in Joomla Content The is an error in the Joomla Content: The HTML either does not parse or absolute paths have

There was an as­yet unspecified System Error. See preceding and following error messages for
more details.

General System Error

been used where they should not have been.

­4002 SYSTEM_PAGE_ACCESS

You do not have access
to this page.

You need to be logged in and be assigned to a specific user group for access to this page.

How to refresh this documentation

As the Matchi system evolves, more error codes will get generated. To update the error code documentation run the script below and paste the results in the Wiki editor.

```sql
set session group_concat_max_len = 1000000; 
set @lastsubsystem:= ''; 
select concat(group_concat(wikitext separator ''), 
              char(10),'|}',char(10) ) 
 from (  select concat(if(@lastsubsystem=subsystem, 
                        '', 
                        concat(if(@lastsubsystem<>subsystem and @lastsubsystem<>'', 
                                  concat('|}',char(10)), 
                                  ''), 
                               '==',subsystem,' Error Codes ==',char(10), 
                               '{| style="text‐align:left;" class="wikitable"',char(10), 
                               '|‐',char(10), 
                               '! colspan="4" style="font‐weight: bold; font‐size: 18px; text‐align:left; background‐color:orange;" | ',subsystem,char(10), 
                               '|‐',char(10), 
                               '! Code',char(10), 
                               '! Alias',char(10), 
                               '! Error',char(10), 
                               '! Explanation',char(10)) 
                      ), 
                      '|‐',char(10), 
                      '| ',id,'||',alias,'||',item_en_gb,'||',ifnull(help_en_gb,''),char(10) 
                     ) as wikitext, 
               (select @lastsubsystem:=subsystem) 
          from mtchi_inno_system_picklist_error_codes 
         order by  display_order_id asc ) a;
```

Error Architecture ­ 

Security Architecture ­ 

Security Architecture

Contents

Access Matrix of Matchi's Sub­Systems

Security Architecture ­ 

High­level summary of access levels to content and sub­systems, with authentication method:

Sub­System Access Matrix

Use Case:

Manager Innovators Buyers Sponsors Challenge
Owner
Open

Open

Open

Open

Open

Challenge
Admin

Open

Challenge
Judge Developer Tester
Open

Open

Open

System

Administrator

Open

Password

Open

Access Area Public/Guest Content
Website public
pages
Website own
innovation
Website
others’
innovations
Website
content
management
Website
functional
development
Website
functional
administration
Challenge
Entry
Challenge
Scoring
Challenge
Management
Challenge
Reports
Server
development
Server
operations
Sever
administration
Database
development
Database
operations
Database
administration
Business
systems
development
Business
systems
operations
Business
systems
administrations

Password

Password Password Password

Password Password Password Password Password Password Password Password

Password

Password Password Password

Password Password Password

Password Password Password

Password Password

Password

Password Password

Password

Password Password

Password

Password Password Password

PPK

PPK

PPK

PPK

PPK

PPK

PPK+SUDO

Password Password Password

Password Password Password

Password

Password Password Password

Password Password Password

Password

Notes on simplifications

1. Business Support Systems have been grouped together and currently have the same access model and methods and consist of:

Self­hosted:

Cloud­hosted:

JIRA Issue Management
TEMPO Timesheet management
Wiki system documentation
OwnCloud file storage documentation system (in the process of replacing DropBox)

ZoHo CRM and tactical reporting system
DropBox tactical file storage and sharing system
GMail Email and Calendaring system
Slack Communications

Security Architecture ­ 

BitBucket configuration management

2. Both System Administration roles and Developer and Tester roles span over the following:

Business Support sub­system
Server Backend sub­system
Website

Technical Details on Authentications

Password: Joomla password authentication mechanism, uses various password saltings, hashes and the BCrypt library.
PKK: Public/Private key authentication with 1024­bit RSA encryption and using the OpenSSH library. It is only possible to connect as user
madman.
SUDO + PKK: Same as PKK, but a sudo command is required to escalate the user to user root, since it has been made impossible to directly
connect as user root.

Security Overview
Common Weaknesses in an enterprise

The top weaknesses in the security chain in an enterprise are the staff / employees who work for the enterprise. This is why they are the commonest
attack vector.
Origins of Attacks
Types of Attacks

Sophisticated attacks

A sophisticated attack can take a long time to plan and is executed over a number of days.The planning usually involves profiling a selection of i ndividuals in the company. They are usually aimed at high­value companies. The average cost to cyber­criminals of a planned attack averages at about $1300. The most common attacks are:

Spear Phishing attack: This is mostly done via a plausible­looking email that can contain booby-­trapped attachments that unleashes malware on the victim's machine if the attachment is opened or viewed or an instruction to go to a website that the victim sheepishly follows ­ however the website is a plausible copy of a real website and armed with malware or information­capturing features.

Watering Hole attack: By offloading mal­ware from a peripheral site that is known to be visitid by an individual, the mal­ware executes its attack when the individual subsequently visits the target site.

Brute Force attacks: 

These are simple in nature and are aimed at public­facing systems, such as websites and email servers. The cost of these attacks are trivial, as the
attackers simply run a never­ending script that scans random IP addresses until a possible victim is found. The most frequently­encountered attacks are:

Dictionary attacks: These are aimed at servers themselves, websites logins, and email logins.
Distributed Denial of Service: Many compromised computers can be instructed to send resource­consuming IP packets to the targeted server or
domain, and so rendering the server incapable of performing its intended function

Attack Vectors
Direct server attack on specific ports

This is usually committed by opportunistic "script­kiddies" who deploy as password dictionary attack against the user 'root'. This is the simplest form of
attack, which is why it is so popular. Once a server has been compromised and a server session is obtained, much local damage can be committed, and
the server can be used as a launching point to compromise more servers, thus further obfuscating the attacker's origins.

Attack Surface area

All Matchi servers are visible on the public Internet, and there is little point in changing the stadard SSH port from 22 to something else, since a port­
scan will show the few open ports and making the guessing of the SSH port trivial.

It is planned to place SSH­access to the servers behind a VPN in future as a further precaution.

Potential damage

Dictionary attacks waste bandwidth and computation resources. Even though password authentication is not possible on Matchi servers, not all attack
scripts are sophisticated to detect this and cease the dictionary attack.

Should an SSH attack have been successful, an attacker could have

Security Architecture ­ 

Vandalised the system
Added spamming or DDoS processes to run on the server
Opened up ports to the public for internal services
Installed a root­kit in order to access the server at leisure at the later time
Uploaded illegal or incriminating content
Host a phishing site
etc...

Defences

SSH Daemon Configuration The SSH Daemon has been configured in each server such that:

Access via SSH is not possible using password
It is impossible to log in to any servers as user root
It is only passible to log as one single nominated account. Subsequent escalation to user root is possible once logged in, where required.

Fail2Ban Fail2Ban daemon runs on each server:

Fail2Ban immediately bans an IP address after one failed attempt to connect. The ban is lifted after 24 hours to stop the blacklist on the server's
firewall from growing out of control.

RKHunter The RKHunter daemon (Root­Kit Hunter) runs on each server:

Detects if any of the binary files have been altered, and if so, it sends out an email alert to security@matchi.biz
Looks for file signatures in files that match those of known root­kits. If one is found, it sends out an email alert to security@matchi.biz

Automated Detection

A daily digest of banned IP addresses detected by the Fail2Ban daemon is sent to security@matchi.biz.

Manual Detection

Log files can be analysed to see which sessions were disconnected.*

root@mweb02 /var/log # grep "disconnect" secure |awk '{print $9}' | grep '[1‐9]' | sort ‐u | sed ‐e 's/:$//' 
etc...

The IP addresses are inevitably shown to originate from unusual locations, like Vietnam below:

```bash
% [whois.apnic.net] 
% Whois data copyright terms    http://www.apnic.net/db/dbcopyright.html 
netname:        CMCTELECOM‐VNNIC‐VN 
descr:          CMC Telecommunications Services Company 
descr:          273 Doi Can str, Ba Dinh, Ha Noi 
etc...
```

Check who is currently logged on to the server*

It would only be one, sometimes two sessions on a server.

```bash
root@mweb02 /var/log # w 
USER     TTY      FROM             LOGIN@   IDLE   JCPU   PCPU WHAT 
```

Recovery

Recovery from a successful SSH attack if root access was obtained is risky and if possible, a full server rebuild is preferred.

Possible recovery steps after an attack like this are, in order of increasing effort:

If only a root­kit was discovered, the adulterated files can be replaced by just re­installing the relevant packages
The server needs to go into fail over mode (if a fail­over server exists for the attacked server)
All packages on the compromised are re­installed, if the package manifest has not been corrupted
Capture all access logs for later analysis and evidence if a server rebuild is required (see next steps)
The compromised server needs to be rebuilt from a recent diskimage that is known to not be compromised
The compromised server needs to be rebuilt from scratch

Attack on port 25: Postfix SMTP mail service

Security Architecture ­ 

An attacker can attempt to send or relay spam emails via the SMTP services that on services.

Attack Surface area

Each server runs an SMTP service that acts as a relay for locally­generated emails to the GMail email service.

Potential damage

Reputational damage
If sufficient complaints are lodged, your  the matchi.biz domain may be repoted to one of many spam­prevention offices such as Spamhaus. This will
cause most outgiong emails from Matchi to automatically get rejected by the recipient.

Defences

Post 25 is only accessible from with the server.

Detection

It is currently only possible to detect SMTP­service abuse by studying the SMTP/Postfix log files

Recovery

After having determined which anti­span offices deem the matchi.biz domain to be a spam originator, it is possible to appeal to each of them to them in
order to remove the blacklisting. This is a very time­consuming process and the request will only be effected after 24 hours at least, since email servers
typically update their local spam domain blacklists once per day.

A whole range of attacks are possible the Apache attacks in order to compromise its integrity, slow it down, or crash it.

Attack Surface area

The public­-facing website at http://[your-domain]
The administration website at http://[your-domain]/administrator

Potential damage

Most of the attack types results in a loss of performance or loss of integrity of the presented data on a browser. Ultimately, reputation suffers followed
by the inevitable loss of revenue.

Defenses

Keep the patch­level of Apache up to date
Cloudflare prevents a number of typical attacks types on Apache

Detection

Recovery
Distributed Denial of Service (DDoS) attack on servers

Attack Surface area

Any of your servers in the data centre. DDoS attacks are usually focussed on webservers, however.

Potential damage

Loss of service to users, that can range from being annoying through to being detrimental to revenue. A DDoS usually results in a loss of reputation.

Defenses

All traffic to the webserver is bound to the domain matchi.biz and is routed via the Cloudflare Content Delivery Service. Cloudflare additionally offers
a low­level DDoS prevention. On experiencing a DDoS attack, Cloudflare can manually be set to actively repel DoS agents.
Detection

When access to the website is slow
Observing the session count on Apache management console

Security Architecture ­ 

Keeping abreast with current DDoS attacks on http://www.digitalattackmap.com/

Recovery

Your reputation needs to be restored. It may be prudent to send an email to all users who are believed to have a session open on the website at the
time of the attack, depending on the severity of the impact ­ should the defense have failed for whatever reason.

Additional reading

https://f5.com/Portals/1/PDF/security/2016_DDoS_Attack­Trends.pdf

Website fake user account creation

Attack Surface area

The Matchi website: An adversary would attempt to create an account (either automatically or manually) in the hope that the account would be
approved and access to the Matchi Innovation Database be obtained.

Potential damage

This adds an unnecessary workload on the load on member management staff, who need to remove this person.
Should an attacker accidentally be given access as an innovator, the attacker can only see his own innovation and not that those of others.
There is no limit to the number of innovations that an innovator can create, and an adversary who has obtained access could automate the
creation of unlimited innovations, which will consume system resources.

Defenses

The sign­up process is protected by Google's "I am not a robot" reCAPTCHA. This is a very successful measure, although there are reports that it
can be circumvented in automated attack scripts.
The sign­up process includes an email verification step
Every user who applies to become a member (Innovator, Buyer, Sponsor, Challenge Owner), is manually vetted. A failed applicant can
summarily be rejected. Each member approval event or rejection event is notified to other member management staff.
Members' email addressed that belong email domains known to be favourited by attackers, are scrutinised and if the email has not been verified
within a certain period, or the applicant has not been accepted within a certain period, then the applicant is summarily rejected. The applicant is
not notified of this event. A list of all automated rejections is emailed in a daily digest to security@matchi.biz.
New email domains that are used can be added to the configuration of automated rejection process.

Detection

Invalid sign­ups that pass the initial scrutiny can only manually be detected, which number on average one per month.
An adversary who has obtained access and who automates the creation of unlimited innovations will draw attention on completing the innovation
entry.
Recovery

Any (fake) innovations that an attacker may have created are automatically removed when that user is removed from the Matchi members' database.
Dictionary attack agaisnt the Matchi website

Attack Surface area

The Matchi website: An adversary would attempt to access the site with random user names and passwords (either automatically or manually) in the
hope that access to the Matchi Innovation Database be obtained.
Potential damage

Consumes network and system resources
A successful attack to the correct user account allows access to all Matchi Innovations.

Defenses

Successive, repeated failures with a given time frame to gain access is detected and the attacker's origin IP address is permanently banned. The number
of repeats and time frame duration is configurable.
Detection

The list of banned IP addresses can be viewed through the "Brute Force Stop" Joomla component in the Matchi Administration website.

Recovery

It is not possible to undo any data­theft damage done by an adversary who has gained unlawful access to the system.

Website SQL injection

Security Architecture ­ 

By manipulating a URL on a database­driven website and adding SQL commands, it can be possible to effect data changes on the database.

The favourite motive for an attack is to replace website content in order to espouse some ideology or to brag amongst peers.

Attack Surface area

The Matchi webserver

Potential damage

The potential damage from such an attack is limitless. If the

Defenses

All SQL operations on the Matchi site are performed via the Joomla database API, which offers a very solid protection against this. The Joomla
Framework is regularly updated as new vulnerabilities are discovered. Most vulnerabilities are "zero­day", which means that they have not yet been
know to be used "in the wild" by attackers.

Detection

It is not possible to detect a SQL Injection attack as such: Data will either be observed as incorrect or deleted, or parts of the Matchi website will not
work correctly.
Immediate action

Ban the attacking IP address from all the Matchi servers

Recovery

Restore the most recent backup know to now have been subjected to this attack
Switch over to the fail­over system, if it can be ascertained that the fail­over database does not contain a replication of the production database's
attack.

Website data slurping

It is in theory possible to slurp attachment documents and customers' corporate logos.

Attack Surface area

Matchi webserver

Potential damage

An adversary can infer what innovations are on the Matchi Innovation Database by looking at the collection of innovation­related documents and
the corporate logos.

Defenses

The Matchi website is front­ended by Cloudflare, which detects unusual content downloads to a single IP address and will stop it.
There are .htaccess files that are configured to prevent access to directories that contain collections of images and documents

Detection

This can manually be detected by looking at server logs and the volume that is downloaded to an IP address.

Recovery

It is not possible to recover from an attack like this.
Uploading Malware in Attachments

Attack Surface area

Innovators only can upload files to further support their innovations. These are typically brochures and white papers. It is possible that an attachment
can contain a specially­crafted piece of malware that executes when the file is opened again in the right environment.

Potential damage

Since we are running Linux, it is unlikely that our system can be damaged from malware that is hidden in attachments.

Security Architecture ­ 

We do allow innovation buyers and innovation sponsors to download attachment files, and we would effectively be distributing the malware to
our clients. This can lead to reputational damage.

Defenses

New attachments to innovations are scanned for malware using maldet.

A daily update of malware signatures is updated to maldet.

Detection

Detection is automated. A notification email is sent to security@matchi.biz when an attachment with malware is found.

Recovery

The offending file is moved to a safe directory, from where it can either be manually cleansed or deleted and the file uploader can be asked to resubmit
the attachment.

Server Build

Contents

Server Build ­ 

Server Build ­ 

Server Build ­ 

Common Server Build

The following series of build steps needs to be performed for each server, regardless of the server’s function.
Conventions

Builds are consistently referred to by their initial inception date in ISO date­format (YYYYMMDD). This is reflected in the names of the directories for source
code, static content and databases.
All account names and server names are in lower case
All file names are either in lower case with “_” separators between terms, or in Camel­case with the first letter of each term being a capital letter
Example commands that begin with a '$' are performed by a non­root user, and commands that begin with a '#' are performed by the root user.

First Access

From your terminal (use PuTTY if you are using Windows), open an SSH session to the server using the root account and default password. The password and server
details are provided by the hosting provider and will be different for each server.

$ ssh root@s470071337.websitehome.co.uk 
root@s470071337.websitehome.co.uk's password:

Type in the root password and hit Return. Ignore any warnings for now:

Warning: untrusted X11 forwarding setup failed: xauth key data not generated 
Warning: No xauth data; using fake authentication data for X11 forwarding. 
X11 forwarding request failed on channel 0 
Last login: Fri May 31 15:42:09 2013 from host86‐142‐19‐185.range86‐142.btcentralplus.com 
[root@s16972616 ~]#

You are now logged in as user ‘root’, who is the super user on the server.

Since this system does not host individual enterprise user­accounts, we only need one more system administrator user who is a less powerful than the 'root' user to
perform basic management tasks. It will be possible to temporarily escalate this user's privileges to perform tasks that only the 'root' user would normally be able to
perform (see the section on SUDO). From a security perspective, we will completely disable the ability to log into the server using the 'root' account (because everyone
knows that such a user exists!) and allow solely through this Matchi system ADministrator MANanger account, madman,

[root@s16972616 ~]# useradd ‐g adm madman ‐c 'MWEB02 System Administrator'

Set the internal password for administrator user. If the password is weak, you will be warned, as in this example.

[root@s16972616 ~]# passwd madman 
Changing password for user madman. 
New password:  
BAD PASSWORD: it is based on a dictionary word 
Retype new password:  
passwd: all authentication tokens updated successfully. 
[root@s16972616 ~]#

Replace Password logins with Key logins

Passwords are by nature unsafe and are far more likely to fall into the wrong hands than other forms of authentication. We therefore use Public/Private Key
authentication where possible on the system. All terminal­based network traffic between server and public network is encrypted since we are using the Secure Shell
Version 2 (SSH2) protocol.
Setting up a Key­Pair

To set up a public private key­pair for the server, do this:

$ ssh‐keygen ‐t rsa 
Generating public/private rsa key pair. 
Enter file in which to save the key (/home/madman/.ssh/id_rsa):  
Enter passphrase (empty for no passphrase):  
Enter same passphrase again:  
Your identification has been saved in /home/madman/.ssh/id_rsa. 
Your public key has been saved in /home/madman/.ssh/id_rsa.pub. 
The key fingerprint is: 
2e:77:26:0c:28:08:ef:16:d9:93:ed:2f:e4:17:23:3a madman@mdev01.localdomain 
The keys randomart image is: 
+‐‐[ RSA 1024]‐‐‐‐+ 
|                 | 
|                 | 
|.                | 
|.o o +           | 
|. = = o S        | 
| . o oo+o        | 
|  o  +o.=oo      | 
| .  E o+.+       | 
|     . o.        | 
+‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐+

Accessing the Remote Server

To access the remote server from your local desktop machine, you will also need to have a public/private key­pair. If you do not have such a key­pair you can create
your own key­pair on your own machine as follows. (Do not specify a passphrase for the Private Key when prompted)

[mymachine] $ ssh‐keygen ‐t rsa 
Generating public/private rsa key pair. 
Enter file in which to save the key (/home/[myname]/.ssh/id_dsa) 
Enter passphrase (empty for no passphrase):  
Enter same passphrase again:  
Your identification has been saved in id_rsa. 

Server Build ­ 

Your identification has been saved in id_rsa. 
Your public key has been saved in id_rsa.pub. 
The key fingerprint is: 
03:5f:9f:fa:0d:47:33:6f:ca:bf:ee:15:67:c3:9f:09 
The keys randomart image is: 
+‐‐[ RSA 1024]‐‐‐‐+ 
|                 | 
|                 | 
|      .   .      | 
|       o . . ..  | 
|        S   oE++o| 
|         . . ..=B| 
|          . . .o=| 
|           . = o.| 
|            . *=o| 
+‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐+

The Key­pair for your machine is now created. You can list the public and private keys them with the command:

[mymachine] $  ls ‐al ~/.ssh 
‐rw‐‐‐‐‐‐‐   1 only_me only_me  668 Feb 17  2011 id_rsa 
‐rw‐r‐‐r‐‐   1 only_me only_me  607 Feb 17  2011 id_rsa.pub

Where:

id_rsa is the private key file. Keep it safe on your personal machine. Do not let it escape!
id_rsa.pub is the public key file. It goes onto the keyring of every server that you want to connect to. It is OK to share this file with anyone in the public.

Adding your Key on the Server

To be able to access the server using your key, you need to get the public key onto the server first. For this, you do need to know what the password to the server is, and
then only this once.

In the case where you are not a system administrator but need access to the server, you would email your public key to a system administrator who would then
manually add it to the server's key ring, as explained in the section below.

The 'First­Principles' way

The basic way to put the public key file onto the server's key ring is to simply copy and paste it using a text editor. First we list the public key:

[mymachine] $ cat .ssh/id_rsa.pub  
ssh‐rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDI6DGYYu2Zzm2Gy5BFvgAt7qg8DDJJbnpVHu82mLCAqwx+fa2gWj+sc7S2utkhEwEJD5Qcs103gUBU4xwHwGMbHDPGY6cSmPTB6geo4cgWwjMB1UQG5j5zfoHRx/9gEZXiTGvdqy5R/gfo8P3kW2r2GlFEIzLD1CHWzowTgesIrNRfWl6FwP+IWH710YmlULwN/AgAKY78JG8MslnfRO5fSFz5yfXjrO9DH0m/kfcbhoXVrTjOOXa12JNuqmQKogXqICViB3lh+FbUbT4hWrFFp3Pm5Lt/V9HXsVH788OV3pqVKYrqrfPXvCceHmaLkCgN+iw6hKJktkxBdfPa938X captainspectular@ziltoidtheomnicient

Note
Remember that it is OK to display a public key in public ­ hence the name "public". But don't ever let anyone ever see your private key.

Now select the text that starts from the ssh‐dss… bit all the to the user name bignose.the.third@terminator.com and copy this. On the target server, open the following
file using the vi­editor, type  i  for insert­mode, and paste the content into the bottom of the file. It is a long line of text, so it will wrap:

[madman@[server] $ vi .ssh/authorized_keys

After you have pasted the key value in, save and close the file (for the vi­editor at least): Hit the  Esc  key, then type  :wq , then hit  Return .

You have now successfully set up Public/Private­key authentication for the user madman from your personal machine to the server, albeit using the manual way.

A nicer way to disseminate your Public Key

There is a dedicated command that also accomplished the same as the above process: ssh‐copy‐id. You will of course still be prompted for a password:

[mymachine] ~ $  ssh‐copy‐id ‐i .ssh/id_dsa.pub madman@[servername] 
madman@[servername]s password: <....> 

Number of key(s) added: 1 

Now try logging into the machine, with:   "ssh madman@[servername]" 
and check to make sure that only the key(s) you wanted were added.

Testing your SSH connection

Test your new key authentication from a new terminal session on our personal machine. It would be helpful to keep the old session open in case you accidentally did
something wrong.

[mymachine] $ ssh madman@[server]  
Warning: untrusted X11 forwarding setup failed: xauth key data not generated 
Warning: No xauth data; using fake authentication data for X11 forwarding. 
X11 forwarding request failed on channel 0 
madman@[server] ~$

Look! No password was required! You appear to have successfully logged on to the server. Check if this really is the user 'madman' who is logged on to the server:

$ id 
uid=503(madman) gid=4(adm) groups=4(adm)

SUDO: Granting root­level functions to a mortal user

In order to govern a secure system, it should under normal circumstance not be possible to log in as the root­user. However, an administrator will occasionally need to
perform root­level functions by momentarily elevating the user to root status and to execute root­level operations. For instance, installation of software can only be as
user root, or as a user with temporarily­elevate rights through the sudo­process. This is done by making the user a "sudo­er" (from the concept pseudo­root) and
granting previously­agreed functions that the admin user may need to execute. The granting of privileges is done by either making the admin user a member of a
specific group (we do this here) or by allocating specific functions to the admin user (too labour­intensive).

The only person who can make sudo privilege grants is the root­user.

As user root, edit the /etc/sudoers file using the VI editor, using a special command:

root@s16972616 ~]# visudo

The VI­editor is a very sophisticated editor which you will you will either love or hate. In the case here where we need to start editing the file, hit the  i ­key (for insert
mode in the vi­editor) and add this to the bottom of the file:

## MATCHi 
%admin  ALL=(ALL)       ALL

By default, a sudo­user can only execute programs that are in the directories /sbin, /bin, /usr/sbin and /usr/bin ­ unless the full directory­path to the program is

By default, a sudo­user can only execute programs that are in the directories /sbin, /bin, /usr/sbin and /usr/bin ­ unless the full directory­path to the program is
given, which is a pain. Since we have a number of our own system administration scripts deployed in /usr/local/bin, this directory needs to be added too. So change
line 86 (more or less) and add this directory to the path so that it looks like this:

Server Build ­ 

Defaults    secure_path = /sbin:/bin:/usr/sbin:/usr/bin:/usr/local/bin

Save and close the file: In vi, this is done by hitting the  Esc ­key, then hitting these 3 keys:  : w q  (for 'write', 'quit').

Create a new group for sudo'ers and associate the administrator user, madman, to the newly­created group called admin:

[root@s16972616 ~]# groupadd admin 
[root@s16972616 ~]# usermod ‐a ‐G admin madman

Test the sudo'ing capability of the administrator user. First, log in as the administrator user. Rather than create a new session, we can do a "substitute user" (su­
command):

[root@s16972616 ~]# su ‐ madman 
[madman@s16972616 ~]$

Also test and ensure that the administrator can sudo to root­level:

madman@s16972616 ~ $ sudo su ‐ 
[sudo] password for madman:  
root@s16972616 ~ # id 
uid=0(root) gid=0(root) groups=0(root)

If this test failed, then you should fix the problem using the existing and open, root­logged­in terminal session to the server. Hopefully you have not closed it already.
Set up User and Server Identifiers in the command prompt

Since there are multiple servers in the solution, it is helpful for always clearly identify the user and the server to avoid the wrong command to be executed on the wrong
server. Since access to the servers will mostly be via SSH­terminal session, the best­practice approach is to display this information on every command in the form of
an elaborate command prompt. The standard convention is that the root­user command prompt ends in a ‘#’­character, and all other (non­root) users’ command
prompts end in a ‘$’­character.

Non­root user command prompt:

For the current (non­root) user, set the command prompt and include the server alias name in there:

[madman@s16972616 ~]$ vi ~/.bash_profile

Add to the file for a green command and blue directory path, and set the traditional $ character at the end of the non­root prompt. Replace the mweb01 with the
'friendly' name of the server:

export PS1="\[\033[01;34m\]\u@mweb01 \[\033[01;34m\]\w $\[\033[00m\] "

Root user command prompt:

When you do the same for the user root, the conventsion is to use a # in the command prompt, in which case you would need to do this:

export PS1="\[\033[01;31m\]\u@mweb01 \[\033[01;34m\]\w #\[\033[00m\] "

To make it more obvious that the root user is active, the prompt is also set to red. Again, do the same for user root later on the other servers.

Command history

The command history holds the last 1000 commands entered by default. This is often not enough, so this can be extended to 10000 by setting this system variable in
the file:

export HISTFILESIZE=10000

Save and Close

Save and Close the file (hit  Esc  and then  : w q ). You can either open another console session to see the effect of the changes that you made in the .bash_profile
file, or you can effect is immediatel with the source command. See how the command prompt changes:

$ source ./.bash_profile 
madman@mweb01 ~ $

Document Convention going forward

Going forward in the documentation, we don't show the full command prompt in console commands and simply indicate with a $ in the first column to show whether
the line was an input command or just output from the preceding command. When logged in as user root, we show the # in the command prompt of course.
Server aliases in hosts file

It convenient to refer to the servers by their local aliases instead of the formal instance names that were allocated to them by the hosting provider. Referring to servers
via aliases makes the migration of infrastructure from one hosting provider to another easier. The current servers are known among each other by the following aliases,
which are set on each server’s hosts file:

Web Server, alias mweb01
Database Server, alias mdb01
Application Server, alias mapp01
Test Server, alias mtst01

Extend this pattern as further servers are added to the solution.

Server MWEB01

On the web server, edit the hosts file /etc/hosts and add the following:

::1         localhost localhost.localdomain localhost6 localhost6.localdomain6                                                                               

Server MDB01

On the database server, edit the hosts file /etc/hosts and add the following:

::1         localhost localhost.localdomain localhost6 localhost6.localdomain6                                                                               

Server MAPP01

Server Build ­ 

On the application server, edit the hosts file /etc/hosts and add the following:

::1         localhost localhost.localdomain localhost6 localhost6.localdomain6                                                                               

Any new Servers

::1         localhost localhost.localdomain localhost6 localhost6.localdomain6                                                                               
# Any the other friendly server names and their IP addresses 
...

Your own Machine

On your own machine, add the following to your hosts file. If your machine is a Linux or Apple machine, add this to the file /etc/hosts using nano or vi.

If your machine runs Windows, add the following text to the file C:\Windows\Drivers\etc\hosts using Notepad or any similar tool:

# Any other friendly server names and their IP addresses 
...

Setting up additional Server Repositories

The default code repository that comes with CentOS or RedHat is very conservative and does not contain leading­edge releases of many services and applications. PHP

The EPEL and REMI repositories

These two repositories have proven over time to be the most robust and stable repositories:

EPEL: "Extra Packages for Enterprise Linux"
REMI: Remi is a lovely person who devotes much time to the management of open source packages

These two additional "catalogs of software packages" are sufficient to serve the current needs. Follow the steps below to add more repositories if ever a need for it
arises.

Install more repositories

This installs further repository catalogs on the server. Once the these are installed and enabled, they will automatically be updated with the core CentOS repository on
the yum update command.

For CentOS 6.x, the commands are:

$ sudo su ‐ 
# wget https://dl.fedoraproject.org/pub/epel/epel‐release‐latest‐6.noarch.rpm && rpm ‐Uvh epel‐release‐latest‐6.noarch.rpm 
# wget http://rpms.famillecollet.com/enterprise/remi‐release‐6.rpm && rpm ‐Uvh remi‐release‐6*.rpm

For CentOS 7.x, the commands are:

$ sudo su ‐ 
# wget https://dl.fedoraproject.org/pub/epel/epel‐release‐latest‐7.noarch.rpm && rpm ‐Uvh epel‐release‐latest‐7.noarch.rpm 
# wget http://rpms.famillecollet.com/enterprise/remi‐release‐7.rpm && rpm ‐Uvh remi‐release‐7*.rpm

Enabe the REMI Repository

Set the enable=1 flag for the REMI repository so that this repository does not need to be explicitly declared when installing software packages from there.

$ nano /etc/yum.repos.d/remi.repo 
... 
[remi] 
name=Remi RPM repository for Enterprise Linux 6 ‐ $basearch 
#baseurl=http://rpms.remirepo.net/enterprise/6/remi/$basearch/ 
mirrorlist=http://rpms.remirepo.net/enterprise/6/remi/mirror 
enabled=1 
gpgcheck=1 
gpgkey=file:///etc/pki/rpm‐gpg/RPM‐GPG‐KEY‐remi

Change it accordingly for CentOS 7.x
Enabe the EPEL Repository

Set the enable=1 flag for the EPEL repository so that this repository does not need to be explicitly declared when installing software packages from there. Recently, this
repository is enabled by default, so there may not be anything to do here.

$ nano /etc/yum.repos.d/epel.repo 
... 

[epel] 
#baseurl=http://download.fedoraproject.org/pub/epel/6/$basearch 
mirrorlist=https://mirrors.fedoraproject.org/metalink?repo=epel‐6&arch=$basearch 
failovermethod=priority 
enabled=1 
gpgcheck=1 
gpgkey=file:///etc/pki/rpm‐gpg/RPM‐GPG‐KEY‐EPEL‐6

Change it accordingly for CentOS 7.x

Update the new Repositories

Now would be a good time to update the new repositories:

# yum ‐y update

# php ‐‐version 

Operational Tools

Server Build ­ 

These tools are required for performing general operations such as deploying new releases.

Subversion Client

We use Subversion at the moment for our code management, although the aim is to eventually use GIT.

Installing the Subversion Client

Install the Subversion Client if it is not already installed:

$ sudo yum ‐y install subversion

Connecting for the first time to Matchi's Subversion Repository

The default location for the local Subversion sandbox is ~/svn<code>. On the assumption that the Subversion Repository has been set up, do a check out of
this repository into the server's workplace:

$ mkdir ~/svn 
$ cd ~/svn 
$ svn co http://mapp01/svn/matchi/trunk/php

You will be prompted for your subversion username and password:

Authentication realm: <http://mapp01:80> Subversion repositories 
Password for 'madman':  

‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐ 
ATTENTION!  Your password for authentication realm: 

   <http://mapp01:80> Subversion repositories 

can only be stored to disk unencrypted!  You are advised to configure 
your system so that Subversion can store passwords encrypted, if 
possible.  See the documentation for details. 

You can avoid future appearances of this warning by setting the value 
of the 'store‐plaintext‐passwords' option to either 'yes' or 'no' in 
'/home/madman/.subversion/servers'. 
‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐ 
Store password unencrypted (yes/no)? yes 
A php/... 
...

Do the same for the other pertinent directories ‐ there is no need to get the entire repository, as it contains branches and archives which will just
clutter up the server's hard drive.

$ svn co http://mapp01/svn/matchi/trunk/sql 
$ svn co http://mapp01/svn/matchi/trunk/usr

Git Client

Some of the diagnostic utilities are only available from GIT repositories for which the GIT client is required. The default location for the local GIT
sandbox is <code>~/git<code>.

Installing the Git Client

$ sudo yum ‐y install git

C‐Compiler

In rare cases, a C/C++ compiler is required to build third‐party utilities, and perhaps even internal utilities.

$ sudo yum ‐y install gcc

General Utility Tools

A consistent set of tools is required on each server for managing and monitoring the server. The following are assumed to be installed for moving
forward with the server build, so install them first.

The tools are installed using the preferred package management application of the Red Hat and CentOS operating system, called YUM. Other package
management tools such as RPM can also be used, if you have previously pulled down the correct version of the RPM file from the appropriate repository.
So RPM sounds complicated? Stick to YUM then!

Install the NANO editor

VI is the preferred editor to many sysadmin people, but NANO is a simpler editor, although less sophisticated. Install it using YUM, and when
prompted, enter the password for user madman (and not the password for user root):

[madman@server ~]$ sudo yum install nano 
[sudo] password for madman:  
... 
Success.

Fine‐tune the nano‐editor settings for the type of application. Since this configuration files is in the /etc/ ‐directory, it can only be written to
as root, or as we do here, a sudo‐ed user and make the following changes:

[madman@server ~]$ sudo nano /etc/nanorc 
... 
set tabsize 2 
... 
set tabstospaces 
... 
include "/usr/share/nano/nanorc.nanorc" 
include "/usr/share/nano/perl.nanorc" 
include "/usr/share/nano/sh.nanorc" 
include "/usr/share/nano/php.nanorc"

Save the changes in the file and Close the editor using the key‐strokes  Ctrl ‐ O  and then  Ctrl ‐ X .

Tree ‐ A Directory Organization Tool

This comes by default on many other types of Linux servers but for some reason not with Red Hat / CentOs, yet is nice tool to have on hand for
sysadmins. It displays a tree of directories and files, which is useful to visualize large directory trees and for producing documentation with.

$ sudo yum install tree

The tree of directories and files are shown like this:

$ tree /etc/yum 
/etc/yum 

Server Build ­ 

/etc/yum 
├── fssnap.d 
├── pluginconf.d 
│   ├── fastestmirror.conf 
│   └── langpacks.conf 
├── protected.d 
│   └── systemd.conf 
├── vars 
│   └── infra 
├── version‐groups.conf 
├── yum‐cron.conf 
└── yum‐cron‐hourly.conf 

4 directories, 7 files

Figlet ‐ Large Character Display

Figlet converts text into large characters that are made up of ordinary screen characters. It is mostly just a fun tool to have for making banners.

Install it like this:

$ sudo yum install figlet

Have some fun ‐ try this:

```bash
$ figlet "Hello, World" 
 _   _      _ _         __        __         _     _  
| | | | ___| | | ___    \ \      / /__  _ __| | __| | 
| |_| |/ _ \ | |/ _ \    \ \ /\ / / _ \| '__| |/ _` | 
|  _  |  __/ | | (_) |    \ V  V / (_) | |  | | (_| | 
|_| |_|\___|_|_|\___( )    \_/\_/ \___/|_|  |_|\__,_| 
                    |/
```

Or something a little more complex with embedded string delimiters and a special execute‐in‐place character "!":

```
$ cat <<EOF | figlet 
Hi y'all! 
EOF 

 _   _ _         _       _ _ _  
| | | (_)  _   _( ) __ _| | | | 
| |_| | | | | | |/ / _` | | | | 
|  _  | | | |_| | | (_| | | |_| 
|_| |_|_|  \__, |  \__,_|_|_(_) 
           |___/

```

Why do we need to do it like this? Read all about it in the section on the BASH shell.

System Diagnostic Tools

Install HTOP

HTOP is a server performance viewer with a rich set of features

Installation

```$ sudo yum ‐y install htop```

Usage

Test it with the command:

```$ htop```

This utility displays the following useful metrics:

Server uptime
CPU usage
Memory usage
Details of currently‐running processes

It is possible to arrange the order of display using the function key shortcuts. Hit F10 or ‘Q’ to quit.

Install LYNX

LYNX is a text‐based browser that you can run through a browser. It supports most browser features like cookies, however it does not support
JavaScript and since it is a text‐based browser, it also does not show graphic images but just leaves a hint that there is a graphic on a page, based
on the <code>alt­tag.

It is useful for validating firewall configurations and for crude screen­scraping operations from other websites.

Installation

Simple!

```$ sudo yum  ‐y install lynx```

Usage

Server Build ­ 

Usage

Test it with the command:

```$ lynx http://your-domain```

 - which should display a text-like rendition of your website.

Network Diagnostic Tools

Warning
The installation of these tools on servers can make the servers be used to attack other devices on the Internet, should contol of the servers end up in the wrong hands. If
in doubt, do not install these tools, or at least un­install them when finished using them.

NMAP is a used to probe a remote server for various information, including what operating system it is running and what ports are open.

Installation

```$ sudo yum install nmap```

Usage

Examples:

Check to see if MySQL/MariaDB access is allowed over a network connection on the database server mdb02:

```bash
$ nmap ‐p 3306 mdb02 

PORT     STATE    SERVICE 
3306/tcp closed   mysql 
```

We can see that this port is 'closed', which means that it is not possible to access a MySQL database from anywhere other than from the database server itself. This
would of course present a problem to the webserver since it is hosted on a different device.

Check to see what ports are open over a network connection on the database server mdb02:

```
$ nmap  mdb02 

Not shown: 995 filtered ports 
PORT     STATE SERVICE 
21/tcp   open  ftp 
22/tcp   open  ssh 
80/tcp   open  http 
443/tcp  open  https 
8443/tcp open  https‐alt 
```

Install NTOP (Next Generation)

NTOP is a used to view network loading and bandwidth consumption.

More details:

http://www.ntop.org/
http://redis.io/

Installation

This installation guide covers RedHat 7.x only.

Create a special repository file for NTOP and add the following details to it:

  
```$ sudo nano /etc/yum.repos.d/ntop.repo```

```bash
[ntop] 
name=ntop packages 
baseurl=http://www.nmon.net/centos‐stable/$releasever/$basearch/ 
enabled=1 
gpgcheck=1 
gpgkey=http://www.nmon.net/centos‐stable/RPM‐GPG‐KEY‐deri 
[ntop‐noarch] 
name=ntop packages 
baseurl=http://www.nmon.net/centos‐stable/$releasever/noarch/ 
enabled=1 
gpgcheck=1 
gpgkey=http://www.nmon.net/centos‐stable/RPM‐GPG‐KEY‐deri
```

Save and exit  Ctrl ­ O ,  Ctrl ­ X .

Update all the repositories

  
$ sudo yum ‐y update

Install the necessary packages:

  
$ sudo yum ‐y install redis ntopng 
$ sudo yum ‐y install hiredis‐devel

Configuration of NTOP

Basic configuration

Server Build ­ 

This will remove all warnings that we are 'only' running the "Community Edition". Add the following to the file /etc/ntopng/ntopng.conf:

  
$ sudo nano /etc/ntopng/ntopng.conf 

‐G=/var/tmp/ntopng.pid\ 
‐‐community

Set up the services

The service redis and ntopng need to started and the set to restart again when the server is rebooted:

  
sudo systemctl start redis.service 
sudo systemctl enable redis.service

  
sudo systemctl start ntopng.service 
sudo systemctl enable ntopng.service

Opening up the firewall Configuration for NTOP

This opens up port 3000 so that it can be accessed from other devices.

  
sudo firewall‐cmd ‐‐permanent ‐‐add‐port=3000/tcp 
sudo firewall‐cmd ‐‐reload

Usage

Test it by pointing your browser to this server over port 3000.

If this does not work, then try to browse directly from the server to the ntopng service using the lynx text­based browser, which should look like this.

$ lynx http://localhost:3000 

Welcome to ntopng 

   ____________________ ____________________ 
   (BUTTON) Login 

   © 1998‐2016 ‐ ntop.org 
   ntopng is released under GPLv3

By default, the access criteria is admin, admin. Change the password immediately to something more secure.

Nethogs

Use this tool to see which processes consume the most TCP­protocolled bandwidth. It is similar to HTOP, and lists processes in order of bandwidth consumption.

Installation

$ sudo yum ‐y install nethogs

Use

Specify the network interface for which bandwidth needs to be monitored. For a virtual servers, this is normally venet0, for tin servers this is either eth0, eth1. For Wifi
interfaces, this can be wlan0 or ath0 or something else. Check the network device names for the server in /proc/net/dev:

$ cat /proc/net/dev 
Inter‐|Receive                                                       |Transmit 
 face |bytes        packets errs drop fifo frame compressed multicast|bytes      packets errs drop fifo colls carrier compressed 
    lo: 1539420091  6908499    0    0    0     0          0         0 1539420091 6908499    0    0    0     0       0          0 
venet0: 97709451743 75682952   0    0    0     0          0         0 2856837870 32029423   0    0    0     0       0          0

Priviledged execution is required, so run this under sudo:

$ sudo nethogs venet0

Server Build ­ 

To quit, hit  Ctrl ­ C .

Install Internet forensic tools

We need tools such as whois, dig and other tools to help determine the source of web­based attacks.

Installation

$ sudu yum ‐y install whois 
$ sudo yum ‐y install bind‐utils 
$ sudo yum ‐y install tcpdump

Usage

Read one of the many dodgy books on hacking. This is a big subject area.
Application Diagnostic Tools

ShellPic – a tool for viewing images on a text terminal

Instead of having to view image files on the server via an SSH tunnel, SCP’ing it to a desktop client first, or viewing in on a web browser (not always possible), it is
possible to view a low­fidelity image directly on the terminal. This is very useful for quick verifications that the correct images are where they should be. Bear in mind
that what you see will not provide any indication of the quality of the image, however.

Installation

To install thia utility, some system libraries and Python development libraries are required:

$ sudo yum ‐y install libjpeg‐devel 
$ sudo yum ‐y install python‐devel 
$ sudo yum ‐y install python‐pip

Then the Python Imaging Library library Pillow needs to be installed using Python's package manager pip:

$ sudo pip install pillow

Note that Pillow replaces the legacy PIL library. Do not use PIL (Python Image Library) any more.

The source code for shellpic is pulled from its GIT repository:

$ cd ~/git 
~/git $ git clone https://github.com/larsjsol/shellpic.git 
~/git $ cd shellpic 
~/git $ sudo python setup.py install

Installation errors or warnings

You might get an error message like this:

You should consider upgrading via the 'pip install ‐‐upgrade pip' command.

So do it!

$ sudo pip install ‐‐upgrade pip

Usage

You should be able to get a good but low­fidelity indication of what an image contains by viewing it on the terminal with the command:

$ shellpic [image_path]

For example:

Server notification email set­up

System notification events need to be communicated from the server to a real user via email. By default, system emails are sent to the internal user root, which needs
to be passed to a real email address sysadmin@matchi.biz.

The /etc/aliases file

Edit the file /etc/aliases and set the real email addresses up for all server accounts, which all point to root, as sysadmin@matchi.biz.

# Person who should get root's mail 
root:   sysadmin@matchi.biz

The result of this is that all system alerts emailed from the server end up in the same email address at sysadmin@matchi.biz, and the server that emitted the alert is
identifiable from the friendly server name that appears in the recipient email address, e.g. sysadmin@matchi.biz.

Install the PostFix Mail server

Only install for RedHat / Centos 6.x Virtual Servers

Do this if the /etc/postfix directory does not yet exist.

# yum ‐y install postfix

The /etc/postfix/main.cf file

Server Build ­ 

Add or replace the following lines to the file, and amend this according to the 'friendly server name', which in this case is mweb01:

myhostname = mweb01.matchi.biz 
myorigin = $myhostname

Manage the Postfix Server

Restart the Postfix server:

On RedHat 6.x, do this:

$ sudo /etc/init.d/postfix restart 
Shutting down postfix:                                     [FAILED]    
Starting postfix:                                          [  OK  ]

Set the service so that it will automatically start each time the server is booted up:

$ sudo chkconfig ‐‐levels 2345 postfix on

On red Hat 7.x, Postfix will already be running. You can check it:

$ sudo systemctl status postfix 
● postfix.service ‐ Postfix Mail Transport Agent 
   Loaded: loaded (/usr/lib/systemd/system/postfix.service; enabled; vendor preset: disabled) 
   Active: active (running) since ...

Testing emailing from the server

Test the email capability on each server by sending an email from the server's console:

$ mail ‐s 'test' root <<!                        
This is a test. 
!

Assuming that this test was done from server mapp02, then an email addressed to sysadmin+mapp02@matchi.biz should arrive at the inbox sysadmin@matchi.biz.
Setting up Secure Shell (SSH) channels between the servers

The simplest and most secure method to transfer files from one server to another is via SSH secure shell. While password­based access may still be possible a this
stage, you can connect to a server and enter the password when prompted for it. However, for any automated process such as file transfers, a password­less approach is
required, and to achieve this we use a public/private key pair.
Creating the public­private key­pair

For each server we create a key­pair:

madman@s16972616 mweb1 ~ $ ssh‐keygen ‐t rsa 
Generating public/private rsa key pair. 
Enter file in which to save the key (/home/myname/.ssh/id_rsa) 
Enter passphrase (empty for no passphrase):  
Enter same passphrase again:  
Your identification has been saved in id_rsa. 
Your public key has been saved in id_rsa.pub. 
The key fingerprint is: 
03:5f:9f:fa:0d:47:33:6f:ca:bf:ee:15:67:c3:9f:09 
The keys randomart image is: 
+‐‐[ RSA 1024]‐‐‐‐+ 
|                 | 
|                 | 
|      .   .      | 
|       o . . ..  | 
|        S   oE++o| 
|         . . ..=B| 
|          . . .o=| 
|           . = o.| 
|            . *=o| 
+‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐+

Desimating the public key to target servers

Note
Only do this between servers where there SSH file transfers and SSH terminal sessions are likely to occur.

Now add the public key of each server to the key ring of all the other servers.

If password­based authentication is still enabled on the target server, use the BASH shell to pipe the public key over SHH. You will be prompted for a password one
final time on each server. Do this on all 3 servers, changing the target server each time. Here we distribute the public key of server web01 to servers mapp01 and
mdb01:

madman@mweb01 ~ $ cat ~/.ssh/id_rsa.pub | ssh mapp01 'cat >> ~/.ssh/authorized_keys' 
RSA key fingerprint is e6:f1:c4:66:b6:a2:38:86:8b:61:9b:73:74:34:0f:c6. 
Are you sure you want to continue connecting (yes/no)? yes 
madman@mapp01s password:  
madman@mweb1 ~ $ cat ~/.ssh/id_rsa.pub | ssh mdb01 'cat >> ~/.ssh/authorized_keys' 
RSA key fingerprint is e6:f1:c4:66:b6:a2:38:86:8b:61:9b:73:74:34:0f:c6. 
Are you sure you want to continue connecting (yes/no)? yes 
madman@mdb01s password:

There is an even more elegant way of doing this with a single command:

madman@mweb01 ~ $ ssh‐copy‐id i ~/.ssh/id_rsa.pub mapp01  
madman@mapp01s password:

If password­based access via SSH has already been disabled to the target server, the public key of the new server can only be distributed from a device that is already
able to connect to the older servers, by copying and pasting the public key into the file .ssh/authorized_keys using a text editor.

Securing the Secure Shell (SSH) Service

Securing the Secure Shell (SSH) Service

Server Build ­ 

Use the nano editor (if it already installed) or vi (installed by default) to edit the /etc/ssh/sshd_config file in order to secure the SSH service to achive the following
objectives:

The user 'root' can never log in remotely. Trying to log in as user root is a favourite attack vector, since every UNIX­based server has this user account.
Only the specified user 'madman' can ever log in, even if there are other user accounts on the server (which there are ­ see the content of the /etc/passwd file)
Password­based authentication is not possible and it is only possible to log in through the use of a public/private key­pair
Add a warning banner to all those who attempt to log in to the server

$ sudo nano /etc/ssh/sshd_config 
... 
PasswordAuthentication no 
PermitRootLogin no 
AllowUsers madman 
Banner /etc/warning 
...

Save and Close the /etc/ssh/sshd_config file ( Ctrl ­ O ,  Ctrl ­ X ).

Secure Shell (SSH) Warning Banner

Warning Banner will display a no­trespassing warning message at the start of each SSH session. If password authentication were enabled, then this would be displayed
even before the user is prompted for a password. This message will not deter a persistent adversary, but it does cause some basic attack scripts to break and it is also
useful from a legal point of view to support the eventual prosecution of persistent attackers. It is not advised to keep this message simple and to not give too much
information away about the server, the business or the people involved in this message. Create this standard message in the /etc/warning file:

$ sudo nano /etc/warning 
[sudo] password for madman: 
############################################################################## 
# You are entering a secured and monitored area.                             # 
# Your IP, login time and username have now been noted.                      # 
# This service is restricted to authorized users only.                       # 
# All activities on this system are logged.                                  # 
# Unauthorized access will be reported to relevant law enforcement agencies. # 
# Disconnect immediately if you are not an authorized user.                  # 
##############################################################################

Save and Close the /etc/warning file ( Ctrl ­ O ,  Ctrl ­ X ).

These changes need to be effected ("actualized") on the server by restarting the SSH daemon. Open up another SSH terminal to the server as a failover before you
perform the next step, in case something goes wrong and you do not completely loose your way to the server. Restart the SSH service to make these changes effective
as follows:

On RedHat 6.x, do this:

$ sudo /etc/init.d/sshd restart 
[sudo] password for madman: 
Stopping sshd:                                             [  OK  ] 
Starting sshd:                                             [  OK  ]

On RedHat 7.x, do this:

$ sudo systemctl restart sshd 
[sudo] password for madman:

Test your settings:

Try to login as user root:

[mydesktop] $ ssh root@mweb02 
Permission denied (publickey,gssapi‐keyex,gssapi‐with‐mic).

This is the desired results and already makes the server safe from a substantial part of the adversaries.

Try to login as user madman from a device that does not have its public installed on this server:

[mydesktop] $ ssh madman@mweb02 
Permission denied (publickey,gssapi‐keyex,gssapi‐with‐mic).

Again, this is the desired results and already makes the server safe from another substantial part of the adversaries, who will attempt to run a dictionary attack.

Now open a new SSH session to ensure that the configuration changes are correct. If it turns out to be impossible to now connect to the target server from the new
terminal, use the previously­opened fail­over session to recover from this situation by checking for possible errors in the /etc/ssh/sshd_config configuration file.

Work­around for the X11­based warning message:

if you encounter the warning message xauth: file .Xauthority does not exist, the workaround is to leave X11­forwarding over SSH enabled (even though we don't
serve X11 here). Install the Xauthority package and set up an empty ~/.Xauthority file:

$ sudo yum ‐y install xauth 
$ touch ~/.Xauthority

Add a Welcome Message

This is a message that will only be displayed after a user has successfully logged on via an SSH session in a terminal, and displays the text in the file /etc/motd.
(“motd” stands for “Message Of The Day”). By default, this file is blank as it is not essential. However, we use it here as it is useful to system administrators who are
reminded which server it is that they have just logged on. It will be display whenever to log in like this:

$ ssh madman@server 
... Display of the welcome message ... 
... Do stuff on the server ...

If you don't want to see the welcome message, or your are logging in as part of a batch process, redirect the STDERR (file handle #2) to the null device:

$ ssh madman@server 2>/dev/null 
... Do stuff on the server ...

Utilities, such as fortune exist that can randomly select and put a prithy little quote in the welcome message.

Manual creation of the /etc/motd file:

Manually edit the /etc/motd file with NANO (or VI if you are well­hard):

$ sudo nano /etc/motd 
[sudo] password for madman:

Server Build ­ 

Have some fun and make a pretty welcome message. Generate some ASCII­text using this tool: http://patorjk.com/software/taag and then copy and paste the result into
your edit on your terminal. Or copy this text below:

########################################################        
#       Welcome to another happy server of             # 
#  __  __    _  _____ ____ _   _ _   _     _           # 
# |  \/  |  / \|_   _/ ___| | | (_) | |__ (_)____      # 
# | |\/| | / _ \ | || |   | |_| | | | '_ \| |_  /      # 
# | |  | |/ ___ \| || |___|  _  | |_| |_) | |/ /____   # 
# |_|  |_/_/   \_\_| \____|_| |_|_(_)_.__/|_/_______|  #  
#                                                      # 
########################################################

Save and Close the file.

Programatic creation of the /etc/motd file:

Use figlet to create large text. Sudo to root­user first:

$ sudo su ‐ 
[sudo] password for madman:  
# echo "Welcome to " > /etc/motd 
# figlet "mweb02" >> /etc/motd                 
# echo "Another happy and secure server from" >> /etc/motd              
# figlet "matchi.biz" >> /etc/motd 
# exit 
$

This is what it will look like ­ use the cat­command to list the content of the file:

# cat /etc/motd 
Welcome to             _      ___ ____   
 _ __ _____      _____| |__  / _ \___ \  
| '_ ` _ \ \ /\ / / _ \ '_ \| | | |__) | 
| | | | | \ V  V /  __/ |_) | |_| / __/  
|_| |_| |_|\_/\_/ \___|_.__/ \___/_____| 
                                         
Another happy and secure server from 
                 _       _     _   _     _      
 _ __ ___   __ _| |_ ___| |__ (_) | |__ (_)____ 
| '_ ` _ \ / _` | __/ __| '_ \| | | '_ \| |_  / 
| | | | | | (_| | || (__| | | | |_| |_) | |/ /  
|_| |_| |_|\__,_|\__\___|_| |_|_(_)_.__/|_/___|

Security Services

It is necessary to install a few additional processes that actively prevent attacks or at least let you know that your server may have been attacked, to allow you to take
the necessary action.
FAIL2BAN

Ban unwelcome IP addresses that attempt to connect via SSH. This defence layer is in addition to the defence layer that the data centre itself offers.
Warning
Do not solely rely on the defence systems of others! In particular, the data centre's defence system is very weak. This is why we need to bolster our own local defenses
here.

It is possible to ban unwelcome IP address from known adversaries and annoyances at the server level through the use of the fail2ban daemon, which adds the IP
addresses to the server's firewall configuration, such that the IP addresses are simply ignored. Although it is far more optimal to ban IP addresses at the network switch
level, only a server­based process is able to determine when an IP address repeatedly fails to log in to a server via SSH. We set this process so that 1 failed attempt to
establish an SSH session from a given IP address will ban the IP address for a very long time.

The Symptoms

Here is how you know that your server is under attack and to find out what the attackers' IP addresses are:

You get notified when you log in

$ sudo su ‐ 
[sudo] password for madman:  
Last login: Mon Feb 23 12:43:38 SAST 2015 on pts/0 
There were 15326 failed login attempts since the last successful login.

$ sudo su  ‐ 
# grep Failed /var/log/secure 
... 
# grep Failed /var/log/secure | awk '{print $11}' | sort ‐u  
...

Most of these IP addresses originate from the Chinese mainland. Pick one of the IP addresses above to check:

address:        INT'L TOWER 707‐713 NATHAN RD MONGKOK  KLN HONG KONG, hongkong KLN 999077 
address:        TOWER 707‐713 NATHAN RD MONGKOK KLN HONG KONG

Installation

Fail2Ban is not part of the Red Hat Linux distribution, so it needs to be installed from the EPEL third­party library. First, check that this product is actually in the 3rd­
party repository:

Install Fail2Ban using yum:

$ sudo yum ‐y install fail2ban 
... 
Total download size: 867 k 
Installed size: 3.0 M

This installs all the dependencies and the eventual package.

Configuration

We configure the Fail2Ban daemon to:

Server Build ­ 

Ban all IP addresses that failed in their attempt to connect to the server over the SSH port
Banned IP addresses are banned for a duration of 24 hours (86400 seconds)
Send all banning notifications to root@localhost. The configuration of the /etc/aliases file will identify which server this notification originated from.

Edit the /etc/fail2ban/jail.local file, which will override any default settings in the /etc/fail2ban/jail.conf file. We may need to add future overrides of other
protocols in the /etc/fail2ban/jail.conf file later on as we discover other types of attacks on the server.

$ sudo nano /etc/fail2ban/jail.local

Add the following overrides:

[DEFAULT] 
bantime = 84600 
findtime = 600 
maxretry = 1

Save and Exit.

Add a check specifically for the SSH protocol with the /etc/fail2ban/jail.local file:

$ nano /etc/fail2ban/jail.d/sshd.local

Add the following :

[sshd] 
enabled = true 
port = ssh 
#action = firewallcmd‐ipset 
logpath = %(sshd_log)s 
maxretry = 5 
bantime = 86400

Save and Exit.

Starting the Service

Start the Fail2Ban service and also make it self­start on server boot:

On RedHat 6.x:

$ sudo service fail2ban start 
Starting fail2ban:                                         [  OK  ] 
$ sudo chkconfig ‐‐add fail2ban

Also, restart the IPTables firewall service. This also flushes all banned IP addresses, so only do this once after the installation of Fail2Ban is completed:

$ sudo service iptables restart && service iptables status 
iptables: Flushing firewall rules:                         [  OK  ] 
iptables: Setting chains to policy ACCEPT: nat mangle filte[  OK  ] 
iptables: Unloading modules:                               [  OK  ]

On RedHat 7.x:

$ sudo systemctl start fail2ban 
$ sudo systemctl enable fail2ban

The firewall service on Centos/RedHat 7.x is called firewalld' and does not need to be restarted.

Check which IP adddresses have been banned

Check which IP addresses have been banned. Nothing will show if you have just previously flushed the banned IP addresses:

$ sudo  iptables ‐L ‐‐line‐numbers | grep DROP 
1    DROP       all  ‐‐  host86‐142‐19‐185.range86‐142.btcentralplus.com  anywhere             

Line 1 shows the IP address of an experimental ban. It is possible to unban IP addresses if there genuinely was a valid reason for the failed login attempts, as follows,
including a check that this IP address does not get DROP’ed by the firewall:

Unban trusted IP­addresses

If the banned IP address is known to be a friendly one (i.e. someone you trust may have accidentally used the incorrect access criteria in succession), then you can
unban their IP adddress:

or 

sudo  iptables ‐L ‐‐line‐numbers | grep DROP

You will know that your IP address has been banned when you get a message like this when remotely trying to log in:

$ ssh [user]@[server] 
ssh: connect to host [server] port 22: Connection refused

Note
If you find that your IP address has been banned but it does not appear on iptable's DROP list, then it has been restricted by the data centre's security system. You will
need to contact the data centre and ask them to remove the IP restriction.

References: http://centoshelp.org/security/fail2ban/

RKHUNTER (Rootkit Hunter)

Installation

This process checks that no Rootkits have been installed in on the server. In the unlikely event that it finds one, it sends and email alert to the system administrator.
Install it as follows:

$ sudo yum  ‐y install rkhunter

Server Build ­ 

This installation adds a job to the list of other daily batch processes. Daily batch jobs start their execution at 4:05 am UTC and can be be viewed like this:

$ ls /etc/cron.daily/ 
... 
rkhunter

Cron jobs are performed in sequence and in alpha­numeric order, which is the same order that the ls command lists files.

The final step in setting up the rootkit hunter is to establish a reference of file hashes, against which all system files are be compared to on a daily basis:

$ sudo rkhunter ‐‐propupd 
[sudo] password for madman:  
File created: searched for 167 files, found 137

Using RKHUNTER to scan the server

This step is performed by the daily cron process, and can manually be performed at any time.

$  sudo rkhunter ‐c ‐‐report‐warnings‐only

You should not get any alerts after a fresh server install.

Dealing with RKHUNTER Alerts

You may receive the following notification email if either:

The operating system was updated or patched
The operating system has been compromised

Subject: [rkhunter] Warnings found for s16972617 
Please inspect this machine, because it may be infected. 

This is followed by a more descriptive alert notification:

File size has changed

And a following­on email notification that either the size or the file­hash has changed, e.g.

Subject: rkhunter Daily Run on [server] 
‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐ Start Rootkit Hunter Scan ‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐ 
Warning: The file properties have changed: 
         File: /usr/bin/size 
         Current inode: 184336503    Stored inode: 233033071 
Warning: The file properties have changed: 
         File: /usr/bin/strings 
         Current inode: 184336504    Stored inode: 233032818 
‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐ End Rootkit Hunter Scan ‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐ 

In this case it means that the 2 files in question where relocated on the storage device but were not actually changed, so we can safely mute this alert.

File's inode has changed

Subject: rkhunter Daily Run on [server] 
‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐ Start Rootkit Hunter Scan ‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐ 
Warning: The file properties have changed: 
         File: /usr/bin/curl 
         Current inode: 233045587    Stored inode: 233039515 
‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐ End Rootkit Hunter Scan ‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐ 

This occasionally happens on virtual machines that use SANs. We can safely mute this alert.

File Hash has changed

Another case is where the file hash has been changed. This means that the content of the file has been altered but the size remains unchanged:

Warning: The file properties have changed: 
         File: /usr/bin/chattr 
         Current hash: 5c8123ff9c92c6a361b465517c397a699670bba8 
         Stored hash : d327e24dbddacbd6f39c54619abf695fcbeb386f6419246b73299c0d3d7928ff 

Investigate which RPM package this file belongs to:

$ sudo rpm ‐qf /usr/bin/chattr 

Check if the file has been changed since that RPM packages was installed. A null response means that there are no changes.

$ sudo rpm ‐Vf /usr/bin/chattr

If still in doubt, re­install the RPM package:

...

It should now be safe to mute the alert. See the next step.

Muting RKHUNTER Alerts

If you are sure that there are no real issues, then the list of file hashes can be refreshed:

$ sudo rkhunter ‐‐propupd 
File updated: searched for 167 files, found 138

Warning
All RKHUNTER alerts should be thoroughly investigated and understood before muting them.

Permanently removing annoying RKHUNTER alerts

Unscheduled updates of the PLESK server management system cause harmless and false alerts, but they are annoying. There are a few other alerts that can be safely
ignored too. Stop these alerts by making the following configuration changes:

$ sudo nano /etc/rkhunter.conf

Server Build ­ 

$ sudo nano /etc/rkhunter.conf

At line 309:

ALLOW_SSH_ROOT_USER=no

At line 359:

ENABLE_TESTS="all" 
DISABLE_TESTS="suspscan hidden_procs deleted_files packet_cap_apps apps loaded_modules"

At line 825, comment this line out:

# XINETD_ALLOWED_SVC=/etc/xinetd.d/echo

Add this if the server is supported by PLESK:

# Matchi sysadmin says: Add this if your server is supported by PLESK 
XINETD_ALLOWED_SVC=/etc/xinetd.d/ftp_psa 
XINETD_ALLOWED_SVC=/etc/xinetd.d/poppassd_psa 
XINETD_ALLOWED_SVC=/etc/xinetd.d/smtp_psa  
XINETD_ALLOWED_SVC=/etc/xinetd.d/smtps_psa 
XINETD_ALLOWED_SVC=/etc/xinetd.d/submission_psa

Setting the System Clock

It is important that the clocks on all servers are synchronized so that the time­stamped logging of information between servers is consistent. The NTP Daemon is used
to synchronize the server's clock to an atomic clock.

Virtual Servers vs Physical Servers

Running the NTP Daemon on a Virtual Machine is not possible since the time clock for all guest virtual machines is owned by the hosting VM hypervisor (Virtuozzo
in our case). The VM hypervisor itself is synchronized to an atomic clock, so therefore all virtual servers are synchronized too. It is also not possible to set the clock
time manually on a virtual server. The only thing that can be set is the particular virtual server's time zone.

Network Time Protocol Service

Only do this on a dedicated (tin) server:

The Network Time Protocol Daemon ensures that the server is synchronized to a remote atomic clock using the NTP network time protocol. This protocol includes
triangulation algorithms that compensate for the latency in the actual network delay over which the time signal is sent. If all servers are synchronized to an atomic
clock, then they will be synchronized with each other. By default, the servers have all the configurations set up to the external atomic clocks. All that is required, is to
install and start the NTP daemon and to set the daemon that it restarts should the server ever get rebooted:

$ sudo yum ‐y install ntp ntpdate ntp‐doc 
... 
$ sudo /etc/init.d/ntpd start 
Starting ntpd:                                             [  OK  ] 
$ sudo chkconfig ‐‐levels 2345 ntpd on

This will gracefully change the clock on the server to the correct time.

Manually Changing the Server's Wall­Clock Time

On a physical server, and for testing purposes usually, you can also force a server time change by manually turning the NTPD service and then changing the time and
date with this command:

$ sudo date ‐s 'Mon Nov 17 11:14:21 UTC 2013'

More about the date command can be found with this command:

$ man date

Remember to turn the NTPD service back on again when testing is completed ­ this will gracefully change the wall­clock time to the correct time.

Setting the Server's Time Zone

Do this on both Virtual or Physical servers:

Check your server's current Wall­Clock time zone:

$ date 
Fri Apr 22 05:21:56 CDT 2016

In this case it is CDT (Central Dailight Time in the USA ­ Wisconsin etc...). All Matchi's servers are set to 'Europe/London', which means that depending on when you
run the date command, you either get BST (British Summer Time) or GMT (Greenwich Mean Time).

All possible timezone supported by UNIX are in /usr/share/zoneinfo/ ­ there are more than 1700 of them. We are interested in the file
/usr/share/zoneinfo/Europe/London that contains everything that needs to be known about clocks in London, birthplace of time and also the coolest city in the world.

Remove the current symbolic link at /etc/localtime and re­point it to the correct timezone definition file:

$ sudo rm ‐fr /etc/localtime 
$ sudo ln ‐s /usr/share/zoneinfo/Europe/London  /etc/localtime

Check that you now get the correct time zone:

$ date 
Fri Apr 22 11:32:43 BST 2016

You also need to update the timezone file for the local SMTP mail daemon, Postfix. Postfix does not like symbolic links, so you need to copy the actual time zone file:

$ sudo mkdir /var/spool/postfix/etc 
$ sudo cp /usr/share/zoneinfo/Europe/London /var/spool/postfix/etc/localtime 
$ sudo chown ‐R postfix /var/spool/postfix/etc

Restart Postfix for this change to take effect. For RedHat 6.x, do:

$ sudo /etc/init.d/postfix restart 
Shutting down postfix:                                     [  OK  ] 
Starting postfix:                                          [  OK  ]

For RedHat 7.x, do:

$ sudo systemctl restart postfix

Server Build ­ 

From this point onwards, all date­based calculations will be based on this time zone.
TRIPWIRE

Tripwire is an intrusion detection system (IDS) that monitors critical system files on the server and alerts if they have been destroyed or modified by an adversary, or
by mistake. It allows the system administrator to know immediately what was compromised on the system to be able to repair it. The first time Tripwire is run, it stores
checksums, exact sizes and other data of all the selected files in a database. The successive runs check whether every file still matches the information in the database
and report all changes.

This has not yet been installed on the servers.
Server Mail Services

Emails sent from servers, whether they are customer notification emails or system alerts, are all routed through Google GMail service using the email domain of
'matchi.biz'. This improves the chances that emails will be delivered, in particular, where the target recipient's email host has been poorly configured. Furthermore, the
MX domain 'matchi.biz' has its domain key registered (DKIM) and further supports deliverability of emails to spam­adverse recipients. To achieve this, the default
mail delivery configuration of Postfix needs to be converted into a mail relay. To use GMail as the end delivery host, some stringent authentication settings need to be
set.

The email address and Google account that forms the core of Matchi's automated system emailing is sysadmin@matchi.biz. This is a 'real' account on Google Apps.

Setting up the Google Authentication

Add the following to the file /etc/postfix/sasl_passwd, where XXXXXX is the password that was set for the sysadmin@matchi.biz account on Google Appls. Note that
the square brackets are required:

[smtp.gmail.com]:587 sysadmin@matchi.biz:XXXXXXXX

Convert the file into 'database file' that is readable by Postfix:

$ cd /etc/postfix 
$ sudo postmap sasl_passwd

Setting up the TLS Certficated

Create file /etc/postfix/tls_policy containing this text:

[smtp.gmail.com]:587 encrypt

Convert the file also into 'database file' that is readable by Postfix:

$ cd /etc/postfix 
$ sudo postmap tls_policy

Set up the SMTP Relay

Add the following to the file /etc/postfix/main.cf, and replace SERVERALIAS with the friendly server name, e.g. mweb01, mapp01, etc...

myhostname = SERVERALIS.matchi.biz 

relayhost = [smtp.gmail.com]:587 

smtp_sasl_auth_enable = yes 
smtp_sasl_password_maps = hash:/etc/postfix/sasl_passwd 
smtp_sasl_security_options = noanonymous 
smtp_sasl_tls_security_options = noanonymous 
smtp_sasl_mechanism_filter = plain 

# TLS parameters 
smtp_use_tls = yes 
smtp_tls_CAfile = /etc/ssl/certs/ca‐bundle.crt 
smtpd_use_tls = yes 
smtpd_tls_session_cache_database = btree:${data_directory}/smtpd_scache 
smtp_tls_session_cache_database = btree:${data_directory}/smtp_scache 
smtp_tls_note_starttls_offer = yes 
smtp_tls_policy_maps = hash:/etc/postfix/tls_policy 

# Debugging & Logging 
debug_peer_list=smtp.gmail.com 
debug_peer_level=2

Restart the Postfix Service

Restart the Postfix Service to actualize the settings:

$ sudo /etc/init.d/postfix restart 
Shutting down postfix:                                     [  OK  ] 
Starting postfix:                                          [  OK  ]

Test the SMTP Relay

Send a text email from the server to a test account and check that it arrives. Also look at the internal message details and ascertain that it arrived Google's GMail SMTP
service, smtp.gmail.com.

$ mail ‐s 'Test for new Postfix configuration' test@matchi.biz <<! 
This is a test 
!

Securing the Server

The attack surface of the server needs to be reduced to a minimum. A simple way to achieve this (for now) is to keep the services that need to be accessed from the
public internet to a minimum. You can view the open ports of a server from the outside world by running the nmap command from your local machine. In this example,
the attack surface is larger than what it needs to be, with too many services running and potentially causing a vulnerability:

Server Build ­ 

$ nmap [server] 

Nmap scan report for [server] 
Not shown: 985 closed ports 
PORT     STATE SERVICE 
21/tcp   open  ftp 
22/tcp   open  ssh 
25/tcp   open  smtp 
53/tcp   open  domain 
80/tcp   open  http 
106/tcp  open  pop3pw 
110/tcp  open  pop3 
143/tcp  open  imap 
443/tcp  open  https 
465/tcp  open  smtps 
587/tcp  open  submission 
993/tcp  open  imaps 
995/tcp  open  pop3s 
3306/tcp open  mysql 
8080/tcp open  http‐proxy 
8443/tcp open  https‐alt

Services that we definitely will never require are IMAP and POP services, so we can stop them on Red Hat 6.x as follows:

$ cd /etc/init.d 
$ sudo ./courier‐imapd stop 
[sudo] password for madman:  
Stopping Courier IMAP server:                              [  OK  ] 
$ sudo ./courier‐imaps stop 
Stopping Courier IMAP server with SSL/TLS support:         [  OK  ] 
$ sudo ./courier‐pop3d stop 
Stopping Courier POP3 server:                              [  OK  ] 
$ sudo ./courier‐pop3s stop 
Stopping Courier POP3 server with SSL/TLS support:         [  OK  ]

On Red Hat 7.x use the systemctl command.

We then also ensure that these services will not be restarted when the server is rebooted, but permanently turnining then off, again for RedHat 6.x:

$ sudo chkconfig courier‐imapd off 
$ sudo chkconfig courier‐imaps off 
$ sudo chkconfig courier‐pop3d off 
$ sudo chkconfig courier‐pop3s off 
$ sudo chkconfig courier‐authdaemon off

On Red Hat 7.x use the systemctl command:

$ sudo systemctl disable courier‐imapd 
$ sudo systemctl disable courier‐imaps 
$ sudo systemctl disable courier‐pop3d 
$ sudo systemctl disable courier‐pop3s 
$ sudo systemctl disable courier‐authdaemon

You can view a summary of services that will start if the server is rebooted ­ for Red Hat 6.x:

$ chkconfig | grep on 

cgconfig        0:off   1:off   2:off   3:off   4:off   5:off   6:off 
crond           0:off   1:off   2:on    3:on    4:on    5:on    6:off 
cups            0:off   1:off   2:on    3:on    4:on    5:on    6:off 
fail2ban        0:off   1:off   2:on    3:on    4:off   5:off   6:off 
httpd           0:off   1:off   2:off   3:on    4:off   5:off   6:off 
ipset           0:off   1:off   2:on    3:on    4:on    5:on    6:off 
iptables        0:off   1:off   2:on    3:on    4:on    5:on    6:off 
maldet          0:off   1:off   2:on    3:on    4:on    5:on    6:off 
messagebus      0:off   1:off   2:on    3:on    4:on    5:on    6:off 
modules_dep     0:off   1:off   2:on    3:on    4:on    5:on    6:off 
netconsole      0:off   1:off   2:off   3:off   4:off   5:off   6:off 
netfs           0:off   1:off   2:off   3:off   4:on    5:on    6:off 
network         0:off   1:off   2:on    3:on    4:on    5:on    6:off 
nfslock         0:off   1:off   2:off   3:on    4:on    5:on    6:off 
portreserve     0:off   1:off   2:on    3:off   4:on    5:on    6:off 
psa             0:off   1:off   2:on    3:on    4:on    5:on    6:off 
rabbitmq‐server 0:off   1:off   2:on    3:on    4:on    5:on    6:off 
restorecond     0:off   1:off   2:off   3:off   4:off   5:off   6:off 
rpcbind         0:off   1:off   2:on    3:off   4:on    5:on    6:off 
rpcgssd         0:off   1:off   2:off   3:on    4:on    5:on    6:off 
rsyslog         0:off   1:off   2:on    3:on    4:on    5:on    6:off 
saslauthd       0:off   1:off   2:off   3:on    4:off   5:off   6:off 
sshd            0:off   1:off   2:on    3:on    4:on    5:on    6:off 
sw‐cp‐server    0:off   1:on    2:off   3:off   4:off   5:off   6:off 
sw‐engine       0:off   1:off   2:on    3:on    4:on    5:on    6:off 
udev‐post       0:off   1:on    2:on    3:off   4:on    5:on    6:off 
vzquota         0:on    1:on    2:on    3:on    4:on    5:on    6:on 
vzreboot        0:off   1:off   2:off   3:off   4:off   5:off   6:on 
xinetd          0:off   1:off   2:on    3:on    4:on    5:on    6:off

At the end of this rationalization of publicly­visible services, you can view which services are still visible to the public by looking at the server from your own machine
with the nmap command:

nmap [server] 

Nmap scan report for [server] 
Not shown: 989 closed ports 
PORT     STATE SERVICE 

22/tcp   open  ssh 
53/tcp   open  domain 
80/tcp   open  http 
106/tcp  open  pop3pw 
443/tcp  open  https 
465/tcp  open  smtps 
587/tcp  open  submission 
3306/tcp open  mysql 
8080/tcp open  http‐proxy 
8443/tcp open  https‐alt

Sizing the Logical Volumes on a Dedicated Server

By default, a dedicated server ('tin') comes with the logical volumes sized very small, even though there is a plenty of capacity (1TB usually). You can see the default
sizings:

$ df ‐h 
Filesystem             Size  Used Avail Use% Mounted on 
/dev/md1               4.0G  225M  3.7G   6% / 
devtmpfs               7.8G     0  7.8G   0% /dev 
tmpfs                  7.8G     0  7.8G   0% /dev/shm 
tmpfs                  7.8G   33M  7.8G   1% /run 
tmpfs                  7.8G     0  7.8G   0% /sys/fs/cgroup 
/dev/mapper/vg00‐usr   4.8G  2.4G  2.2G  53% /usr 
none                   7.8G     0  7.8G   0% /tmp 
/dev/mapper/vg00‐var   4.8G  3.5G  1.1G  78% /var 
/dev/mapper/vg00‐home  4.8G  3.8G  846M  82% /home 
tmpfs                  1.6G     0  1.6G   0% /run/user/10002 

Server Build ­ 

$ echo $(( `df ‐m | sed '1d' | awk '{print $2 "+"}' | tr ‐d '\n' | sed ‐e 's/.$//'` )) 
60242

This totals 60G, and typically we have 1000G available. The var volume is impossibly small and the home volume could also so with a little more space. To extend the
volumes and leave some space for future expansion, we do a 'physical volumne show' pvs to see how much physical storage is still available:

$ sudo pvs 
  PV         VG   Fmt  Attr PSize   PFree   

Extend the var logical volume by a further 400G:

$ sudo lvextend ‐L +400G /dev/mapper/vg00‐var  
  Logical volume var successfully resized.

Also extend the home logical volume by 50G:

$ sudo lvextend ‐L +50G /dev/mapper/vg00‐home 
  Logical volume home successfully resized.

A 'logical volume show' lvs command shows that we have been successful:

$ sudo lvs 
  LV   VG   Attr       LSize   Pool Origin Data%  Meta%  Move Log Cpy%Sync Convert 

The physical disk consumption needs to be aligned with the new logical volume sizings. We can see how these volumes are actually mounted in the operating system:

$ mount | grep var 
/dev/mapper/vg00‐var on /var type ext4 (rw,noatime,quota,usrquota,data=ordered)
$ mount | grep home 
/dev/mapper/vg00‐home on /home type ext4 (rw,noatime,quota,usrquota,data=ordered)

Both volumes use the EXT4 file system. For this file system we use the resize2fs<//code> to extend the physical volume:

$ sudo resize2fs /dev/mapper/vg00‐var 
Filesystem at /dev/mapper/vg00‐var is mounted on /var; on‐line resizing required 
old_desc_blocks = 1, new_desc_blocks = 26 
The filesystem on /dev/mapper/vg00‐var is now 106168320 blocks long. 

$ sudo resize2fs /dev/mapper/vg00‐home 
Filesystem at /dev/mapper/vg00‐home is mounted on /home; on‐line resizing required 
old_desc_blocks = 1, new_desc_blocks = 4 
The filesystem on /dev/mapper/vg00‐home is now 14417920 blocks long.

A quick check shows that we have also been successful in extending the physical volume:

$ df ‐h 
Filesystem             Size  Used Avail Use% Mounted on 
/dev/md1               4.0G  225M  3.7G   6% / 
devtmpfs               7.8G     0  7.8G   0% /dev 
tmpfs                  7.8G     0  7.8G   0% /dev/shm 
tmpfs                  7.8G   33M  7.8G   1% /run 
tmpfs                  7.8G     0  7.8G   0% /sys/fs/cgroup 
/dev/mapper/vg00‐usr   4.8G  2.4G  2.2G  53% /usr 
none                   7.8G     0  7.8G   0% /tmp 
/dev/mapper/vg00‐var   399G  3.6G  379G   1% /var 
/dev/mapper/vg00‐home   55G  3.8G   49G   8% /home 
tmpfs                  1.6G     0  1.6G   0% /run/user/10002

File Sharing between Servers

TODO: Review what directories need to be shared

File Sharing over the Network: Within the local server network, we use the Network File System (NFS) protocol to share directries.

By convention, file systems on a server that are exported to other servers are hosted off a root‐directory called ‘/exports’ and file systems from a
remote server are mounted locally on a root‐directory called ‘/mnt’.

Preparing for Content Network Delivery: A root‐directory will hold all static data so that it is easily identifiable for future mapping to content
delivery networks or other storage array systems. It is named ‘/exports/cdn/[build]’, where [build] is the ISO‐date of the production release preceded
with a prefix ‘build_’, and is created as in the following example, where the build date is 1st of June 2013: build_20130601. The directory is
prepared with the correct ownership and access rights:

madman@s16972616 mweb1 ~ $ sudo mkdir ‐p /exports/cdn/build_20130601 
madman@s16972616 mweb1 ~ $ sudo chmod –R g+w /exports/cdn/build_20130601 
madman@s16972616 mweb1 ~ $ ls ‐al /exports/cdn 
total 12 
drwxr‐xr‐x  3 root     root     4096 Jun 10 11:36 . 
dr‐xr‐xr‐x 23 root     root     4096 Jun 10 11:36 ..

Export configurations to the other servers: By sharing the relevant configuration files for read‐only use by other servers allows any changes in a
configuration to be instantly visible across the system. For file sharing within a secured environment, such as the PROD environment in a data center,
it is sufficient to share files unencrypted over NFS (Network File System) – a network protocol similar to Windows CIFS. The Content Management
System’s configuration file, configuration,php, needs to be shared from the webserver. This file resides in a directory /var/www/html/[build‐
instance], where [build‐instance] is the name of the build. As new builds are deployed, this instance name will change, and so will the actual
directory name. The solution is to create a new sharable directory and to manually create a file‐link from the [build‐instance] directory to there.

Install NFS support

madman@s16972616 mweb1 ~ $ sudo yum install nfs‐utils nfs‐utils‐lib 
. . . 
Complete!

Configure nfs, nfslock and rpcbind to run as daemons and start then up:

madman@s16972616 mweb1 ~ $ sudo chkconfig ‐‐level 35 nfs on 
madman@s16972616 mweb1 ~ $ sudo chkconfig ‐‐level 35 nfslock on  
madman@s16972616 mweb1 ~ $ sudo chkconfig ‐‐level 35 rpcbind on 
madman@s16972616 mweb1 ~ $ sudo service rpcbind start 
madman@s16972616 mweb1 ~ $ sudo service nfslock start 
madman@s16972616 mweb1 ~ $ sudo service nfs start

Create a sharable directory on the webserver where the configuration files are shared to:

madman@s16972616 mweb1 ~ $ sudo mkdir /var/www/html/config 
[sudo] password for madman:

Make this directory exportable by adding it using an editor to the /etc/exports file:

Server Build ­ 

madman@s16972616 mweb1 ~ $ sudo nano /etc/exports

Add this to the file:

/var/www/html/config             mapp1(ro,sync,no_root_squash,no_subtree_check)

Where:

ro: The client can only read within the shared directory
sync: Sync confirms requests to the shared directory only once the changes have been committed.
no_subtree_check: This option prevents the subtree checking. When a shared directory is the subdirectory of a larger filesystem, nfs performs
scans of every directory above it, in order to verify its permissions and details. Disabling the subtree check may increase the reliability of
NFS, but reduce security.
no_root_squash: This phrase allows root to connect to the designated directory

Activate the latest export settings:

madman@s16972616 mweb1 ~ $ sudo exportfs –a

Make a symbolic link for the web application’s build instance’s configuration file (configuration.php). Since the web server may potentially be
hosting multiple web applications, it is useful the name the symbolic linked file after the instance build name that it was exported from. We export
the configuration file as file named [build‐instance].conf, Assuming we have a build instance called ‘demo’, the configuration file in the exported
/var/www/html/config directory is named demo.conf.

madman@s16972616 mweb01 ~ $ cd /var/www/html/demo 
madman@s16972616 mweb01 /var/www/html/demo $ ls configuration.php 
configuration.php 
madman@s16972616 mweb01 /var/www/html/demo $ cd ../config 
madman@s16972616 mweb01 /var/www/html/config $ sudo ln ‐s ../demo/configuration.php demo.conf  
madman@s16972616 mweb01 /var/www/html/config $ ls ‐al  
total 8 
drwxr‐xr‐x 2 root root 4096 Jun  3 15:00 . 
drwxr‐xr‐x 3 root root 4096 Jun  3 14:59 .. 
lrwxrwxrwx 1 root root   36 Jun  3 15:00 demo.conf ‐> ../demo/configuration.php

Set up the NFS client:

madman@s16972617 mapp01 ~ $ sudo yum install nfs‐utils nfs‐utils‐lib 
. . .  
Complete!

If the NFS‐client installation was successful, one should be able to query the NFS server (mweb1) what has been exported to it:

madman@s16972617 mapp01 ~ $ sudo showmount ‐e mweb01 
Export list for mweb01: 
/var/www/html/config mapp01

Make mount point on the client where the remote share is to be mounted, then then mount it. Test that the mount contains what you expected – in this
case we expect the demo.conf to appear in there. It is also a symbolic link to a different file on the remote server, so we need to make sure that we
can read the content:

madman@s16972617 mapp01 ~ $ sudo mkdir /mnt/config 
Mount the exported directory from server mweb01 here: 
madman@s16972617 mapp01 ~ $ sudo mount mweb01:/var/www/html/config  /mnt/config
madman@s16972617 mapp01 ~ $ ls ‐al /mnt/config

Finalizing the Server Installations

Some final installation steps are required before the server can be considered ready for production use, to ensure basic recovery from failure and
security.

Rebooting the server

Not only should we be able to demonstrate a successfully reboot of each server (should this ever be required), but it is recommended that the server
memory be flushed after all the configuration changes that have been applied to it in the course of the installation. A server can either be rebooted
from the PLESK control panel, or from the command line as shown here:

Important:

Remember to use the ‐r option (which means restart) so that the server comes back up again, rather than just halt‐ing the server.

madman@s16972617 mapp1 ~ $ sudo shutdown ‐r now 

Broadcast message from madman@s16972617.onlinehome‐server.info 
        (/dev/pts/0) at 13:12 ... 

The system is going down for reboot NOW! 
madman@s16972617 mapp1 ~ $ Connection to s470071337.websitehome.co.uk closed by remote host. 
Connection to s470071337.websitehome.co.uk closed.

Attempt connecting to the server after 10 seconds or so to give the server some time to come back up. From your local terminal, open an SSH session
again:

bignosethethird@terminator $ ssh madman@mapp01  
######################################################## 
# AUTHORIZED ACCESS ONLY.                              # 
# You are entering into a secured area. Your IP, Login # 
# Time, and Username has been noted and sent to the    # 
# server administrator. This service is restricted to  # 
# authorized users only. All activities on this system # 
# are logged. Unauthorized access will be fully        # 
# investigated and reported to the relevant law        # 
# enforcement agencies. Disconnect IMMEDIATELY if you  # 
# are not an authorized user.                          # 
######################################################## 

Last login: Mon Jun 24 13:06:22 1066 from host86‐154‐124‐192.range86‐154.btcentralplus.com 
########################################################        
#       Welcome to another happy server of             # 
#  __  __    _  _____ ____ _   _ _   _     _           # 
# |  \/  |  / \|_   _/ ___| | | (_) | |__ (_)____      # 
# | |\/| | / _ \ | || |   | |_| | | | '_ \| |_  /      # 
# | |  | |/ ___ \| || |___|  _  | |_| |_) | |/ /____   # 
# |_|  |_/_/   \_\_| \____|_| |_|_(_)_.__/|_/_______|  #  
#                                                      # 
########################################################

Success!

The server, which is very far away deep in a data centre, has rebooted with no problems.

Or:

Oh Dear!

It is possible to remedy any booting problems by contacting the hosting providers with the contract and server details via email on
support@1and1.co.uk, or by telephone: +44 333 336 5691 / +44 871 641 2121
System Administration Tasks

It is occasionally required to perform some system‐level tasks such as clearing storage space up or to migrate deployments between environments, e.g.
from a testing environment to a production environment. These processes are described below. Most of these processes can be scripted to either
manually execute or executed on a batch basis (via a cron batch job).

Setting up the System Administration Work Area

Setting up the System Administration Work Area

Server Build ­ 

The system administration tasks are normally executed by user 'madman'. All system administration scripts are held in the /usr/local/bin directory.
This directory is already on the user’s path and you can test this by displaying the PATH environment variable:

$  echo $PATH  
/usr/local/bin:/bin:/usr/bin:/usr/local/sbin:/usr/sbin:/sbin

Check who else has attempted to log into each server

All failed SSH‐logins are noted in the file /var/log/messages. Each week a new file is created and the previous week’s file is saved as a date‐stamped
file name. Message files over 30 days old are automatically deleted.

madman@s16972617 mapp1 ~ $ ls ‐al /var/log/mess* 
‐rw‐‐‐‐‐‐‐ 1 root root    869 Jun  3 02:59 /var/log/messages 
‐rw‐‐‐‐‐‐‐ 1 root root 268573 May 19 02:48 /var/log/messages‐20130519 
‐rw‐‐‐‐‐‐‐ 1 root root  20711 May 26 02:41 /var/log/messages‐20130526 
‐rw‐‐‐‐‐‐‐ 1 root root 224355 Jun  2 03:52 /var/log/messages‐20130602

Scan the message files for lines containing text similar to:

Since the pertinent term is "denied", it is sufficient to grep for this term alone and to extract the IP addresses of the offenders:

madman@s16972617 mapp1 ~ $ sudo grep denied /var/log/messages* | cut ‐f 5 ‐d ":"  | sed ‐e 's/\s*client\s*//' | sed ‐e 's/#.*//' | sort –u  
... etc.

For added geo‐political amusement, you can check where these attacks originate from by looking up the IP addresses:

address:        Baidu Plaza, No.10, Shangdi 10th street,Haidian District Beijing,100080 
address:        10th Floor No.6 2nd North Street Haidian District Beijing,100080

You can also look up all the attacks in one command:

madman@s16972617 mapp1 ~ $ sudo grep denied messages* | cut ‐f 5 ‐d ":" | cut ‐f 1 ‐d "#" | sed ‐e 's/client//' | sort ‐u | xargs ‐I {} whois {} | grep address

CRON System Scheduler

Overview

All batch processes are driven from the CRON system scheduler. There is a working CRON scheduler on each server which perform basic server
adminsitration and security management tasks (see rkhunter). Large processing jobs are from the application server so that production performacen is
not impacted. It is unavoidable that a few batch jobs need to run on the production web servers too but these are kept to a minimum. As rule, batch
jobs are scheduled to run at around 4am UTC when minimum impact on the production infrastructure will be experienced by users.

Batch jobs can be scheduled to run hourly, daily, weekly or any other recurring time pattern within limitations. A process can be scheduled by
dropping its script (or symbolic link) in the relevant directory, or by adding a line to what is know as a <code>crontab file.

Any output that a batch job creates to either STDOUT or STDERR is collected and on termination of a batch job is emailed to the sysadmin. It is good practise to only
explicitly output text to STDOUT from scripts on error conditions that justify a sysadmin being notified by email. Error messages are written to a log file, as is all other
output from the script such as debug, trace, info and warning messages.

There are 5 approaches of how batch jobs can be invoked:

Approach 1: Local, non­root user level

Batch jobs can be set up by running crontab ‐e from the local account. The batch job will be run under the this user's account. There is currently no need to run any
jobs at this level since all batch run under user root.

Approach 2: Root user level

Batch jobs can be set up by running crontab ‐e when logged in as user root and the batch job will be run with the priviledges of the root account. Each uncommented
line is new scheduled job and is in the format:

 .‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐ minute (0 ‐ 59) 
 |  .‐‐‐‐‐‐‐‐‐‐‐‐‐ hour (0 ‐ 23) 
 |  |  .‐‐‐‐‐‐‐‐‐‐ day of month (1 ‐ 31) 
 |  |  |  .‐‐‐‐‐‐‐ month (1 ‐ 12) OR jan,feb,mar,apr ... 
 |  |  |  |  .‐‐‐‐ day of week (0 ‐ 6) (Sunday=0 or 7) OR sun,mon,tue,wed,thu,fri,sat 
 |  |  |  |  | 
 *  *  *  *  * command‐to‐be‐executed

For the sake of simplicity we avoid this approach too.
Approach 3: Any user crontab file

Batch jobs can be set up by editing the file /etc/crontab using any editor as a sudo user. Batch jobs need to specify the user under which the job is run, which is why
user‐name has to be specified:

 .‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐ minute (0 ‐ 59) 
 |  .‐‐‐‐‐‐‐‐‐‐‐‐‐ hour (0 ‐ 23) 
 |  |  .‐‐‐‐‐‐‐‐‐‐ day of month (1 ‐ 31) 
 |  |  |  .‐‐‐‐‐‐‐ month (1 ‐ 12) OR jan,feb,mar,apr ... 
 |  |  |  |  .‐‐‐‐ day of week (0 ‐ 6) (Sunday=0 or 7) OR sun,mon,tue,wed,thu,fri,sat 
 |  |  |  |  | 
 *  *  *  *  * user‐name command‐to‐be‐executed

Approach 4: Any user crontab directory

An alternative is to drop the crontab file into the /etc/cron.d directory, in which the file can be given any name. Third­party vendors use this approach to deploy a
scheduled job for their product. The crontab file format is the same as that for the /etc/crontab file, since the execution user needs to be specified. This is an example
of the batch job configured in /etc/cron.d/maldet_pub to run the maldet malware checking process every 10 minutes as user root:

*/10 * * * * root /usr/local/maldetect/maldet ‐‐mkpubpaths >> /dev/null 2>&1

Approach 5: Drop batch scripts into a cron directory

Instead of having to write a crontab file with error­prone recurrance specifiers, it is possible to drop the batch scripts (or better: make symbolic links to them) into the
either one of the following directories:

Server Build ­ 

/etc/cron.hourly: All scripts in this directory will be executed once per hour, on the hour, in the natural listing order.
/etc/cron.daily: All scripts in this directory will be executed once per day at 4am, executed in the order of listing.
/etc/cron.weekly: All scripts in this directory will be executed once per week on Monday at 4am, executed in the order of listing.

It is customary to prefix the filenames with a 2­digit value to indicate the order of execution, e.g.

 $ ls ‐al /etc/cron.hourly/ 
total 44 
drwxr‐xr‐x  2 root root  4096 Apr 22 16:10 . 
drwxr‐xr‐x 95 root root 12288 Apr 15 11:09 .. 
lrwxrwxrwx  1 root root    62 Oct 29  2014 01restart_fsm_daemon_ORG.sh ‐> /usr/local/etc/cron.hourly/01restart_fsm_daemon_ENVIRONMENT.sh 
lrwxrwxrwx  1 root root    62 Sep 27  2014 01restart_fsm_daemon_PROD.sh ‐> /usr/local/etc/cron.hourly/01restart_fsm_daemon_ENVIRONMENT.sh 
lrwxrwxrwx  1 root root    55 Apr 16 17:48 08update_data_ORG.sh ‐> /usr/local/etc/cron.hourly/08update_data_ENVIRONMENT.sh 
lrwxrwxrwx  1 root root    55 Apr 16 17:48 08update_data_PROD.sh ‐> /usr/local/etc/cron.hourly/08update_data_ENVIRONMENT.sh 
lrwxrwxrwx  1 root root    59 Apr 16 17:43 10update_keywords_ORG.sh ‐> /usr/local/etc/cron.hourly/10update_keywords_ENVIRONMENT.sh 
lrwxrwxrwx  1 root root    59 Apr 16 17:43 10update_keywords_PROD.sh ‐> /usr/local/etc/cron.hourly/10update_keywords_ENVIRONMENT.sh 
lrwxrwxrwx  1 root root    60 Nov 29 21:41 12update_ipdetails_PROD.sh ‐> /usr/local/etc/cron.hourly/12update_ipdetails_ENVIRONMENT.sh 
lrwxrwxrwx  1 root root    62 Apr 21 15:53 66delete_bad_members_PROD.sh ‐> /usr/local/etc/cron.hourly/66delete_bad_members_ENVIRONMENT.sh

These batch jobs are executed every hour on the hour and this way there is no doubt what the order is that they will be executed in. Failures from multiple batch jobs
are consolidated into one email to the sysadmin, rather than a separate email for each batch, as would be the case for the other approached to CRON jobs. This is the
preferred way to control the execution of batch jobs, as there can potentially be many batch jobs in a complex system.
Note
We use symbolic links to the actual files that are deployed on the /usr/local/etc/cron.hourly directory sub­tree. This makes deployment up updated scripts easier,
and also provides an element of protection from accidental deployment of scripts out of the Subversion code repository. Also note that the name of the symbolic link is
different to the name of the real file being linked to. This is a trick used for running scripts for multiple environments on one server and some extra coding inside the
script itself makes this process work.
Backing up and Restoring of Servers

Backup File Conventions

The convention is to back up and package the relevant content on each server as separate packages. The packages are implicitly grouped together by the name of the
backup files, which is constructed from the build name and date that the backup was performed on, where:

The build is named based on the release date of the build, in the form: build_YYYYMMDD
The short­name source server alias is be added, e.g. mweb1
The backup date is added to the backup file in the form YYYYMMDD
The term _backup is added to the file name to remove any ambiguity of its origins and purpose
The file extension is added depending on the type of backup:

Application code: tar.gz – which means lots of files archived together and compacted using GZIP compression
Data: sql.gz – One SQL file which will recreate the entire database, that is compacted using GZIP compression
Binary Dump: dump.gz – One binary file that is created from an application­specific backup tool, for example Subversion uses the dump command.
Images: tar – which means lots of files archived together but not compressed as the images themselves are already compressed (although providing
persistence will be taken care of in future by the Cloud Flare service)

Example of a Joomla backup is: build_20130716_mweb1_20130720_backup.tar.gz

Backup File Creation

The process of backup file creation is run from the APP server to minimize impact on the DB and WEB servers. Data is extracted from the source servers via SSH or
NFS file share ­ in the case of WEB server data, or a MySQL data link ­ in the case of database data. The backup files are created on the APP server. The backup
process scripts are run in succession once a day shortly after the server’s local midnight and is scheduled with a cron job. The scripts are:

backup_remote_database.sh – makes a backup of the latest database build on the remote DB server
backup_remote_application.sh ­ makes a backup of the latest website build on the remote WEB server

The scripts require no parameters and reside in the /home/madman/bin directory. Output of all the scripts is logged to the log file /var/log/matchi. When either of these
scripts are run in batched mode in cron, an email is sent to the System Administrator if there has been a failure.

Backup File Location

Backup Files are located in the directory /backups on the APP server. Only user root can write to this directory, but all users (well, there is currently only one other
user, ‘madman’), can read it.

Off­Site Backup File Vaulting

The latest back­up files are also copied to Google Drive. Backup files can be manually retrieved from there in case of catastrophe. The account details for Google
Drive are:

User: matchi.biz@gmail.com
Password: [*****]
URL: https://drive.google.com

TODO: Vaulting scripts still needs to be added to the backup process. Due to limited available space, rigorous housekeeping is required.

Setting up the batch Backup Job

The standard scheduler is cron. In Red Hat, a dedicated cron­job exists that executes all scripts in the directory /etc/cron.daily, starting at 04:02 local server time. The
scripts are executed in the order of their file name. Since it is desirable to execute backup scripts before any other daily processes, the batch scripts for backups are
named 01… and 02… so that they will be processed first.   Create the script /etc/cron.daily/01backup_remote_database.sh:

madman@s16972617 mapp1 ~ $ sudo nano /etc/cron.daily/01backup_remote_database.sh Password:

Enter this:

#!/bin/bash 
if [[ ‐x /home/madman/bin/backup_remote_database.sh ]] 
then 
  /home/madman/bin/backup_remote_database.sh 
  exit $? 
else 
  exit 99 
fi

Save and exit. Make the script executable:

madman@s16972617 mapp1 ~ $ sudo chmod +x /etc/cron.daily/01backup_remote_database.sh

Apply a similar approach for all other required batch jobs and set the order in which they need to be executed using the file naming technique, e.g. create a script
/etc/cron.daily/02backup_remote_application.sh, etc…

Execution of Batch Jobs

When any one of the batch jobs fail to complete successfully, then a notifications email is sent to user ‘root’, which is redirected to the assigned system administrator.
The email contains all the STDOUT console output that generated during the execution of the batch jobs

Server Build ­ 

If there no problems were encountered during the execution of the batch jobs, then no notification is sent. By convention, all logged output of MATCHI­specific
processes is held in the file /var/log/matchi. The file can retrospectively be searched, using tools such as grep, for events of interest.

Validating of backup files To reduce the risk of backup file getting corrupted for whatever reason as they are copied between environments, a small check file is created
when the backup file is created that should accompany the backup file at all times. The validity of the backup can be checked for at any point using the “md5sum –c”
command against the actual checksum file:

madman@s16972617 mapp1 ~ $ ls ­alrt /backups/ . . ­rw­r­­r­­ 1 root root 118566221 Aug 3 04:02 build_20130802_mdb1_20130803_backup.sql ­rw­r­­r­­ 1 root root
83 Aug 3 04:02 build_20130802_mdb1_20130803_backup.sql.md5 . . madman@s16972617 mapp1 ~ $ md5sum ­c
/backups/build_20130802_mdb1_20130803_backup.sql.md5 /backups/build_20130802_mdb1_20130803_backup.sql: OK

How to install an Application from backup on a new Server

Copy the backup file to the target server using SCP:

madman@s16972616 xxxxx ~ $ scp build_YYYYMMDD_YYYYMMDD_mweb1_backup.tar.bz2 madman@targetserver:~/.

If you have correctly set up the public keys between servers, then you should not be prompted for a password and the file should land in the home directory of the
“madman” account. On the target server, unpack the backup file:

madman@targetserver ~ $ cd /var/www/html madman@targetserver /var/www/html $ sudo tar ­xjvf ~/build_YYYYMMDD_YYYYMMDD_mweb1_backup.tar.bz2
Password:

This will create a new directory /var/www/html/build_YYYYMMDD that holds the Joomla application files. Make the new installation accessible to the LIGHTTP­
daemon, by recursively (see the –R option) changing the owner and group to lighttpd: madman@s16972616 taergetserver /var/www/html $ sudo chown ­R
lighttpd:lighttpd matchi

How to Restore a Database Backup to a new database

The database backup was created in the backup script with a command like this:

$ mysqldump –h[servername] ‐u[dbusername] ‐p[password] ‐‐routines [build_YYYYMMDD] >  build_YYYYMMDD_$(date +%Y%m%d)_mdb1_backup.sql

Restoring is the reverse of this process: On the target database server, restore the database by running the database backup into a newly­create database. First create the
target database. Then run the SQL backup file into the new database using the database’s authentication credentials, as per the code below. Note the ­c option when
importing the data as this prevents the comments in the stored procedures from getting stripped out.

$ mysql –h[server] ‐uroot –p[pwd] –e ‘create database build_YYYYMMDD’ 
$ mysql ‐c –h[server] ‐uroot –p[pwd] build_YYYYMMDD < build_YYYYMMDD_YYYYMMDD_mdb1_backup.sql

Test that the restore was successful by listing the tables:

$ mysql –h[server] ‐uroot –p[pwd] build_YYYYMMDD  –e ‘show tables’ 
+‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐+ 
| Tables_in_build_YYYYMMDD                    | 
+‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐+ 
| ix02_assets                                 | 
| ix02_associations                           | 
| ix02_banner_clients                         | 
etc ...

Web Server Build
Enabling Apache

If the Apache service does not start on server boot, start it like this and set it to start on boot­up:

$ sudo systemctl start httpd 
$ sudo systemctl enable httpd 
...

Install the MALDET malware Checker

This utility is required to ensure that uploaded documents that contain malware are cleansed, before being made available for user consumption.

The installation is as follows:

$ wget http://www.rfxn.com/downloads/maldetect‐current.tar.gz 
$ tar ‐xzf maldetect‐current.tar.gz 
$ cd maldetect* 
$ sudo ./install.sh

Edit the configuration file:

$ sudo nano  /usr/local/maldetect/conf.maldet

Make the following changes:

email_alert="1" 
email_addr="sysadmin@matchi.biz" 
email_subj="[Security] MALDET Malware Alert from $(hostname)" 
... 
quarantine_hits="1" 
quarantine_clean="1"

The subsequently­installed batch jobs will continuously monitor the relevant directories for files that contain malware.

The subsequently­installed batch jobs will continuously monitor the relevant directories for files that contain malware.
Install ImageMagick

Server Build ­ 

ImageMagick is used for validating, fixing and resizing any images on the web server. Install it (note the text­case of the package name):

$ sudo yum install ImageMagick

Install Libre Office

We need to install the headless version of Libre Office (similar to Open Office) so that icons can be made of attachment files, which are typically, PDF, Powerpoint,
Excel and Word documents. The actual process that creates the icons is an inode­watcher that is driven and restarted by one of the batch jobs for the time being. Install
Libre Office like this:

$ sudo yum install libreoffice‐headless

Installing and Configuring PHP

Standard PHP Version across all servers

version. If it is installed,it should return the following:

$ php ‐‐version 
Copyright (c) 1997‐2014 The PHP Group 

Installation steps

By default, CentOS comes with a very old (weak, slow, vulnerability­prone) version of PHP. Set up the configuration for the REMI repository to install the desired
version of PHP by adding the following:

$ sudo nano /etc/yum.repos.d/remi.repo 
... 
[remi‐php56] 
name=Les RPM de remi de PHP 5.6 pour Enterprise Linux 6 ‐ $basearch 
#baseurl=http://rpms.famillecollet.com/enterprise/6/php56/$basearch/ 
mirrorlist=http://rpms.famillecollet.com/enterprise/6/php56/mirror 
# WARNING: If you enable this repository, you must also enable "remi" 
enabled=1 
gpgcheck=1 
gpgkey=file:///etc/pki/rpm‐gpg/RPM‐GPG‐KEY‐remi

With the new PHP version enabled in the REMI repository, updatge the repository itselt:

$ sudo yum ‐y update php*

PHP should be installed by default on the server. If not, install it like this:

$ sudo yum ‐y install php‐mysql php‐devel php‐gd php‐pecl‐memcache php‐pspell php‐snmp php‐xmlrpc php‐xml

It does not have the timezone setting set and some PHP modules refuse to work correctly without that setting. In the file /etc/php.ini, find the section marked 'Module
Settings' and set the following:

date.timezone = "Europe/London"

You need to restart the Apache server to effect the timezone setting and the new version of PHP:

$ sudo /etc/init.d/httpd restart 
Stopping httpd:                                            [  OK  ] 
Starting httpd:

MySQL Database Server Build

The MySQL Database Server is based on the Standard Matchi Linux Server build, and has the following

MySQL/MariaDB
Support tools for MySQL/MariaDB

MySQL vs. MariaDB

MySQL and MariaDB are mostly code­equivalent databases (and thus functionally the same), however their licensing terms differ and MariaDB is a free­er database
than MySQL.

By default, Red Hat and CentOS 6.x distributions come bundled with MySQL, whereas CentOS 7.x comes bundled with MariaDB, i.e.:

Virtual Machines in the data centre run CentOS 6.5, therefore they use MySQL. MySQL is pre­installed.
Physical server are built with CentOS 7.x, therefore they use MariaDB. MariaDB may need to be installed as an additional step. See the next section how to
install it.

All the usual mysql­commands remain the same between MySQL and MariaDB and the only change is the actual name of the service­daemon: it is either mysqld or
mariadb.
Installing the MySQL database on CentOS 6.x

To install the MySQL database service and client:

$ yum ‐y install mysql‐server mysql

Start the MySQL service and set it up as a service so that it automatically restarts on server boot:

$ sudo /etc/init.d/mysqld start 
... 
$ sudo chkconfig ‐‐levels 2345 mysqld on

Note that CentOS 6.x still uses the old method of service controls through scripts in the /etc/init.d directory.

Enable consistent Stored Procedures coding

Enable consistent Stored Procedures coding

Server Build ­ 

Run the following script to align the coding of stored procedures on the new database with the current Matchi standard:

$ mysql_upgrade ‐u root ‐p 
Enter password:

Note
You should run this script after every upgrade of MySQL.
Installing the MariaDB database on RedHat 7.x

If it is not already installed on your server (not likely to be the case for hosted servers), then install the MariaDB database service and client:

$ yum ‐y install mariadb‐server mariadb

Start the MariaDB service and set it up as a service so that it automatically restarts on server boot:

$ sudo systemctl start mariadb.service 
... 
$ sudo systemctl enable mariadb.service

CentOS 7.x uses the systemctl method of service controls through the systemd control mechanism, instead of the legacy init.d method of older version of Linux.
Configuration

The configuration of the MySQL database service is mostly managed through the file /etc/my.cnf.

Make a backup of the configuration file before making any changes. After having made the configuration changes, restart the database service when complete:
Note
Remember to test that you can still connect to the database after a service restart.

New Configuration on MySQL on Centos 6.5

$ sudo /etc/init.t/mysqld restart 
Stopping mysqld:                                           [  OK  ] 
Starting mysqld:                                           [  OK  ]

New Configuration on MariaDB on Centos 7.0

$ sudo systemctl restart mariadb 
Stopping mariadb:                                          [  OK  ] 
Starting mariadb:                                          [  OK  ]

Default Character Set and Collation

Our character set must always be set to UTF8 and our collation must always be set to UTF8­General­Case­Insensitive (utf8_general_ci). By default this is set to
Swedish, which on a bad day can completely mess with an otherwise fine database.

Avoid collation disasters and make it so that the creation of a new database is always of the correct character set and collation, by adding these three sections of the file
/etc/my.cnf:

[client] 
default‐character‐set=utf8 

[mysql] 
default‐character‐set=utf8 

[mysqld] 
init_connect='SET collation_connection = utf8_general_ci' 
character‐set‐server = utf8 
collation‐server = utf8_general_ci

Note
When we support multiple spoken­languages one day, we may need to consider changing the collation to UTF8­UNICODE­Case­Insensitive, which supports extended
characters in collations more elegantly but is not as efficient.
Setting up Logging

The default installation on CentOS has very limited logging enabled. Since a number of log file types will need to be stored, it is best to create a dedicated directory in
the /var/log directory. Create the directory if it does not already exist:

In Centos 6.0, you need to create these directories.

$ sudo mkdir /var/log/mysql 
$ sudo chown mysql:mysql /var/log/mysql

In Centos 7.x, the logging directories have already been established and are /var/log/mariadb.

Add the configurations to the configuration file /etc/my.cnf where necessary:

# Section: 
[mysqld] 
... 
# MySQL error log ‐ included aborted connections 
# For Centos 6.x: 
log_error                      = /var/log/mysql/error.log 
# For Centos 7.x 
log_error                      = /var/log/mariadb/mariadb.log 

log_warnings                   = 2 

# Slow Query Log ‐ disabled by default 
# For Centos 6.x: 
slow_query_log_file            = /var/log/mysql/slow.log 
# For Centos 7.x 
slow_query_log_file            = /var/log/mariadb/slow.log 
slow_query_log                 = 0 
log_queries_not_using_indexes  = 1 
long_query_time                = 0.5 
min_examined_row_limit         = 100 

# General Query Log ‐ disabled by default 
# For Centos 6.x: 
general_log_file               = /var/log/mysql/general.log 
# For Centos 7.x 
general_log_file               = /var/log/mariadb/general.log 
general_log                    = 0 

# Section: 
[mysqld_safe] 
.... 

# For Centos 6.x: 
log_error                      = /var/log/mysql/mysqld.log 
# For Centos 7.x 
log_error                      = /var/log/mariadb/mysqld.log

Server Build ­ 

The 'General' and 'Slow' logs are very resource intensive and can be manually enabled to trace performance errors, but should be turned off again when done:

$ mysql 

mysql> set global general_log=1; 
..  
mysql> set global general_log=0;

mysql> set global slow_query_log=1; 
..  
mysql> set global slow_query_log=0;

Database Authentication

The default account for access on MySQL is root. This should not be confused with the Linux super user, root. The password for database user root is set up using the
mysqladmin utility:

$ sudo mysqladmin ‐u root password 
New password:  
Confirm new password:

Local authentication

You can set up the login for local maintenance directly on the server. This way you don't need to enter the user name and password every time. Create and edit the file
in your home directory, .my.cnf:

$ nano ~/.my.cnf

Add this text – and replace [password] with the password for database user root:

[client] 
user = root 
password = XXXXXXXXX

Save  Ctrl O  & Close  Ctrl X .

Restricting Remote Database Access

$ sudo /usr/bin/mysql_secure_installation

TODO:

Restricting local Data Access: It is good practice to set data­access restrictions to the ‘root’ account in MySQL, which will be done on a future system design iteration.
For now, database user account root has full access to the MySQL database.

Log in to the MySQL database. Note that there is no need to specify a user and password when using the mysql­shell, since we have set up the ~/.my.cnf file, above.
By default, the database can only be accessed from the local server, mdb1, but it also needs to be accessed from the web server and the application server, for which we
grant access as follows by specifying the IP addresses:

$ mysql 
mysql> use mysql;

Reading table information for completion of table and column names You can turn off this feature to get a quicker startup with ­A

Database changed 
mysql> GRANT ALL PRIVILEGES ON *.* TO  'root'@'localhost'  IDENTIFIED  BY  'XXXXXXXXXX'; 
mysql> flush privileges; 

Install Database Management Tools

Note
Not proven yet! In the mean time, we use custom backup scripts

A few specialized data management tools are require for effective backing up, restoring and data maintenance.

Percona Database Backup and Restore Tool:

Select the latest version

Go to http://www.percona.com/downloads/XtraBackup/LATEST/ for the latest available version. Select the version corresponding to the version of Red Hat/CentOS
and copy the URL ­ no need to download it, see the next step.

First fetch the install RPM file

Fetch the file RPM directly onto the server:

Install the downloaded RPM file:

More information about this utility is available at http://www.percona.com.

Editing SQL using Nano

Server Build ­ 

You can add keyword­sensitive colour coding for the nano editor, by creating this configuration script on either the Database Server for remote editing on the server
itself, or on your local machine.

Create a SQL­Language file

$ sudo nano /usr/share/nano/sql.nanorc 
[sudo] password for madman:

Add this (copy and paste from this doc!):

syntax "sql" "\.sql$" "sqliterc$" 

color brightred "\<[A‐Z_][0‐9A‐Z_]+\>"  
color green "\<(VARCHAR|TINYINT|TEXT|DATE|SMALLINT|MEDIUMINT|INT|INTEGER|BIGINT|FLOAT|DOUBLE|DECIMAL|DATETIME|TIMESTAMP|TIME|YEAR|UNSIGNED|CHAR|TINYBLOB|TINYTEXT|BLOB|MEDIUMBLOB|MEDIUMTEXT|LONGBLOB|LONGTEXT|ENUM|BOOL|BINARY|VARBINARY)\>"
color brightyellow "\<(ALL|ASC|AS|ALTER|AND|ADD|AUTO_INCREMENT|BETWEEN|BINARY|BOTH|BY|BOOLEAN|CHANGE|CHECK|COLUMNS|COLUMN|CROSS|CREATE|DATABASES|DATABASE|DATA|DELAYED|DESCRIBE|DESC|DISTINCT|DELETE|DROP|DEFAULT|ENCLOSED|ESCAPED|EXISTS|EXPLAIN)\>"                                                                                                                                           
color brightyellow "\<(FIELDS|FIELD|FLUSH|FOR|FOREIGN|FUNCTION|FROM|GROUP|GRANT|HAVING|IGNORE|INDEX|INFILE|INSERT|INNER|INTO|IDENTIFIED|IN|IS|IF|JOIN|KEYS|KILL|KEY|LEADING|LIKE|LIMIT|LINES|LOAD|LOCAL|LOCK|LOW_PRIORITY|LEFT|LANGUAGE|MODIFY|NATURAL|NOT|NULL|NEXTVAL)\>"                                                                                                                     
color brightyellow "\<(OPTIMIZE|OPTION|OPTIONALLY|ORDER|OUTFILE|OR|OUTER|ON|PROCEDURE|PROCEDURAL|PRIMARY|READ|REFERENCES|REGEXP|RENAME|REPLACE|RETURN|REVOKE|RLIKE|RIGHT|SHOW|SONAME|STATUS|STRAIGHT_JOIN|SELECT|SETVAL|SET|TABLES|TERMINATED|TO|TRAILING|TRUNCATE|TABLE|TEMPORARY|TRIGGER|TRUSTED)\>"                                                                                          
color brightyellow "\<(UNIQUE|UNLOCK|USE|USING|UPDATE|VALUES|VARIABLES|VIEW|WITH|WRITE|WHERE|ZEROFILL|TYPE|XOR)\>"                                                                              
                                                                                                                                                                                                
## String highlighting.  You will in general want your comments and                                                                                                                             
## strings to come last, because syntax highlighting rules will be                                                                                                                              
## applied in the order they are read in.                                                                                                                                                       
color brightyellow "<[^=        ]*>" ""(\\.|[^"])*"" 
## 
## This string is VERY resource intensive! 
color brightyellow start=""(\\.|[^"])*\\[[:space:]]*$" end="^(\\.|[^"])*"" 

## Comment highlighting 
color brightblue "\‐\‐.*$" 
color brightblue start="/\*" end="\*/" 

## Trailing whitespace 
color ,green "[[:space:]]+$"

Enabling the Language file

Enable this configuration file by adding the following to the main configuration file:

madman@s16972619 mdb1 ~ $ sudo nano /etc/nanorc  
[sudo] password for madman:

Add this:

# SQL Code 
include "/usr/share/nano/sql.nanorc"

Save and close. From now on, when you edit a SQL script in nano, SQL keywords it will look like this:

Set up the system Time Zone Data in MariaDB/MySQL

Explanation

MySQL can host a copy of the system's time zone definitions. These definitions differ from system to system, which is why this data is manually installed after the
basic system and been built and the MySQL/MariaDB has been set up. The operating system's time zone database is defined by the files in the /usr/share/zoneinfo
directory. The utility mysql_tzinfo_to_sql reads these files and populates the relevant tables in MySQL/MariaDB's mysql system database. All built­in time zone­based
functions, such as convert_tz, refer to the content the time zone­tables in there. If data in not populated, then these functions return a NULL.

In the case of Matchi, we need to consider customer time zones (see Challenges), so the time zone information is therefore essential. The tables in the
<cide>mysql</code> database that must be populated are:

time_zone
time_zone_leap_second
time_zone_name
time_zone_transition
time_zone_transition_type

Installation

This is how to load MySQL's dictionary database from the operating system's time zone database:

$ mysql_tzinfo_to_sql /usr/share/zoneinfo | mysql mysql

Server Build ­ 

Since local authentication has now been enabled in the .my.cnf</conf< file, no further parameters are required for the <code>mysql command. If this is yet set
up, then also provide the user name (‐uroot and password (‐pXXXXXX) who also has rights to write to the mysql system database.

Verification

The table time_zone should contain some data now. Check it like this:

 $ mysql mysql ‐e 'select * from time_zone limit 5' 
+‐‐‐‐‐‐‐‐‐‐‐‐‐‐+‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐+ 
| Time_zone_id | Use_leap_seconds | 
+‐‐‐‐‐‐‐‐‐‐‐‐‐‐+‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐+ 
|            1 | N                | 
|            2 | N                | 
|            3 | N                | 
|            4 | N                | 
|            5 | N                | 
+‐‐‐‐‐‐‐‐‐‐‐‐‐‐+‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐+

Connecting to the Database

Local connection to a database

You connect manually to a database while in an SSH session on the actual database server.

If you are logged in as user madman on the Database Server, and /etc/my.cnf is correctly set, then you can connect to the database without having to supply your
username or password. You can list the databases, select a database, and so on as follows:

$ mysql 
Welcome to the MySQL monitor.  Commands end with ; or \g. 
.. 
Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.             

mysql> show databases;                                                                    
+‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐+ 
| Database                | 
+‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐+ 
| information_schema      | 
| 20130611                | 
| apsc                    | 
| backup_test             | 
...

Remote connection to a database from with the Matchi Datacenter

Specific access has been granted for the other Matchi servers in the datacenter to directly connect to the database on the Database Server through IP address restriction.
It is not possible for any other devices, other than the assigned devices, to connect. (See the next section on how to connect from an arbitrary IP address)

From, say mapp01, connect to the database test on mdb01 as follows, using password authentication:

mapp01 ~ $ mysql ‐uroot ‐p******  ‐hmdb01 test

where:

­u = Database user
­p = Database user's Password
­h = Server that the database is on

Remote connection to a database from outside the Matchi Datacenter

It is only possible to connect remotely to a database on the database server through a previously­established SSH­tunnel beteen yourself on the remote computer and
one of the servers. This is a very secure method to connect to the servers and do data manipulations from a remote terminal.

This secure SSH tunnel can only be established if you have previously set up the public / private key­pair on your local machine and have your public key on the
Database Server's key chain. When the SSH­tunnel is set up one can connect a local MySQL development program or terminal session to the remote database by
actually connecting to the local machine and letting it act as a proxy to the remote server via the SH tunnel.

On your local machine, set up the SSH­tunnel in a separate terminal window so that this side of your local connection is on port 3307 and is presented on port 3306 on
the remote side of the tunnel:

bignosethethird@terminator ~ $ ssh ‐L 3307:localhost:3306  madman@mdb01

Keep this tunneling session open and open another terminal to connect to the Database test through the tunnel. You are specifically indicating that you want to connect
to the previoulsy­established tunnel by specifying the port number of the tunnel 3307 that the tunneling session is listening on:

bignosethethird@terminator ~ $ mysql ‐uroot ‐p***** ‐hlocalhost ‐P3307 test

where:

­u = Database user
­p = Database user's Password
­h = Server that the database is on
­P = Port number to connect to on your local side of the tunnel
test = the name of the database on the server to connect to

Install phpMyAdmin

phpMyAdmin is a web­based, database development and administration tool. It can be installed on any server and made to access a database on any authorised server.

Installation

The EPEL Repository needs to be installed and enabled: Do this if this is not the case:

$ wget http://download.fedoraproject.org/pub/epel/6/x86_64/epel‐release‐6‐8.noarch.rpm 
# sudo rpm ‐ivh epel‐release‐6‐8.noarch.rpm

Install phpMyAdmin as follows:

$ sudo yum install phpmyadmin

Configuration

By default, phpMyAdmin is configured to only access databases on the server that it is installed. It is also installed to be accessed from the same IP address (i.e. same
server) that the phpMyAdmin service is installed on. Make the following changes to the Apache configuration file for phpMyAdmin to allow access from external
addresses:

Server Build ­ 

$ sudo nano /etc/httpd/conf.d/phpMyAdmin.conf

Change the 2 lines that contain Allow from local to Allow from [ipaddress] [ipaddress] [domain] .... The IP addresses or domains of points where this service is
likely to be accessed from need to added in here as a space­delimited list.

If access to this service is required via a domestic network provider, which mostly means that a new IP address is occasionally assigned to the subscriber, you need to
specify a range of IP addresses. However, if the domestic router has a dynamic domain resolution service configured, you can set the domain instead of the IP address.

Warning
It is important to not allow access from all IP addresses, as this represents a significant security risk. It is therefore far more preferable to allow access from domestic
approximately 120,000 different IP addresses (roughly 95% of 255x255x2)

Your Apache configuration should end containing 2 lines that read something like this:

Determining an IP address for a domestic Internet service

If you need to set up access for a domestic, dynamic­allocated IP address service on a router that does not support dynamic domain name resolution, you can specify
your current IP address by looking up the IP address of your own ADSL connection on the status report page on your router. Of visit http://www.whatismyip.com/.

Hiding the phpMyAdmin service

By default, the service name for the phpMyAdmin service is phpmyadmin and it can be accessed from the public network by browsing to this address:
http://mdb01/phpmyadmin. An adversary may attempt to discover if such a service is available on a server by specifically targeting the term 'phpmyadmin'. A possible
solution is to give the name of the publicly­visible service a cryptographic nonce. An 8 character­long nonce that is a valid URL can be generated like this:

$ openssl rand ‐base64 8 | tr ‐cd '[[:alnum:]]._‐' | sed ‐e 's/\(.\{8\}\).*/\1\n/' 
t5ZyNCkS

Replace the line Alias /phpMyAdmin /usr/share/phpMyAdmin with Alias /[nonce] /usr/share/phpMyAdmin, where [nonce] is the nonce that was generated.

Restart the Apache Server

To effect new configuration changes, the Apache server needs to be restarted:

$ sudo service httpd restart

You should now be able to access the phpMyAdmin service by pointing your browser this URL: http://mdb01/[nonce].

More information

General phpMyAdmin Configuration: http://docs.phpmyadmin.net/en/latest/config.html

Prettify your command­line inteface!

Run this alias declaration and also add this alias to your .bash_profile file. The next time you need to access the database server using the command prompt, use
colormysql command instead of mysql command.

alias colormysql=$(echo ‐e 'mysql ‐‐prompt="\x1B[31m\\u\x1B[34m@\x1B[32m\\h\x1B[0m:\x1B[36m\\d>\x1B[0m "')

It will look like this:

There exists a convention to prefix 'color' ('merkin spelling ­ stick to it, it's the UNIX way!) to standard commands to achieve just that, for example colordiff for the
very colourful (sic) version of diff.

Application Server Build

This server’s designated purpose is to perform as many as possible back­end operations that can be outsourced to it, in order to allow the web server and the database
server to provide the serving of web content. Candidates for such asynchronous back­end processes are:

State Machine Management
Image Manipulations
Data Manipulations
Server Maintenance tasks
Data Maintenance tasks
Reporting functions
Notifications Management
Mass Mailing Management

Install Additional Packages

In addition to the packages installed on a standard Matchi server, we need install a few developer­oriented software packages due to the specialized nature of some of
the tasks that this server needs to install.

the tasks that this server needs to install.
Development packages

Server Build ­ 

This installs gcc (a C/C++ compiler), git, swig, make, automake, doxygen, fortran (not required!), patch, flex, yacc / bison, and a few others in one go:

$ sudo yum groupinstall 'Development Tools' 
Complete

Maths Libraries

Install a richer mathematical environment: Some heavy­duty mathematical functions are performed for the calculation of heuristics to match counter­parties up. For
this, the GNU Arbitrary Precision Library has to be installed:

$ sudo yum install gmp‐devel

Perl environment

Install a richer Perl environment: The servers come with a Perl environment, but some additional Perl­packages need to be installed. The best tool for installing Perl­
packages is the CPAN tool, which is not yet installed. The first task therefore is to install the CPAN package manager for Perl as follows:

$ sudo yum install perl‐CPANPLUS.noarch

Then run the CPAN package manager. The first time that it runs, it will prompt a number of times, to which you should just accept the default. After that, it should
come up like this:

$ sudo cpan 
Terminal does not support AddHistory. 

Enter 'h' for help. 

cpan[1]>

Use CPAN to install the necessary Perl packages and to upgrade the latest packages, by typing the following commands:

cpan> install CPAN 
cpan> reload CPAN 
cpan> install DBI 
cpan> install DBD::mysql 
cpan> install Pod::Perldoc 
cpan> install Getopt::Long 
cpan> install LWP 
cpan> install Log::Log4perl 
cpan> install DateTime 
cpan> install DateTime::Format::MySQL 
cpan> install DateTime::Format::DateParse 
cpan> install Data::Dumper 
cpan> install URI 
cpan> install List::Util 
cpan> install JSON::Parse 
cpan> install PHP::Serialization 
cpan> install MIME::Base64 
cpan> install Error 
cpan> install Math::BigInt 
cpan> install Math::BigInt::GMP 
cpan> install Math::Base36 
cpan> install Digest::SHA2 
cpan> install PadWalker

ImageMagick Utility

Install this utility on the Application Server if it is not already installed. ImageMagick is used for resizing and optimizing images that have been upload by users. Install
it (note the character­case of the package name):

$ sudo yum install ImageMagick

GeoIP Utility

This utility is used for providing geographical details of IP addresses. Install it like this:

$ sudo yum install geoip

The geographical data needs to be updated for the first time and can then occasionally be updated again by running this command:

$ sudo GeoIP‐update

Optional step: Manually replace the updates with even more accurate files:

$ cd /usr/share/GeoIP 
$ sudo wget http://geolite.maxmind.com/download/geoip/database/GeoLiteCity.dat.gz 
$ sudo wget http://geolite.maxmind.com/download/geoip/database/GeoLiteCountry/GeoIP.dat.gz 
$ sudo wget http://download.maxmind.com/download/geoip/database/asnum/GeoIPASNum.dat.gz 
$ sudo gunzip GeoIPASNum.dat.gz GeoIP.dat.gz GeoLiteCity.dat.gz

Usage:

Country­level details:

GeoIP Country Edition: US, United States 
GeoIP ASNum Edition: AS15169 Google Inc.

City­level details (will only work if you have run geoipupdate at least once):

Note: The file /usr/share/GeoIP/GeoLiteCity.dat that is installed when geoipupdate is run does not always contain accurate information. It is possible to get a more
accurate and complete data file by either manually installing the updates as described above, or by first obtaining a licence (at some considerable cost) from
https://www.maxmind.com/en/my_license_key, and applying the license key in the file /etc/GeoIP.conf.
Install MATCHi­specific Application Programs

MATCHi­specific / home­grown Application Programs and scripts have been written in a number of programming languages and scripts:

Perl
Python

Python
PHP
BASH

Server Build ­ 

Some are batch­run programs and others are utility programs that are manually executed as and when required.

Deployment Directories

All these scripts reside in the directory /usr/local directory tree (as per standard Unix practise), which looks as follows:

$ tree ‐d ‐L 2 /usr/local 
/usr/local 
├── bin 
 
├── etc 
 
│   └── cron 
 
├── sbin 
 
 
└── share 
    └── templates
 

Each directory contains:

/usr/local/bin: Utility scripts, report genators, batch processes
/usr/local/etc/cron: Batched calling scripts. These are called either hourly, daily, weekly or monthly by setting symbolic links between them and
/etc/cron.hourly, /etc/cron.daily, /etc/cron.weekly respectively.
/usr/local/sbin: Background daemons
/usr/local/share/templates: Templates used for automated generation of document, reports and notification.

The scripts and application are owned by root and have their executable flag set (see the x's in the left hand columns):

$ ls ‐al /usr/local/bin 
‐rwxr‐xr‐x  1 root root    2228 Sep 15 00:18 adjoinall.sh 
‐rwxr‐xr‐x  1 root root    7555 Sep 22 18:34 backup_local_database.sh 
‐rwxr‐xr‐x  1 root root    5453 Sep 22 18:34 backup_local_subversion.sh 
‐rwxr‐xr‐x  1 root root    8850 Nov  2 11:54 backup_remote_application.sh 
‐rwxr‐xr‐x  1 root root    8787 Nov  2 11:54 backup_remote_database.sh 
etc...

If the executable flag is not set, then you can set it like this:

$ sudo chmod +x /usr/local/bin/*

By default, all Unix users have the /usr/local/bin on their path. You can check this:

$ echo $PATH 
/usr/local/bin:/bin:/usr/bin:/usr/local/sbin:/usr/sbin:/sbin:/home/madman/bin

Application Program Logging

All Application programs log to a common file called /var/log/matchi. The logging­libraries Log4Perl, Log4PHP, Log4Python etc. are used to perform the logging. The
content of each log entry is sufficiently detailed to distinguish the application that wrote to it, contains the time stamp and the line of code. Logging occurs on 6 levels:

TRACE: Only possible if turned on as an option when the application is run. Produces very verbose output. Used for tracing the value of variables of logic flow
at a very detailed level.
DEBUG: Only possible if turned on as an option when the application is run. Produces very verbose output. Used for tracing the value of variables of logic flow.
INFO: Produces tracking information and metrics, such as when the program was run and when how records it processed.
WARN: Notifies if an expected error condition was encountered that was dealt with in the program
ERROR: An error in a transaction occurred and program either reattempts the transaction or ignores it.
FATAL: A catastrophic system­based error occurred, or the program was abandoned because too many processing errors were encountered.

Preparing for Logging

The applications, if run as user root, will create the log file if it does not exist. In order to run the application as any other user, the user needs to have write access to
the log file. This is done by making the user in question the log file owner:

$ sudo touch /var/log/matchi 
$ sudo chown madman:adm /var/log/matchi 
$ ls ‐al /var/log/matchi 
‐rw‐r‐‐r‐‐ 1 madman adm 0 Jun 25 11:34 /var/log/matchi

Log File Rotation

A log file rotation process exists that places the previous day's log entries in a date­stamped file in the form /var/log/matchi‐YYYYMMDD. An option exists to also
compress the file using GZIP to save space, which is not used here. Log files older than 3 months (90 days) are automatically deleted. The log file rotation is set up by
adding a configuration file to the /etc/logrotate.d directory. These configurations are read each day by the logrotate cron job and responded to accordingly:

$ sudo nano /etc/logrotate.d/matchi

Enter the following configuration:

/var/log/matchi { 
  missingok 
  notifempty 
  create 0640 madman adm 
  copytruncate 
  rotate 90 
}

Save and close  Ctrl‐O  and  Ctrl‐X .

Viewing and searching log files

Various sophisticated tools exist to scan and view the content of log files. In the examples here we rely on simple yet powerful console commands.

To search for INFO events:

$ grep INFO /var/log/matchi  
...

To search for events that relate to a particular program:

$ grep IdeaFSM /var/log/matchi  
...

To search for events that occurred around a particular date range, e.g. 19 June to 20 June:

$ egrep '06/(19|20)' /var/log/match

Server Build ­ 

To search for events that occurred around a particular time range, e.g. between 10:30pm to 11:30pm on 19 June:

To view a continuous scrolling of the log file, use the tail –f command, which only stops once you hit  Ctrl‐C .

$ tail ‐f /var/log/matchi 
... 
^C

For a colour­coded display of the running log, run logwatch. The code for logwatch is this one­liner:

tail ‐f ‐n 50 /var/log/matchi | sed 's#\[WARN\s*\]#\x1b[33m&\x1b[0m#; s#\[ERROR\]#\x1b[31m&\x1b[0m#;  s#\[FATAL\]#\x1b[31m\x1b[5m&\x1b[0m#; s#\[INFO\s*\]#\x1b[32m&\x1b[0m#; s#\[DEBUG\]#\x1b[34m&\x1b[0m#; s#\[TODO\s*\]#\x1b[36m&\x1b[0m#; s#\[SECURITY\]#\x1b[33m\x1b[5m&\x1b[0m#; s#\[HEART\]#\x1b[35m&\x1b[0m#; s#\[TRACE\]#\x1b[1;34m&\x1b[0m#; s#=\{3,\}#\x1b[1;34m&\x1b[0m#g;'

It gives you this:

Node.js

Requirement

Used for running the RabbitMQ Simulator

Installation

On the development server:
Note
If you have not done so yet, you should install the standard group of development tools:

$ sudo yum groupinstall 'Development Tools'

Now install Node.js:

$ sudo yum install nodejs

Followed by installing the Node Page Manager (npm):

$ sudo yum install npm.noarch

Now install Node's Express package and others:

$ sudo npm install

Usage
Download the Node.js application, e.g. RabbitMQSimulator:

$ cd ~/git 
$ git clone https://github.com/RabbitMQSimulator 
$ cd RabbitMQSimulator

Run the Node.js application, typically called app.js:

$ node app.js  
Listening on port 3000

Point a browser to the server on port 3000 and proceed.

Hit  Ctrl‐C  to stop the application.

{{Note|If you want the application run to persist Run the Node.js application, typically called app.js:

$ nohup node app.js & 
nohup: ignoring input and appending output to `nohup.out'

You can close the server session and come back later and kill the Node.ja application if no longer required:

Server Build ­ 

$ ps ‐ef | grep node 
madman   13142     1  0 14:05 ?        00:00:00 node app.js 
$ kill ‐9 13142

RabbitMQ Installation

First enable the EPEL package library for additional packages:

$ sudo sed ‐i 's/^enabled=0/enabled=1/' /etc/yum.repos.d/epel.repo

Then install the Erlang language:

$ sudo yum install erlang

Get the latest version of RabbitMQ Server:

$ cd installs 
HTTP request sent, awaiting response... 200 OK 
Length: 4100214 (3.9M) [application/x‐redhat‐package‐manager] 

100%[==================================================================>] 4,100,214    971K/s   in 4.9s     

Install RabbitMQ Server:

Preparing...                ########################################### [100%] 
   1:rabbitmq‐server        ########################################### [100%]

Remember to disable the EPEL package library: First enable the EPEL package library for additional packages:

$ sudo sed ‐i 's/^enabled=1/enabled=0/' /etc/yum.repos.d/epel.repo

Start the RabbitMQ Service

$ sudo /etc/init.d/rabbitmq‐server start 
Starting rabbitmq‐server: SUCCESS

You can also check the status of the RabbitMQ service:

$ sudo rabbitmqctl status 
Status of node rabbit@s16972617 ... 
[{pid,6678}, 
                        {mnesia,"MNESIA  CXC 138 12","4.5"}, 
 {os,{unix,linux}}, 
...

Auto­start the RabbitMQ Service on server reboot

$ chkconfig rabbitmq‐server on

Install RabbitMQ libraries

On the application server, the message producers and consumers will mostly be written in Perl, so we install Net::RabbitFoot and its dependecies:

$ sudo yum install libxml2‐devel.x86_64

hen we shell into root and install the Perl package, so that it is installed to the Vendor Perl installation instead of the local user's environment, as the Vendor
environment is the Perl environment that will be called by RabbitMQ.

$ sudo su ‐ 
# cpan 
cpan> install Net::RabbitFoot

We are now ready to write Perl code for RabbitMQ.
Subversion Code Management System

Subversion is our chosen source code management system, and is a primary tool used for creating deployments. See article http://www.if­not­true­then­
false.com/2010/install­svn­subversion­server­on­fedora­centos­red­hat­rhel/

Installing Subversion Client

Install the Subversion Client if it is not already installed:

$ sudo yum ‐y install subversion

Installing Subversion Server

The Subversion Server's web access component is installed as follows:

$ sudo yum ‐y install mod_dav_svn

The web interface only allows you to browse the repository but not perform any other version­control / configuration management functions. To set up the web access
component to server the pages via the Apache web server, create the file /etc/https/conf.d/subversion.conf:

Server Build ­ 

# nano /etc/httpd/conf.d/subversion.conf

Add these configuration lines to the file:

LoadModule dav_svn_module     modules/mod_dav_svn.so 
LoadModule authz_svn_module   modules/mod_authz_svn.so 

<Location /svn> 
   DAV svn 
   SVNParentPath /var/www/svn 
   AuthType Basic 
   AuthName "Subversion repositories" 
   AuthUserFile /etc/svn‐auth‐users 
   Require valid‐user 
</Location>

Create subversion admin user

$ sudo htpasswd ‐cm /etc/svn‐auth‐users madman 
New password:  
Re‐type new password:  
Adding password for user madman

Create subsequent users

Note the use of –m, not –cm:

$ sudo htpasswd ‐m /etc/svn‐auth‐users user2 
New password:  
Re‐type new password:  
Adding password for user user2

Create Subversion Repository

Create and configure the Subversion repository and set ownership of the files:

$ sudo mkdir /var/www/svn 
$ sudo chown –R apache:apache /var/www/svn/matchi 
$ cd /var/www/svn 
$ sudo svnadmin create matchi 
$ sudo chown ‐R apache.apache matchi

Restrict access to known users only

Configure the access to the repository to disable anonymous access and to use access control based on the users that were previously created:

$ sudo nano /var/www/svn/matchi/conf/svnserve.conf

Make the following changes:

anon‐access = none 
authz‐db = authz

Restart the Apache Service

To activate recent changes in the Apache configuration, restart the Apache service:

$ sudo /etc/init.d/httpd restart

Browse to Subversion on http://mapp1/svn/subversion and log in using one of the user accounts that were created to test that it works.

Create the Repository Framework

Create an empty dummy­structure as follows:

$ mkdir ‐p /tmp/svn/{trunk,branches,tags}

This creates the template directories that serve a particular function:

trunk: Main source code repository
tags: Snapshots of the trunk repository
branches: Code forks from the trunk repository

This is the standard structure of a subversion repository. Although any other structure is possible, it needs to be in this form so that the JIRA Subversion component
(and any other tools) can integrate with this repository.

Import (don't just copy) the empty template directory structure to the project repository:

$ svn import ‐m 'Initial import' /tmp/svn / http://mapp01/svn/matchi/ 
Adding         /tmp/svn/trunk 
Adding         /tmp/svn/branches 
Adding         /tmp/svn/tags 
Committed revision 1.

Backing up Subversion

Backups of the Subversion repository are made evey night, and here is the process if an ad­hoc backup is required to other media (where YYYYMMDD is the current
date stamp):

root@s16972617 mapp01 ~ # svnadmin dump /var/www/svn/matchi | gzip ‐9 > /backups/subversion_YYYYMMDD.dump.gz

Restore a Subversion Repository Backup

This restores the entire repository, which includes all the historical changes. It is not the same as a code check­out. To restore a repository to a new location, create a
new repository location:

$ sudo svnadmin create /var/www/svn/matchi2 
$ sudo chown –R apache:apache /var/www/svn/matchi2

Unpack the backup file:

$ gunzip /backups/subversion_YYYYMMDD.dump.gz

Load it to the new repository:

$ svnadmin load 2/var/www/svn/matchi < /backups/subversion_YYYYMMDD.dump

Adding Event­Hooks to Subversion

Server Build ­ 

In the directory /var/www/svn/matchi/hooks are a number of template files, each one for a particular type of event on Subversion. A subsequent action can be
performed when for instance when one or more files has been committed, such a sending an event to a log file or sending an email. The steps to set up a hook are as
follows:

$ cd /var/www/svn/matchi/hooks 
$ ls post‐commit* 
post‐commit.tmpl

This file tells you what parameters to use or to pass to the calling script. In this case, it is:

... 
#   [1] REPOS‐PATH   (the path to this repository) 
#   [2] REV          (the number of the revision just committed) 
...

The policy is to call a code­managed script stored in /usr/local/bin/ from this hook script instead coding the actual script in there, i.e. in this case, we call the script
/usr/local/bin/svnlogcommit.pl:

$ nano post‐commit 
#!/bin/bash                                                                                                                                                                                                        

REPOS="$1"  # e.g. /var/www/svn/matchi 
REV="$2"    # e.g. 3087 

/usr/local/bin/svnlogcommit.pl $REPOS $REV

The file post‐commit calls a Matchi­specific script in /usr/local/bin. Save and close this file, post­commit, and set it to executable and set the ownership:

$ sudo chmod a+x post‐commit 
$ sudo chown apache:apache post‐commit

In a similar way, event­hooks can be created for the other events that Subversion exposes if ever required.
Dropbox

Requirement

We currently need Dropbox on the application server for these reasons:

Dropbox is a tactical tool for sharing large files between desktop devices to the server for those who do not access to facilities such as rsync.
Dropbox is one of few ways through which to securely publish data files, for the Zoho CRM to upload data.

Warning
The use of Dropbbox in a production sever scenario is a tactical solution for the above scenarios, and other uses may create vulnerabilities on the server.

Architecture

Dropbox files are held on the /dev/mapper/vg00‐var logical volume, under /var/data/dropbox.

The directory /var/data/dropbox is bind­mounted to /data/dropbox.

The Dropbox account is hosted by the system root account. By default, Dropbox files are held in the /root/Dropbox directory.

Installation

Follow the instructions on https://www.digitalocean.com/community/tutorials/how­to­install­dropbox­client­as­a­service­on­centos­7

Test the Daemon

The Dropbox daemon should now automatically start on server reboot. You can check it by carefully rebooting the server and checking if the process has started:

$ sudo shutdown ‐r now

Attempt to log in 2 minutes later and check if the dropbox process is running:

bignosethethird@ziltoid ~ $ ssh madman@[server] 
Last login: Sat Jan XX XX:XX:XX XXXX from XXX.XXX.XXX.XXX 
$ ps ‐ef | grep drop 

This means that the daemon worked. If no dropbox process is running, then there was was a problem with your Dropbox configuration.

Test the file synchronization

Create random file in the /data/dropbox directory and confirm that it appears on the Dropbox web page view:

$ sudo su ‐ 
# cd /data/dropbox 
# touch a

If a file called a appears in the web view, then the synchronization work.

Remember to clean up after testing:

# rm ‐f a

Office Server Build

Server Build ­ 

Only do this in a place where is no crime. South Africa is not a good place to do this, but if you must, then bolt the box down and surround it with barbed wire in a
server cage. And electrify the cage. Get some fierce dobermans too.

Follow the steps to build a basic server, and add the following features and configurations
Setting the local time zone

Look up the time zone file for the nearest city that the server is located to in /usr/share/zoneinfo/[country]/[city]. Here, for example, we are based in Johannesburg,
so our time zone file is /usr/share/zoneinfo/Africa/Johannesburg. Remove the old time zone setting and assign a new time zone in one command, and then check that
it was successful with the date­command.

$ sudo rm /etc/localtime; sudo ln ‐s /usr/share/zoneinfo/Africa/Johannesburg /etc/localtime 
$ date 
Mon 16 Feb 19:07:20 SAST 20xx

Sensors Support

Since it is a physical server, we need to monitor the actual temperature and other physical characteristics, as there is no VM­hosting operating system to do this for you.
We install the lm_sensors­package:

$ sudo yum install lm_sensors

All the various sensors on the server need to be initially detected:

$ sudo sensors‐detect

To view the temperature of the CPUs:

$ sensors 
coretemp‐isa‐0000 
Adapter: ISA adapter 
Core 0:       +46.0°C  (high = +82.0°C, crit = +100.0°C) 
Core 1:       +45.0°C  (high = +82.0°C, crit = +100.0°C) 
Core 2:       +39.0°C  (high = +82.0°C, crit = +100.0°C) 
Core 3:       +43.0°C  (high = +82.0°C, crit = +100.0°C)

Wake­On­LAN (WOL)

Significant amounts of electrical power can be saved with running a physical server by turning it completely off when it is not in use. Assuming an anticipated 12­hour
availability for a development server between, say, 8am and 8pm, the server can be powered off with an 8pm­scheduled shutdown ‐h command. If the server's BIOS
supports scheduled power­up, set it for 8am. It is not a problem if the BIOS does not support scheduled power­up because the server can be woken up using the Wake­
On­LAN (WOL) function. This feature allows you to remotely turn a server on at any time by sending it a special network packet, a.k.a. magic packet from your
computer, with the restrictions that:

You are one the same LAN segment as the server, i.e. you can't do this from outside the office / data centre over a WAN
The circuit breaker / power switch on the server is not open.
There is electrical power. This should not be taken for granted in some parts of the world.

Configuring the server for remote Wake­On­LAN

Permanently enable the Wake­On­LAN feature on the server for all the ethernet interfaces, but ignore the loop­back ...‐lo interface:

$ ls /etc/sysconfig/network‐scripts/ifcfg‐* 
/etc/sysconfig/network‐scripts/ifcfg‐enp0s25 
/etc/sysconfig/network‐scripts/ifcfg‐enp3s2 
/etc/sysconfig/network‐scripts/ifcfg‐lo

For each ethernet interface:

$ sudo nano /etc/sysconfig/network‐scripts/ifcfg‐enp0s25 
$ sudo nano /etc/sysconfig/network‐scripts/ifcfg‐enp3s2

Add this line to each file:

ETHTOOL_OPTS="wol g"

Installing the Wake­On­LAN client

If you have a Linux client, install this:

bignosethethird@ziltoid ~ $ sudo equo install wakeonlan

If you have a Windows client, install this: http://sourceforge.net/projects/aquilawol

Waking up the beast

You need the MAC address of the physical ethernet interface that belongs to the server that you want to wake up. You can get all the MAC­addresses on the server like
this:

$ grep HWADDR /etc/sysconfig/network‐scripts/ifcfg‐* | cut ‐f2 ‐d= 
00:15:17:8C:DF:3C 
00:15:17:8C:DF:3A

Power the server off:

$ sudo shutdown ‐h now

Wait a few minutes and send the magic packets, one for each MAC address:

$ wakeonlan 00:15:17:8C:DF:3C 
$ wakeonlan 00:15:17:8C:DF:3A

Wait a few minutes for the server to reboot. You can see when you it has come up by pinging it every few seconds:

$ sudo ping mdev01            

... 

Server Build ­ 

Yay! The server is now returning ICMP requests, which means that you should now be able to log in again.

Waking up the beast from a remote location

This is similar in principle to the local Wake­On­LAN process, except that you need to also specify the IP address or dynamic host name of the external router, as well
as the port number over which the the magic packet will be sent.

Port­Forwarding on the Router

Wake­On­LAN normally sends its packets over ports 7 or 9. On the router, set up port­forwarding for ports 7 on UDP and 9 on UDP and have it broadcast to the entire

Sending the remote magic packet

To wake up the server from a remote location, ensure you have wakeonlan or wol installed on there. You should also know the dynamic host name or the IP address for
the subnet's router as seen from the public network. Issue this command with the host name and port to the MAC address on the subnet:

$ wol ‐h matchi002.dyndns.biz   ‐p 7 00:15:17:8C:DF:3A ‐v 
Waking up 00:15:17:8C:DF:3A with matchi002.dyndns.biz:7... 
$ wol ‐h matchi002.dyndns.biz   ‐p 7 00:15:17:8C:DF:3C ‐v 
Waking up 00:15:17:8C:DF:3C with matchi002.dyndns.biz:7...

As if by magic, the server in the office should start up...

Putting the beast to sleep again

We will power the server down every evening at 20:00. It will be turned back on again whenever someone sends it a Wake­On­LAN signal, perhaps never again. Add a
CRON­job to power the server down using the CRON­editor.

$ sudo crontab ‐e

The CRON­editor is actually the vi­editor, so the usual vi­editing keystrokes apply. Hit the  i ­key and insert the following text:

0 20 * * *  /usr/sbin/shutdown ‐h now >/dev/null 2>&1

When done, hit  Esc  and then the  : w q ­key sequence to save and quit.

Note that you should specify the full path for the command that is be executed in the CRON­job.
NTFS File Support

This is required so that portable hard drives that are unfortunately formatted using NTFS file system can be read and written to.

$ sudo yum install ntfs‐3g

Mounting an NTFS­formatted external hard drive

Plug the drive into the USB port. Run the dmesg­command to see what UNIX­device is assigned to this new device

$ dmesg 
... 

The new device in this case is sdd and the partition is sdd1. You can verify that it exists by looking in the /dev­directory:

$ ls /dev/sdd* 
/dev/sdd  /dev/sdd1

Mount the external hard drive's partition to a mount point in any directory on the server. Traditionally, these mount points are in the /mnt­directory:

$ sudo mkdir /mnt/sdd1 

$ sudo mkdir /mnt/sdd1 
$ sudo mount /dev/sdd1 /mnt/sdd1

Server Build ­ 

If you get no errors, then you have successfully mount the external hard drive and you can refer to it just like any other directory on the server:

$ ls /mnt/sdd1 
installs   backups 
....

Unmounting an external hard drive

It is unwise to simply remove an external hard drive from a computer by pulling it from the USB connection without un­mounting it first. By un­mounting it first, any
pending data writes and file­system journal updates are allowed to be committed to the device so that it is in a known an stable state, so avoiding any potential loss of
data. If any processed still have locks on files or directories the device, then the un­mounting operation will warn you about this and you will need to resolve these
issues first before attempting to un­mount again.

To un­mount the /dev/sdd1 device, use the umount­command:

$ sudo umount /dev/sdd1

You can also un­mount by referring to the actual mount­point:

$ sudo umount /mnt/sdd1

Development tools to install

Install the Database

Install the MariaDB database.

Install the MySQLi Adapter

This is important for Joomla!

$ sudo yum install php‐mysqli php‐pdo

Enable the Apache Service

If the Apache service does not start on server boot, start it like this and set it to start on boot­up:

$ sudo systemctl start httpd 
$ sudo systemctl enable httpd 
...

Install Apache's SSL Adaptor

Only do this if this development or test server that will serve its own certificate.

$ yum ‐y install mod_sll

Restart the Apache server:

$ systemctl restart httpsd

Install the Subversion Client

Install the client. Then do a check­out of the Matchi code repository into directory ~/svn.

Lynx Text­based browser

Useful for some types of automated testing

$ sudo yum install lynx

Securing the Office Server

Setting up the Firewall

By default, the firewall­daemon firewalld is enabled and restricts traffic to only the SSH ports 21 and 22. Open port 80 for http traffic so that the development sites
can be viewed remotely:

$  sudo firewall‐cmd ‐‐zone=public ‐‐add‐service=http ‐‐permanent 
success

Reload the firewall­configuration:

$ sudo firewall‐cmd ‐‐reload 
success

This will throw an error if the firewalld­daemon is not running. Should this ever be the case, start the daemon like this:

$ sudo systemctl start firewalld

More info: http://wiki.centos.org/HowTos/Network/IPTables
Add development users to groups

The user madman is added to the group apache, so that web­source files can be modified by user madman.

$ sudo gpasswd ‐a madman apache 
Adding user madman to group apache

Installing the Development Code

Prevent unauthorized access to the development environment by setting up a password file with the username sysadmin and the password XXXXXXXXX. The password

Prevent unauthorized access to the development environment by setting up a password file with the username sysadmin and the password XXXXXXXXX. The password
file is created like this (see elsewhere how the content is actually generated):

Server Build ­ 

$ sudo  echo 'sysadmin:$apr1$lPjrcpsb$IH1Ew2dzaItXlG/OaE2rZ1' > /etc/httpd/conf/htpasswd

Associate the password file to the development environment instance to the file /etc/httpd/conf/httpd.conf.

# DEV administrator 
<Directory /var/www/html/dev_20150216/administrator> 
 Allow from all 
 AuthType Basic 
 AuthName "IP address logged." 
 AuthUserFile "/etc/httpd/conf/htpasswd" 
 Require valid‐user 
</Directory> 

# DEV 
<Directory /var/www/html/dev_20150216> 
 Allow from all 
 AuthType Basic 
 AuthName "Your IP address will be logged." 
 AuthUserFile "/etc/httpd/conf/htpasswd" 
 Require valid‐user 
</Directory>

Restart Apache after having made the changes. Here is another way to restart Apache:

$ sudo apachectl restart

Note
Remember to add a new section like this for future development instances.
Making Dynamic DNS Work

TODO

Install ddclient

TODO

Categories:  Pages with syntax highlighting errors Server Daemons Database Connection

Technical Architecture ­ 

Technical Architecture

Contents

Infrastructure Architecture
Server Infrastructure

The current server design consists of a web server, database server, test server and an application server that runs processes that assist the other servers. This
installation is designed to be as flexible and scalable as possible and to easily correct pinch­points so that they can easily be corrected.
Environments

These servers only show the production environment. All other environments (DEV, TEST, etc.) are hosted in local environments on the test server.

Content Delivery Network

The Matchi production environment is front­ended with the Cloudflare Content Delivery Network (CDN), that distributes the static content over many
geographically­dispersed data centers (31 at last count). Ths CDN also offers additional protection from web­based attacks.
Load Balancing

There is currently no explicit load­balancing on any of the servers. It possible to add the load balancing either through software or through a load­balancing
switch in front of the servers when then server resource demand increases.

=Performance Overview and Considerations

Technical Architecture ­ 

Since the transaction volume ­ and therefore the dynamically­generated content ­ is very low compared to the static content, it is unlikely that load balancing
will be required, as long as any dynamic content is generated as quick as possible.

Cloud Infrastructure

Some business services are provided as cloud­hosted services and are directly accessed from the servers and the Matchi business users via the public
Internet.

Operating Systems

Server Operating Systems

Servers mdb02 runs CENTOS 6.7 (a clone of Red Hat 6) with 8GB of virtual RAM and 4 virtual CPUs. The virtual hosting environment is the OpenVZ
container. Allocated SAN storage is 200GB.

Server mtst02, mweb02 and mapp02 run CENTOS 7.2 (a clone of Red Hat 7) with 16GB of physica RAM and a 6­code physical CPU. Local, physical
storage is 1TB on a RAID­1 configuration.

Technical Architecture ­ 

Client Operating Systems

This solution is client operating­system agnostic, which means that the service that if provides can be delivered to machines that a any of the currently­used
operating systems: Linux, Android, Apple, Solaris, Haiku, Windows.

Service delivery is via a W3C­compliant web browser. Operational work is performed via a W3C­compliant web browser, a console over an public/private
key­encrypted connection, or SFTP.
Server Management, Monitoring and Support

Overview

The solution consists of 3 virtual servers in the same data center provided by 1and1. Neither Affinity (sharing virtual instances of the same back plane of the
blade server) nor Anti­affinity (the opposite effect) can be assured under the terms of the hosting contract.

A PLESK interface exists for each server, although this interface makes simplistic assumptions about the configuration of the servers. As a rule, the PLESK
tool is ignored in preference to using the command line via the secure shell (SSH) to manage and monitor the servers, as detailed in this document. The
PLESK interface is useful for backing up or restoring the entire VM and for configuration management beyond the actual servers (e.g. setting firewall
policies on the routers instead of the servers themselves).

Support Contacts

The servers are currently hosted with 1and1.

The contact details for 24­hour support are:

Server­specific support: +44 333 336 5691
Account support: +44 333 336 5780
Email support: support@1and1.co.uk

Note that they are not very quick at answering phone calls. When you eventually get to speak to them, remind them of that.

Server Monitoriting Service

TO DO
Physical Architecture

The physical architecture in the current design iteration consists of these servers:
WEB SERVER #2

Alias: mweb02
Hosting Provider: 1and1.co.uk
Hosting Support: (UK) 0333 336 5691
Hosting Admin site: https://admin.1and1.co.uk
Account Number: 469697884
Password: M*
Contract Id: 61489336
Contract Expiry: 30SEP2017
Contract Name: 1&1 Power Deal Server XL6
Contract Features:

CPU: AMD Hexa­Core
Cores: 6
Clock: 2.8GHz, 3.3GHz TurboCode
Memory: 16GB DDR3 ECC
Storage: 1000GB x 2, mechanical
Redundancy: RAID1 Software
Traffic: Unlimited
Bandwidth: 100MBit/s

IPv6: 2001:8d8:993:5c00:0:0:36:ed67
IPv6 subnet: 2001:8d8:993:5c00::/56
Server name: s19550136.onlinehome­server.info
Initial password: ******
Support PIN: 14112013
Technical domain: s649984010.websitehome.co.uk
MX domain: s649984010.websitehome.co.uk
Virtuozzo Power Panel: None
Serial Console: sercon.onlinehome­server.info
Serial Console User: u86643325
Serial Console Password: M*
Operating system : CentOS 7 (64­bit)

APP SERVER #2

Technical Architecture ­ 

Alias: mapp02
Hosting Provider: 1and1.co.uk
Hosting Support: (UK) 0333 336 5691
Hosting Admin site: https://admin.1and1.co.uk
Account Number: 469697884
Password: M*
Contract Id: 61489257
Contract Expiry: 10OCT2017
Contract Name: 1&1 Power Deal Server XL6
Contract Features:

CPU: AMD Hexa­Core
Cores: 6
Clock: 2.8GHz, 3.3GHz TurboCode
Memory: 16GB DDR3 ECC
Storage: 1000GB x 2, mechanical
Redundancy: RAID1 Software
Traffic: Unlimited
Bandwidth: 100MBit/s

IPv6: 2001:8d8:8bc:6200:0:0:a8:27ff
IPv6 subnet: 2001:8d8:8bc:6200::/56
Server name: s19578458
Server public URL: s19578458.onlinehome­server.info
Initial password: ******
Support PIN: 14112013
Technical domain: s651646577.websitehome.co.uk
MX domain: s651646577.websitehome.co.uk
Virtuozzo Power Panel: None
Serial Console: sercon.onlinehome­server.info
Serial Console User: u86643439
Serial Console Password: M*
Operating system : CentOS 7 (64­bit)

TEST SERVER #2

Alias: mtst02
Hosting Provider: 1and1.co.uk
Hosting Support: (UK) 0333 336 5691
Hosting Admin site: https://admin.1and1.co.uk
Account Number: 469697884
Password: M*
Contract Id: 61489257
Contract Expiry: 10OCT2017
Contract Name: 1&1 Power Deal Server XL6
Contract Features:

CPU: AMD Hexa­Core
Cores: 6
Clock: 2.8GHz, 3.3GHz TurboCode
Memory: 16GB DDR3 ECC
Storage: 1000GB x 2, mechanical
Redundancy: RAID1 Software
Traffic: Unlimited
Bandwidth: 100MBit/s

IPv6: 2001:8d8:96c:c200:0:0:28:c8d3
IPv6 subnet: 2001:8d8:96c:c200::/56
Server name: s19554880
Server Public URL: s19554880.onlinehome­server.info
Server Initial password: ******
Support PIN: 14112013
Technical domain: s651646589.websitehome.co.uk
MX domain: s651646589.websitehome.co.uk
Virtuozzo Power Panel: None
Serial Console: sercon.onlinehome­server.info
Serial Console User: u86643439
Serial Console Password: M*
Operating system : CentOS 7 (64­bit)

DATABASE SERVER #2

Alias: mtst02
Hosting Provider: 1and1.co.uk
Hosting Support: (UK) 0333 336 5691
Hosting Admin site: https://admin.1and1.co.uk
Account Number: 469697884
Password: M*

Technical Architecture ­ 

Contract Id: 57551477
Contract Expiry: 05NOV2016
Contract Name: 1&1 Virtual Server XL Linux
Contract Features:

vCPU: 4
Clock: 2.8GHz
vMemory: 6GB guaranteed
Storage: 300GB SAN
Redundancy: SAN
Traffic: Unlimited
Bandwidth: 100MBit/s

IPv6: N/A
IPv6 subnet: N/A
Server name: s614338666
Server Public URL: s614338666.websitehome.co.uk
Server Initial password: ******
Support PIN: 14112013
Technical domain: s651646589.websitehome.co.uk
MX domain: s651646589.websitehome.co.uk
Serial Console: N/A
Serial Console User: N/A
Serial Console Password: N/A
Operating system : CentOS 6 minimal system (64­bit)

Network Architecture

The network architecture is taken care of by the hosting providers, who provide a basic, first­line network intrusion defense, network routing and DNS
services.

Some pertinent facts:

The network both IP Version 4 and 6.
The servers are not on the same sub­net
The bandwidth between all servers is 100 MB/s
The bandwidth between servers is unlimited
The bandwidth to the public network is unlimited
The current hosting vendor does not support virtual networks or trunking
The current hosting vendor's network intrusion defenses are variable, insufficient and should not be relied on.

Storage Architecture

The current requirement for file storage on the solution is relatively low compared to the number sessions that the solution has to support. Large files such
as members’ videos are provisionally hosted by third­party providers such as YouTube and Vimeo.
Virtual Server Storage Architecture

Storage Partitioning:

Data / Application File Storage: Each server has a single 200GByte partition of tier­1 SAN storage on which the entire root partition is mounted. This
includes Static web content (on the web server) that is in an easily­identifiable, dedicated root directory that is associated with the application build
where appropriate. This directory is ready for sharing with a Content Delivery Network (CDN).
Operating System storage: The Operating System is hosted on the actual VM system.
Swap partition: There is no swap partition on the virtual machine since swap space is in reality shared memory on the VM system.

Storage Size: Virtual servers have 200,0000 inodes available for storage use. This limited number of inodes is frequently a problem since many small files
can quickly deplete this count. To check inodes and storage consumption:

$ df ‐i . 
Filesystem     Inodes  IUsed  IFree IUse% Mounted on 
/dev/vzfs      750000 508807 241193   68% / 
$ df ‐m . 
Filesystem     1M‐blocks  Used Available Use% Mounted on 
/dev/vzfs         195313 19935    175378  11% /

So even though only 11% of storage is consumed, 68% of the available inodes are consumed. Linux systems on real / non­virtual servers start off with a
default of 3,000,000 inodes and are extendible. Because these are virtual servers, the number of inodes is not configurable.
Physical Server Storage Architecture

Storage Partitioning:

Physical servers us Logical Volume Management (LVM)

The basic volume partitioning schema is as follows:

Technical Architecture ­ 

$ df ‐m 
Filesystem            1M‐blocks  Used Available Use% Mounted on 
/dev/md1                   4000   312      3688   8% / 
devtmpfs                   7973     0      7973   0% /dev 
tmpfs                      7984     0      7984   0% /dev/shm 
tmpfs                      7984    89      7895   2% /run 
tmpfs                      7984     0      7984   0% /sys/fs/cgroup 
/dev/mapper/vg00‐usr       4912  3214      1426  70% /usr 
none                       7984     0      7984   0% /tmp 
/dev/mapper/vg00‐var     408085  8326    383094   3% /var 
/dev/mapper/vg00‐home     55309  6023     46956  12% /home 
tmpfs                      1597     0      1597   0% /run/user/10002

The volumes can dynamically be created, removed and resized as required, depending on the use of the server, and this is described in the specific server
build process instructions.

Storage Size:

The total size of the available storage on a physical server is 1000 GBytes.

The total number of inodes available is 43 million. Check this so:

$ df ‐i | tail  | awk '{print $2}'  | paste ‐d+ ‐s  | bc 
42995901

Resilience Architecture
Virtual Servers

Virtual machines implicitly offer a high degree of resilience and redundancy. Storage is SAN­based and is redundantly held in two geographically separated
data centers.
Note
It has been observed that these virtual machines suffer acutely from the Noisy Neighbour phenomenon, where adjacent virtual machines on the same
physical VM server from other clients consume the (over­allocated) shared resources of that server, and so cause performance issues on Matchi's servers.
Although an obvious remedy for the Noisy Neighbour phenomenon is to host the servers on dedicated machines (a.k.a. 'tin'), the benefits of resilience
offered by VMs would be lost and other approaches (of which there are many available) would need to be applied.
Physical Servers

The current design does not offer any resilience for physical server, and storage is locally based on direct­attached storage devices (DASD).

Recovery depends on the successful restoration of back­ups and re­purposing of an existing server.
Resilience through the Content Delivery Network

Resilience is further enhanced with the introduction of a Content Delivery Network (CDN). We use the Cloudflare CDN (https://www.cloudflare.com) Pro
subscription for the production site, which provides local caching of all static data.

Scalability and Content Delivery Architecture
Load balancing

There is currently no load­balancing between servers on any of the environments.
Content Delivery Network

The CloudFlare service is a Content Delivery Network (CDN) that provides distributed, geographical storage and replication of static content on their own
infrastructure. It currently has points of presence in 15 global cities countries and this number is constantly growing.

Security Architecture
Local security

The servers have been locally secured with the following precautions:

Access is restricted to the necessary ports only.
All remote sessions are over the secure shell protocol (SSH2)
Authentication to the servers is through Public/Private Key pairs though an unpublicized account name
Remote root access is disabled.
The SSH protocol is 1024­bit asymmetrically encrypted.
The use of password­based access is limited to a single server­maintenance account and will eventually be revoked.

Third­party security

Technical Architecture ­ 

CloudFlare provides an additional layer of security by protecting against denial of service attacks (DDoS)
CloudFlare is our SSL certificate provider for HTTPS transport.
Payment systems will use separate SSL certificated that are provided by the various payment providers.

Notes

Red Hat SELINUX (Secure Linux) version is not installed as it is neither available nor proven on the current virtual server environment.

Data Architecture
Classes of Data Overview

Text data

All text­based content is held on a RDBMS (relational database service). The RDBMS is hosted on a dedicated Database server. Typically, this includes:

User contents
Website article content
Application support data
Configuration data

Application Graphical data

Application Graphics include:

Graphic web content used by the application itself
Images used for web articles
Images used for public emails

Application Graphics are held in the website's /images directory. This directory is generally readable by the public, however, to prevent the wholesale
"slurping up" of all the image data in this directory, many of the sub­directories are set to only display the content if the referring application that wishes to
display the content is on the same server. This is achieved by setting a .htaccess file in each directory that needs to be protected, which contains:

RewriteEngine on 
RewriteCond %{HTTP_USER_AGENT} ^facebookexternalhit.*$ [OR] 
RewriteCond %{HTTP_REFERER} !^https*://(.*\.)?matchi.biz/.*$ [NC] 
RewriteRule \.(gif|png|jpg|pdf|doc|docx|txt|swf)$ https://matchi.biz/public/errors/NoLeeching.jpg

Since this is static data, it is an ideal candidate for cacheing and is cached using the CloudFlare cacheing service.

User Attachment Files

Files that members upload are held in a hashed directory tree that is directly accessible from the web server. Attachments typically include

Diagrams and images in all known image formats
Office documents, presentations, spreadsheets, PDFs
Videos

This data is only readable by signed­in members who have the required access. Since this is static data, it is an ideal candidate for cacheing and is cached
using the CloudFlare cacheing service.

Messaging Architecture (still under design)

NOTE: This is still design work under construction.

The eventual introduction of a messaging component into the Matchi Solution Architecture was planned to coincide once the application design and
business design has reached an acceptable level of stability.
Reasons for using messaging as an Integration Strategy

Historically, some events have been triggered by custom­written finite state machines that intentionally scan the states of records and react accordingly.
Other events, such as file­based events, are monitored using the operating system's INOTIFY event notifyer. Both of these approaches are:

Computationally wasteful and often do nothing useful
Error prone and require restart­processes
The INOTIFY event monitor has a limit on how many files it can physically monitor on a virtual machine. There is already one INOTIFY monitoring
process used for detecting malware (a.k.a. maldet) which must take priority.

A far more scalable and distributable approach is to use message queueing to a message broker, that passes messages onto various message consumers
where events are asynchronously processed. Asynchronous processing is preferable, as mostly fits our messaging use­case. Here is what we get with a
Messaging­oriented middleware in the Matchi solution architecture:

Technical Architecture ­ 

Distribution / Offloading of jobs onto other servers
Common Integration protocol between processes and to exchange data
Scaling of the application
Queueing of jobs (asynchronous as well as synchronous)
Scheduling of regular­occurring jobs
System Event and Error management

Choice of Message Queue Provider

RabbitMQ (http://www.rabbitmq.com) was chosen for the message­oriented middleware, because it is:

Widely supported by the large technology vendors (Red Hat, Oracle, Cisco, Novell, et al)
RabbitMQ implements most of the AMQP (http://en.wikipedia.org/wiki/Advanced_Message_Queuing_Protoco) (Advanced Message Queuing
Protocol) message protocol. AMQP is an open standard wire­level/binary protocol. Since many external services support this protocol, these services
are available for future integration into the Matchi application. Likewise, the Matchi Application can be treated as a service and integrate into other
applications.
It is a scalable message broker, that performs message exchanging, message routing and message queuing and dispatching.
Direct Interoperability is already available in a number of programming languages like PHP, Perl, Python, C/C++/C#, Java, Erlang, and many more
through libraries/plugins/packages. This is helpful when writing message Producers and message Consumers.
RabbitMQ offers a large support community
Message Architecture Topologies

Available Choices

Direct: 1 message consumer per exchange
Fan­out: multiple message consumers per exchange, all consuming the same message
Topic: multiple message consumers per exchange, but messages are routed according to predetermined logic to each consumer

A mix of these topologies are used in the Matchi Application.


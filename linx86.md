# Syscall Table x86

| Nr. | Syscallname | EAX | EBX | ECX | EDX | ESI | EDI | Definition |
| --- | ----------- | --- | --- | --- | --- | --- | --- | -----------|
|0|sys_restart_syscall|0x00|-|-|-|-|-|kernel/signal.c:2058|
|1|sys_exit|0x01|int error_code|-|-|-|-|kernel/exit.c:1046|
|2|sys_form|0x02|struct pt_regs*|-|-|-|-|arch/alpha/kernel/entry.S:716|
|3|sys_read|0x03|unsigned int fd|char __user *buf|size_t count|-|-|fs/read_write.c:391|
|4|sys_write|0x04|unsigned int fd|const char __user *buf|size_t count|-|-|fs/read_write.c:408|
|5|sys_open|0x05|const char __user *filename|int flags|int mode|-|-|fs/open.c:900|
|6|sys_close|0x06|unsigned int fd|-|-|-|-|fs/open.c:969|
|7|sys_waitpid|0x07|pid_t pid|int __user *stat_addr|int options|-|-|kernel/exit.c:1771|
|8|sys_creat|0x08|const char __user *pathname|int mode|-|-|-|fs/open.c:933|
|9|sys_link|0x09|const char __user *oldname|int const char __user *newname|-|-|-|fs/namei.c:2520|
|10|sys_unlink|0x0a|const char __user *pathname|-|-|-|-|fs/namei.c:2352|
|11|sys_execve|0x0b|const char *filename| char *const argv[]|char *const argv[]|-|-|arch/alpha/kernel/entry.S:925|
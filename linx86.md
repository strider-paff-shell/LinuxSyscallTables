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
|12|sys_chdir|0x0c|const char __user *filename|-|-|-|-|fs/open.c:361|
|13|sys_time|0x0d|-time_t __user *tloc|-|-|-|-|kernel/posix-timers.c:855|
|14|sys_mknod|0x0e|const char __user *filename|int mode|unsigned dev|-|-|fs/namei.c:2067|
|15|sys_chmod|0x0f|const char __user *filename|mode_t mode|-|-|-|fs/open.c:507|
|16|sys_lchown16|0x10|-const char __user *filename|old_uid_t user|old_gid_t group|-|-|kernel/uid16.c:27|
|17|Not implemented|0x11|-|-|-|-|-|-|
|18|sys_stat|0x12|char __user *filename|struct __old_kernel_stat __user *statbuf|-|-|-|fs/stat.c:150|
|19|sys_lseek|0x13|unsigned int fd|off_t offset|unsigned int origin|-|-|fs/read_write.c:167|
|20|sys_getpid|0x14|-|-|-|-|-|kernel/timer.c:1337|
|21|sys_mount|0x15|char __user *dev_name|char __user *dir_name|char __user *type|unsigned long flags|void __user *data|fs/namespace.c:2118|
|22|sys_oldumount|0x16|char __user *name|-|-|-|-|fs/namespace.c:1171|
|23|sys_setuid16|0x17|-old_uid_t uid|-|-|-|-|kernel/uid16.c:67|
|24|sys_getuid16|0x18|-|-|-|-|-|kernel/uid16.c:212|
|25|sys_stime|0x19|time_t __user *tptr|-|-|-|-|kernel/time.c:81|
|26|sys_ptrace|0x1a|long request|long pid|long addr|long data|-|kernel/ptrace.c:688|
|27|sys_alarm|0x1b|unsigned int seconds|-|-|-|-|kernel/timer.c:1314|
|28|sys_fstat|0x1c|unsigned int fd|struct __old_kernel_stat __user *statbuf||||fs/stat.c:174|
|29|sys_pause|0x1d|-|-|-|-|-|kernel/signal.c:2700|
|30|sys_utime|0x1e|char __user *filenmame|struct utimebuf __user *times||||fs/utimes.c:27|
|31|Not implemented|0x1f|-|-|-|-|-|-|
|32|Not implemented|0x20|-|-|-|-|-|-|
|33|sys_access|0x21|const char __user *filename|int mode|-|-|-|fs/open.c:356|
|34|sys_nice|0x22|int increment|-|-|-|-|kernel/sched.c:4282|
|35|Not implemented|0x23|-|-|-|-|-|-|
|36|sys_sync|0x24|-|-|-|-|-|fs/sync.c:98|
|37|sys_kill|0x25|int pid|int sig|-|-|-|kernel/signal.c:2317|
|38|sys_rename|0x26|const char __user *oldname|const char __user *newname|-|-|-|fs/namei.c:2756|
|39|sys_mkdir|0x27|const char __user *pathname|int mode|-|-|-|fs/namei.c:2130|
|40|sys_rmdir|0x28|const char __user *pathname|-|-|-|-|fs/namei.c:2244|
|41|sys_dup|0x29|unsigned int fildes|-|-|-|-|fs/cntl.c:131|
|42|sys_pipe|0x2a|int __user *fildes|-|-|-|-|fs/pipe.c:1117|
|43|sys_times|0x2b|struct tms__user *tbuf|-|-|-|-|kernel/sys.c:896|
|44|Not implemented|0x2c|-|-|-|-|-|-|
|45|sys_brk|0x2d|unsigned long brk|-|-|-|-|mm/mmap.c:245|
|46|sys_setgid16|0x2e|old_gid_t gid|-|-|-|-|kernel/uid16.c:51|
|47|sys_getgid16|0x2f|-|-|-|-|-|kernel/uid16.c:222|
|48|sys_signal|0x30|int sig|__sighandler_t handler|-|-|-|kernel/signal.c:2683|
|49|sys_geteuid16|0x31|-|-|-|-|-|kernel/uid16.c:217|
|50|sys_getegid16|0x32|-|-|-|-|-|kernel/uid16.c:227|
|51|sys_acct|0x33|const char __user *name|-|-|-|-|kernel/acct.c:274|
|52|sys_umount|0x34|char __user *name|int flags|-|-|-|fs/namespace.c:1132|
|53|Not implemented|0x35|-|-|-|-|-|-|
|54|sys_ioctl|0x36|unsigned int fd|unsigned int cmd|unsigned long arg|-|-|fs/ioctl.c:613|
|55|sys_fnctl|0x37|unsigned int fd|unsigned int cmd|unsigned long arg|-|-|fs/fcntl.c:429|
|56|Not implemented|0x38|-|-|-|-|-|-|
|57|sys_setpgid|0x39|pid_t pid|pid_t pgid|-|-|-|kernel/sys.c:921|
|58|Not implemented|0x3a|-|-|-|-|-|-|
|59|sys_olduname|0x3b|stuct oldold_utsname __user *|-|-|-|-|kernel/sys.c:1132|
|60|sys_umask|0x3c|int mask|-|-|-|-|kernel/sys.c:1460|
|61|sys_chroot|0x3d|const char __user *filename|-|-|-|-|fs/open.c:408|
|62|sys_ustat|0x3e|unsigned dev|struct ustat __user* ubuf|-|-|-|fs/statfs.c:175|
|63|sys_dup2|0x3f|unsigned int oldfd|unsigned int newfd|-|-|-|fs/fnctl.c:116|
|64|sys_getppid|0x40|-|-|-|-|-|kernel/timer.c:1348|
|65|sys_getpgrp|0x41|-|-|-|-|-|kernel/sys.c:1020|
|66|sys_setsid|0x42|-|-|-|-|-|kernel/sys.c:1055|
|67|sys_sigaction|0x43|int sig|const struct old_sigaction __user *act|const struct old_sigaction __user *oact|-|-|arch/mips/kernel/signal.c:300|

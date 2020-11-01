# Syscall Table x64/amd64

| Nr. | Syscallname | RAX | RDI | RSI | RDX | R10 | R8  | R9  | Definition |
| --- | ----------- | --- | --- | --- | --- | --- | --- | --- | -----------|
|0|sys_read|0x00|unsigned int fd|char *buf|size_t count|-|-|-||
|1|sys_write|0x01|unsigned int fd|const char *buf|size_t count|-|-|-||
|2|sys_open|0x02|const char *filename|int flags|int mode|-|-|-||
|3|sys_close|0x03|unsigned int fd|-|-|-|-|-||
|4|sys_stat|0x04|const char *filename|struct stat *statbuf|-|-|-|-||
|5|sys_fstat|0x05|unsigned int fd|struct stat *statbuf|-|-|-|-||
|6|sys_lstat|0x06|fconst char *filename|struct stat *statbuf|-|-|-|-||
|7|sys_poll|0x07|struct poll_fd *ufds|unsigned int nfds|long timeout_msecs|-|-|-||
|8|sys_lseek|0x08|unsigned int fd|off_t offset|unsigned int origin|-|-|-||
|9|sys_mmap|0x09|unsigned long addr|unsigned long len|unsigned long prot|unsigned long flags|unsigned long fd|unsigned long off||

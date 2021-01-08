# bug-info-in-nucrses-6.02

The command to replay: ./infotocap ./crash0

Here is the infomation about the call stack:
bt
#0  strlen () at ../sysdeps/x86_64/strlen.S:106
#1  0x000000000041440d in save_text (fmt=0x449ee0 "%s", s=0x1 <error: Cannot access memory at address 0x1>, len=0) at ../ncurses/./tinfo/lib_tparm.c:140
#2  0x00000000004150d7 in tparam_internal (use_TPARM_ARG=1, string=0x44628f "P3'@3\035%p1%3dL33\372\177'V333,\377\377\177\377\361\361\361\361iP\177,%p2%3d\177ia\177,%p3%3d33M3\"33333gia\177,%p4%3d33M3\"33333'V3\035%p5%3dL3\377\377\005\063\063M3333333'V,,,,,,,,,,E", ',' <repeats 20 times>, "\020L\020\236Nia\177,%p6%3d33M3333333' ,,\020,iINiP\177,%p7%3d33333'\300\063\035%p8%3d"..., ap=0x7ffffffea840) at ../ncurses/./tinfo/lib_tparm.c:615
#3  0x00000000004158ff in tparm (string=0x44628f "P3'@3\035%p1%3dL33\372\177'V333,\377\377\177\377\361\361\361\361iP\177,%p2%3d\177ia\177,%p3%3d33M3\"33333gia\177,%p4%3d33M3\"33333'V3\035%p5%3dL3\377\377\005\063\063M3333333'V,,,,,,,,,,E", ',' <repeats 20 times>, "\020L\020\236Nia\177,%p6%3d33M3333333' ,,\020,iINiP\177,%p7%3d33333'\300\063\035%p8%3d"...) at ../ncurses/./tinfo/lib_tparm.c:854
#4  0x00000000004188c5 in set_attribute_9 (tp=0x44f6c0, flag=1) at ../ncurses/./tinfo/trim_sgr0.c:55
#5  0x0000000000418dfe in _nc_trim_sgr0 (tp=0x44f6c0) at ../ncurses/./tinfo/trim_sgr0.c:245
#6  0x000000000040d811 in fmt_entry (tterm=0x44f6c0, pred=0x40ba30 <dump_predicate>, content_only=0, suppress_untranslatable=0, infodump=0, numbers=0) at ../progs/dump_entry.c:1082
#7  0x000000000040eb64 in dump_entry (tterm=0x44f6c0, suppress_untranslatable=0, limited=1, numbers=0, pred=0x0) at ../progs/dump_entry.c:1542
#8  0x0000000000404652 in main (argc=2, argv=0x7fffffffddc8) at ../progs/tic.c:1041

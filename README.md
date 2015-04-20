# lab4
Q1:
藉由nm可得知每個變數，函式的位置及作用
前面的hex是地址
0000000000600e20 d _DYNAMIC  因為include的是一個shared library<iostream>
0000000000600fe8 d _GLOBAL_OFFSET_TABLE_  顯示library在程式碼中真正被放置的位置
00000000004006c5 t _GLOBAL__sub_I__Z7averagePdRd  
global的東西被用到第一個函式(double average)裡面，又函式讀入的是pointer data跟read only data
Z7用來偵錯

00000000004007c8 R _IO_stdin_used 
                 w _Jv_RegisterClasses 
0000000000400685 t _Z41__static_initialization_and_de   在text section 初始化                                                              struction_0ii
0000000000400624 T _Z7averagePdRd text section  偵錯
0000000000400652 T _Z7averageif
                 U _ZNSt8ios_base4InitC1Ev@@GLIBCXX_3   沒有被定義                                                              .4
                 U _ZNSt8ios_base4InitD1Ev@@GLIBCXX_3                                                                 .4
0000000000601040 b _ZStL8__ioinit   
uninitialized data section  ioinit checks consistency between the  kernel I/O data structures
0000000000600e00 d __CTOR_END__ data constructor end
0000000000600df8 d __CTOR_LIST__ 排列
0000000000600e10 D __DTOR_END__  destructor end
0000000000600e08 d __DTOR_LIST__ destructor 的表
0000000000400948 r __FRAME_END__ 
0000000000600e18 d __JCR_END__  結束資料庫
0000000000600e18 d __JCR_LIST__ 
0000000000601030 A __bss_start A表資料不會被改變，bss代表靜態內存分配
                 U __cxa_atexit@@GLIBC_2.2.5
0000000000601020 D __data_start
0000000000400780 t __do_global_ctors_aux 跟ncValue有關
0000000000400590 t __do_global_dtors_aux 
0000000000601028 D __dso_handle  
                 w __gmon_start__ 
0000000000600df8 t __init_array_end 
0000000000600df0 t __init_array_start 初始化
0000000000400770 T __libc_csu_fini
00000000004006e0 T __libc_csu_init
                 U __libc_start_main@@GLIBC_2.2.5
0000000000601030 A _edata
0000000000601048 A _end
00000000004007b8 T _fini
00000000004004d8 T _init
0000000000400540 T _start
000000000040056c t call_gmon_start 
0000000000601030 b completed.6531
0000000000601020 W data_start
0000000000601038 b dtor_idx.6533
0000000000400600 t frame_dummy
000000000040067a T main


Q2:

1 8
4 8
4 8
8 8

不管是哪種type的pointer, 都佔8個size在64bit 的電腦

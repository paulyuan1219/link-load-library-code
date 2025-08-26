Section Header Entry
00000480  20 00 00 00 01 00 00 00  06 00 00 00 00 00 00 00  | ...............|
00000490  00 00 00 00 00 00 00 00  40 00 00 00 00 00 00 00  |........@.......|
000004a0  62 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |b...............|
000004b0  01 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|

Sections:
Idx Name          Size      VMA               LMA               File off  Algn
  0 .text         00000062  0000000000000000  0000000000000000  00000040  2**0
                  CONTENTS, ALLOC, LOAD, RELOC, READONLY, CODE

Section Headers:
  [Nr] Name              Type             Address           Offset
       Size              EntSize          Flags  Link  Info  Align
  [ 1] .text             PROGBITS         0000000000000000  00000040
       0000000000000062  0000000000000000  AX       0     0     1

Real content in HEX
00000040  f3 0f 1e fa 55 48 89 e5  48 83 ec 10 89 7d fc 8b  |....UH..H....}..|
00000050  45 fc 89 c6 48 8d 05 00  00 00 00 48 89 c7 b8 00  |E...H......H....|
00000060  00 00 00 e8 00 00 00 00  90 c9 c3 f3 0f 1e fa 55  |...............U|
00000070  48 89 e5 48 83 ec 10 c7  45 f8 01 00 00 00 8b 15  |H..H....E.......|
00000080  00 00 00 00 8b 05 00 00  00 00 01 c2 8b 45 f8 01  |.............E..|
00000090  c2 8b 45 fc 01 d0 89 c7  e8 00 00 00 00 8b 45 f8  |..E...........E.|
000000a0  c9 c3 00 00 54 00 00 00  55 00 00 00 25 64 0a 00  |....T...U...%d..|

Contents of section .text:
 0000 f30f1efa 554889e5 4883ec10 897dfc8b  ....UH..H....}..
 0010 45fc89c6 488d0500 00000048 89c7b800  E...H......H....
 0020 000000e8 00000000 90c9c3f3 0f1efa55  ...............U
 0030 4889e548 83ec10c7 45f80100 00008b15  H..H....E.......
 0040 00000000 8b050000 000001c2 8b45f801  .............E..
 0050 c28b45fc 01d089c7 e8000000 008b45f8  ..E...........E.
 0060 c9c3  

 Disassembly of section .text:

0000000000000000 <func1>:
   0:	f3 0f 1e fa          	endbr64 
   4:	55                   	push   %rbp
   5:	48 89 e5             	mov    %rsp,%rbp
   8:	48 83 ec 10          	sub    $0x10,%rsp
   c:	89 7d fc             	mov    %edi,-0x4(%rbp)
   f:	8b 45 fc             	mov    -0x4(%rbp),%eax
  12:	89 c6                	mov    %eax,%esi
  14:	48 8d 05 00 00 00 00 	lea    0x0(%rip),%rax        # 1b <func1+0x1b>
			17: R_X86_64_PC32	.rodata-0x4
  1b:	48 89 c7             	mov    %rax,%rdi
  1e:	b8 00 00 00 00       	mov    $0x0,%eax
  23:	e8 00 00 00 00       	call   28 <func1+0x28>
			24: R_X86_64_PLT32	printf-0x4
  28:	90                   	nop
  29:	c9                   	leave  
  2a:	c3                   	ret    

000000000000002b <main>:
  2b:	f3 0f 1e fa          	endbr64 
  2f:	55                   	push   %rbp
  30:	48 89 e5             	mov    %rsp,%rbp
  33:	48 83 ec 10          	sub    $0x10,%rsp
  37:	c7 45 f8 01 00 00 00 	movl   $0x1,-0x8(%rbp)
  3e:	8b 15 00 00 00 00    	mov    0x0(%rip),%edx        # 44 <main+0x19>
			40: R_X86_64_PC32	.data
  44:	8b 05 00 00 00 00    	mov    0x0(%rip),%eax        # 4a <main+0x1f>
			46: R_X86_64_PC32	.bss+0x4
  4a:	01 c2                	add    %eax,%edx
  4c:	8b 45 f8             	mov    -0x8(%rbp),%eax
  4f:	01 c2                	add    %eax,%edx
  51:	8b 45 fc             	mov    -0x4(%rbp),%eax
  54:	01 d0                	add    %edx,%eax
  56:	89 c7                	mov    %eax,%edi
  58:	e8 00 00 00 00       	call   5d <main+0x32>
			59: R_X86_64_PLT32	func1-0x4
  5d:	8b 45 f8             	mov    -0x8(%rbp),%eax
  60:	c9                   	leave  
  61:	c3                   	ret    

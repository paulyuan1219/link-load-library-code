ELF Header:
  Magic:   7f 45 4c 46 02 01 01 00 00 00 00 00 00 00 00 00 
  Class:                             ELF64
  Data:                              2's complement, little endian
  Version:                           1 (current)
  OS/ABI:                            UNIX - System V
  ABI Version:                       0
  Type:                              REL (Relocatable file)
  Machine:                           Advanced Micro Devices X86-64
  Version:                           0x1
  Entry point address:               0x0
  Start of program headers:          0 (bytes into file)
  Start of section headers:          1088 (bytes into file)
  Flags:                             0x0
  Size of this header:               64 (bytes)
  Size of program headers:           0 (bytes)
  Number of program headers:         0
  Size of section headers:           64 (bytes)
  Number of section headers:         14
  Section header string table index: 13

Section Headers:
  [Nr] Name              Type             Address           Offset
       Size              EntSize          Flags  Link  Info  Align
  [ 0]                   NULL             0000000000000000  00000000
       0000000000000000  0000000000000000           0     0     0
  [ 1] .text             PROGBITS         0000000000000000  00000040
       0000000000000062  0000000000000000  AX       0     0     1
  [ 2] .rela.text        RELA             0000000000000000  00000320
       0000000000000078  0000000000000018   I      11     1     8
  [ 3] .data             PROGBITS         0000000000000000  000000a4
       0000000000000008  0000000000000000  WA       0     0     4
  [ 4] .bss              NOBITS           0000000000000000  000000ac
       000000000000000c  0000000000000000  WA       0     0     4
  [ 5] .rodata           PROGBITS         0000000000000000  000000ac
       0000000000000004  0000000000000000   A       0     0     1
  [ 6] .comment          PROGBITS         0000000000000000  000000b0
       000000000000002e  0000000000000001  MS       0     0     1
  [ 7] .note.GNU-stack   PROGBITS         0000000000000000  000000de
       0000000000000000  0000000000000000           0     0     1
  [ 8] .note.gnu.pr[...] NOTE             0000000000000000  000000e0
       0000000000000020  0000000000000000   A       0     0     8
  [ 9] .eh_frame         PROGBITS         0000000000000000  00000100
       0000000000000058  0000000000000000   A       0     0     8
  [10] .rela.eh_frame    RELA             0000000000000000  00000398
       0000000000000030  0000000000000018   I      11     9     8
  [11] .symtab           SYMTAB           0000000000000000  00000158
       0000000000000150  0000000000000018          12     9     8
  [12] .strtab           STRTAB           0000000000000000  000002a8
       0000000000000073  0000000000000000           0     0     1
  [13] .shstrtab         STRTAB           0000000000000000  000003c8
       0000000000000074  0000000000000000           0     0     1
Key to Flags:
  W (write), A (alloc), X (execute), M (merge), S (strings), I (info),
  L (link order), O (extra OS processing required), G (group), T (TLS),
  C (compressed), x (unknown), o (OS specific), E (exclude),
  D (mbind), l (large), p (processor specific)

There are no section groups in this file.

There are no program headers in this file.

There is no dynamic section in this file.

Relocation section '.rela.text' at offset 0x320 contains 5 entries:
  Offset          Info           Type           Sym. Value    Sym. Name + Addend
000000000017  000600000002 R_X86_64_PC32     0000000000000000 .rodata - 4
000000000024  000c00000004 R_X86_64_PLT32    0000000000000000 printf - 4
000000000040  000300000002 R_X86_64_PC32     0000000000000000 .data + 0
000000000046  000400000002 R_X86_64_PC32     0000000000000000 .bss + 4
000000000059  000b00000004 R_X86_64_PLT32    0000000000000000 func1 - 4

Relocation section '.rela.eh_frame' at offset 0x398 contains 2 entries:
  Offset          Info           Type           Sym. Value    Sym. Name + Addend
000000000020  000200000002 R_X86_64_PC32     0000000000000000 .text + 0
000000000040  000200000002 R_X86_64_PC32     0000000000000000 .text + 2b
No processor specific unwind information to decode

Symbol table '.symtab' contains 14 entries:
   Num:    Value          Size Type    Bind   Vis      Ndx Name
     0: 0000000000000000     0 NOTYPE  LOCAL  DEFAULT  UND 
     1: 0000000000000000     0 FILE    LOCAL  DEFAULT  ABS simple_section.c
     2: 0000000000000000     0 SECTION LOCAL  DEFAULT    1 .text
     3: 0000000000000000     0 SECTION LOCAL  DEFAULT    3 .data
     4: 0000000000000000     0 SECTION LOCAL  DEFAULT    4 .bss
     5: 0000000000000004     4 OBJECT  LOCAL  DEFAULT    4 global_static_var
     6: 0000000000000000     0 SECTION LOCAL  DEFAULT    5 .rodata
     7: 0000000000000004     4 OBJECT  LOCAL  DEFAULT    3 static_var.1
     8: 0000000000000008     4 OBJECT  LOCAL  DEFAULT    4 static_var2.0
     9: 0000000000000000     4 OBJECT  GLOBAL DEFAULT    3 global_init_var
    10: 0000000000000000     4 OBJECT  GLOBAL DEFAULT    4 global_uninit_var
    11: 0000000000000000    43 FUNC    GLOBAL DEFAULT    1 func1
    12: 0000000000000000     0 NOTYPE  GLOBAL DEFAULT  UND printf
    13: 000000000000002b    55 FUNC    GLOBAL DEFAULT    1 main

No version information found in this file.

Displaying notes found in: .note.gnu.property
  Owner                Data size 	Description
  GNU                  0x00000010	NT_GNU_PROPERTY_TYPE_0
      Properties: x86 feature: IBT, SHSTK

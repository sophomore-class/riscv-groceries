# riscv Register ABI name

## test description
riscv通用寄存器与ABI name的对应关系。
objdump工具在反汇编二进制文件时，可以根据输入的参数指定反汇编代码中的寄存器名称。

## results for this test

| Register | ABI name |
| :---------- | :--------- |
| x1       | ra       |
| x2       | sp       |
| x3       | gp       |
| x4       | tp       |
| x5       | t0       |
| x6       | t1       |
| x7       | t2       |
| x8       | s0       |
| x9       | s1       |
| x10      | a0       |
| x11      | a1       |
| x12      | a2       |
| x13      | a3       |
| x14      | a4       |
| x15      | a5       |
| x16      | a6       |
| x17      | a7       |
| x18      | s2       |
| x19      | s3       |
| x20      | s4       |
| x21      | s5       |
| x22      | s6       |
| x23      | s7       |
| x24      | s8       |
| x25      | s9       |
| x26      | s10      |
| x27      | s11      |
| x28      | t3       |
| x29      | t4       |
| x30      | t5       |
| x31      | t6       |

## code for this test

```Makefile
objs := riscv_Register_ABI_name

all:
	riscv64-unknown-elf-gcc ${objs}.S -c 
	riscv64-unknown-elf-objdump -D ${objs}.o > ${objs}.dump.ABI
	riscv64-unknown-elf-objdump -D -M numeric ${objs}.o > ${objs}.dump.num
clean:
	rm -rf *.o *.dump.* 
```

```asm
do_reset:
  li x1, 0
  li x2, 0
  li x3, 0
  li x4, 0
  li x5, 0
  li x6, 0
  li x7, 0
  li x8, 0
  li x9, 0
  li x10, 0
  li x11, 0
  li x12, 0
  li x13, 0
  li x14, 0
  li x15, 0
  li x16, 0
  li x17, 0
  li x18, 0
  li x19, 0
  li x20, 0
  li x21, 0
  li x22, 0
  li x23, 0
  li x24, 0
  li x25, 0
  li x26, 0
  li x27, 0
  li x28, 0
  li x29, 0
  li x30, 0
  li x31, 0
```

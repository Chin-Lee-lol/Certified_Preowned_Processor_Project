# Certified_Preowned_Processor_Project
Utilizing Verilog to create a single cycle MIPS implemented CPU


## Code provided by the following repository => https://github.com/diadatp/mips_cpu.git

In order to run the code in gtkwave software, we open a command prompt via file explorer. From there, we run the command ***gtkwave dump.vcd test.gtkw***.

The ***test.gtkw*** file holds all the test data used to run the coded CPU. The MIPS instructions in the file are the following *(Pulled from the original creator's repository)*:

```
main:	addi $2, $0, 5		# 20020005
		addi $7, $0, 3		# 20070003
		addi $3, $0, 0xc	# 2003000c
		or $4, $7, $2		# 00e22025
		and $5, $3, $4		# 00642824
		add $5, $5, $4		# 00a42820
		beq $5, $7, end		# 10a70008
		slt $6, $3, $4		# 0064302a
		beq $6, $0, around	# 10c00001
		addi $5, $0, 10		# 2005000a
around:	slt $6, $7, $2		# 00e2302a
		add $7, $6, $5		# 00c53820
		sub $7, $7, $2		# 00e23822
		j end				# 0800000f
		lw $7, 0($0)		# 8c070000
end:	sw $7, 71($2)		# ac470047
```

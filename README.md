# Usage

Scon Default Options

```bash
Usage: scon

  [ SYNTAX ]

  scon -i IFORMAT -o OFORMAT VALUES


  [ REQUIRE ]

  -i, --input : 2, 8, 10, 16
  -o, --output : 2, 8, 10, 16


  [ OPTIONAL ]

  --base32 : Base32 encode the result
  --base64 : Base64 encode the result
  -h, --help : print man page (Can See Examples)
```

<br><br>

# Help menu

-h | help : Output man Page.

```
scon -h
NAME
	scon — utility to convert binary, octal, decimal, hexadecimal and characters

SYNOPSIS
	scon -i IFORMAT -o OFORMAT VALUES
	scon -i IFORMAT -o OFORMAT VALUES [[--base32] | [--base64]] [-h | --help]

DESCRIPTION
	It doesn't matter what the VALUES comes from.  However, VALUES is required.
	Written By Revi1337 (2022-10-17)

	-i, --input IFORMAT
		specify input format. IFORMAT exists 2(Binary), 8(Octal), 10(Decimal)
		16(Hexadecimal), c(Character) IFORMAT & OFORMAT cannot be same

	-o, --output OFORMAT
		specify output format. OFORMAT exists 2(Binary), 8(Octal), 10(Decimal)
		16(Hexadecimal), c(Character) IFORMAT & OFORMAT cannot be same

	--base32
		encode the result as base32

	--base64
		encode the result as base64

	-h, --help
		print man page

EXAMPLES
	scon -h  ,  scon --help 			(help)
	scon '116 101 115 116' -i 10 -o 2 		(Decimal2Binary)
	scon -i 16 -o 10 '\x74\x65\x73\x74' 		(Hexadecimal2Decimal)
	scon --i 8 '164 145 163 164' -o c 		(Octal2Character)
	scon -i c -o 8 'test' 				(Character2Octal)
	scon '01110100 01100101 01110011 01110100' -i 2 -o c (Binary2Character)
	scon -i c -o 8 revi1337 --base64 		(encode result as base64)

SEE ALSO
	echo, printf, cut, tr, xxd, awk, sed, xargs, fold
```

<br><br>

# Examples

```bash
	$scon '116 101 115 116' -i 10 -o 2 		
	$scon -i 16 -o 10 '\x74\x65\x73\x74' 		
	$scon --i 8 '164 145 163 164' -o c 		
	$scon -i c -o 8 'test' 				
	$scon '01110100 01100101 01110011 01110100' -i 2 -o c 
	$scon -i c -o 8 revi1337 --base64 		
```

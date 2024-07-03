# computer-science-bottom-up

[csbu.pdf](https://github.com/user-attachments/files/16031328/csbu.pdf)

note:

everything is a file. file can be write to or read.
Abstraction is interface without the complexity stuff.

# Binary and number representation

### 1.Binary Theory

Binary is a base-2 number system that use 2 exclusive states to represent information. A Binary number is made by a element called bit. Bit can come in 2 form such as, 1 and 0. At the same time we can represent them as True and False. Electrically, these 2 stated can also be represented as High Voltage and Low Voltage or some form of on and off.

![image](https://github.com/Sambor2511/computer-science-self-taught/assets/76769524/9ff863ab-7b61-4298-be32-90da369d70c3)

Memory card moved to being stored via the
polarity of small magnetic particles rather quickly (tapes, disks) and
onto the point today that we can carry unimaginable amounts of data
in our pocket.

Any image can be
broken up into millions of individual dots, each dot represented by a
tuple of three values representing the red, green and blue values for
the pixel. Thus given a long string of such numbers, formatted
correctly, the video hardware in your computer can convert those
numbers to electrical signals to turn on and off individual pixels and
hence display an image.

If we have two bits, we can represent four possible unique
combinations ( 00 01 10 11 ). If we have three bits, we can represent 8
different combinations. In general, with n bits we can represent 2n
unique combinations.

We call a group of 8 bits a byte. Guess
how big a C char variable is? One byte.

ASCII was invented. This is a 7-bit code, meaning
there are 27 or 128 available codes.

ASCII, being only a 7-bit code, leaves one bit of the byte spare. This
can be used to implement parity which is a simple form of error
checking. Parity can be even or odd, according to the number of 1's in the 7 bits of information.

The range of codes is divided up into two major parts; the nonprintable
and the printable. Printable characters are things like
characters (upper and lower case), numbers and punctuation. Nonprintable
codes are for control, and do things like make a carriagereturn,
ring the terminal bell or the special NULL code which
represents nothing at all.

### 16, 32 and 64 bit computers

32 bit computers means that their internal registers are 32-bits (or 4-bytes) wide.

### Kilo, Mega and Giga Bytes

SI Unit 1kilo = 1000 and 1000 in binary is 1111101000 which is 10 bits. So since &2^10 = 1024& is also 10 bits then we can represent 1024 as a kilobyte.

### Conversion

Divide by 2.

### Boolean Operations

Boolean operations simply take a particular input and produce a
particular output following a rule.

![image](https://github.com/Sambor2511/computer-science-self-taught/assets/76769524/6d522051-6f9c-4889-80e7-138e594d6d30)
![image](https://github.com/Sambor2511/computer-science-self-taught/assets/76769524/83711885-42f4-4a07-b803-176f24a4709e)
![image](https://github.com/Sambor2511/computer-science-self-taught/assets/76769524/44a9fec6-e5ef-42d1-9111-3d18d77cf1c3)
![image](https://github.com/Sambor2511/computer-science-self-taught/assets/76769524/33a43dff-1f9e-4b3b-8bd0-f354098f3a80)

Half adder is a type of circuit made up from boolean operations that can add bits together (it
is called a half adder because it does not handle carry bits). Put more
half adders together, and you will start to build something that can
add together long binary numbers. Add some external memory, and
you have a computer.

Electronically, the boolean operations are implemented in gates made
by transistors.

### Hexadecimal

Hexadecimal refers to a base 16 number system. Hexadecimal uses the standard base 10 numerals, but adds A B C D E F which refer to 10 11 12 13 14 15.

Traditionally, any time you see a number prefixed by 0x this will
denote a hexadecimal number.

![image](https://github.com/Sambor2511/computer-science-self-taught/assets/76769524/eaf62799-2844-4455-9e20-2af70abc065c)

### Masking and Flags

Remember each bit represents two states, so if we know a variable
only has, say, 16 possible states it can be represented by 4 bits (i.e.
24=16 unique values). But the smallest type we can declare in C is 8
bits (a char ), so we can either waste four bits, or find some way to
use those left over bits

![image](https://github.com/Sambor2511/computer-science-self-taught/assets/76769524/6dd54c06-860a-4b53-b860-dde3175941ed)

### C Standards

Officially this standard is known as ISO/IEC 9899:1999(E), but is
more commonly referred to by its shortened name C99.

### GNU C

The GNU C Compiler, more commonly referred to as gcc, almost
completely implements the C99 standard.

### Types

In a typed language, such as C, every
variable must be declared with a type.

![image](https://github.com/Sambor2511/computer-science-self-taught/assets/76769524/3bcd8424-aac0-47f5-b0bf-034af3be1cbd)

Each architecture and operating system conforms to an Application Binary Interface or ABI. The ABI for a system fills in the details between the C standard and the requirements of the underlying hardware and operating system. An ABI is written for a specific processor and operating system combination.

### Type qualifiers

const means that a variable will never be modified from its original value and volatile suggests to the compiler that this value might change outside program execution flow so the compiler must be careful not to re-order access to it in any way.
signed and unsigned are probably the two most important qualifiers; and they say if a variable can take on a negative value or not.
Qualifiers are all intended to pass extra information about how the variable will be used to the compiler.

### Number Representation

Binary can be negative or positive.

### Standard Types

uint8_t is an unsigned integer exactly 8 bits wide. Many other types are defined.

### Sign Bit

MSB on the leftmost of the bits.

### One's Complement

One's complement simply applies the not operation to the positive number to represent the negative number. One complement have 2 representation of 0 which is 0000 and 1111.

### Two's Complement

Two's complement have only 1 representation of 0 which is 0000. Two's complement work by inverting all the bits at then adding one to the LSB.

### Sign Extension

Sign-extension is a technique used in computer arithmetic to correctly extend the sign of a binary number when increasing the number of bits used to represent that number. This is particularly important when dealing with signed integers in two's complement representation. 4-bit 1010 (-6 in decimal) extended to 8-bit: 1111 1010.

### Floating Point

In scientific notation the value 123.45 might commonly be represented as 1.2345x102. We call 1.2345 the mantissa or significand, 10 is the radix and 2 is the exponent.

In the IEEE floating point model, we break up the available bits to represent the sign, mantissa and exponent of a decimal number. A decimal number is represented by sign × significand × 2^exponent.

- For single precision (32-bit), the exponent field is 8 bits, so the bias is $2^{7} - 1 = 127$.

Scroll down for the English version

VHDL_GEN
vhdl_gen é um gerador de VHDL simples que utiliza um arquivo .txt como entrada e gera um design completo em VHDL, ainda não foi testado em windows mas deve funcionar.

UTILIZACAO
chmod +x o arquivo vhdl_gen.py e execute-o "./vhdl_gen.py path_to_.txt"

Um arquivo .vhd vai ser criado com todas as entradas, saidas e os sinais internos declarados com base no arquivo .txt, a biblioteca padrão 1164 e a numeric_std serão utilizadas.

Tambem sera criada uma maquina de estados do tipo em que se separa a parte combinacional e sequencial do design.

ARQUIVO DE ENTRADA
o arquivo .txt deve seguir este template
ENTIDADE
NomeES-entrada/saida-numeroDeBits
#
NomeSINAL-numeroDeBits

EXEMPLO DE ARQUIVO DE ENTRADA
pisca_led
sysclk-entrada-1
reset_n-entrada-1
enable-entrada-1
leds-saida-16
#
timer-16
leds-16


VHDL_GEN
vhdl_gen is currently a simple VHDL generator that uses a .txt file as input and generates a complete VHDL design. It's not tested under Windows environment but should work. 
Also there is only a Portuguese version of the code currently available.

USAGE
chmod +x the vhdl_gen.py file and execute it "./vhdl_gen.py path_to_.txt"

A .vhd file will be created with all the inputs and outputs and internal signals declared in the .txt file, the standard 1164 library and the numeric_std library are going to be used.

Also a state machine is going to be used with the two state machine style, one with the registers (sequential logic) and another one with the combinational logic.

INPUT FILE
The .txt file MUST have the following template
ENTITY
IO_name-entrada/saida-number_of_bits
#
signal_name-number_of_bits

EXAMPLE OF INPUT FILE
blink_led
sysclk-entrada-1
reset_n-entrada-1
enable-entrada-1
leds-saida-16
#
timer-16
leds-16

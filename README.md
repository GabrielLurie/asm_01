.486
.model flat, stdcall
option casemap :none

include \masm32\include\kernel32.inc
includelib \masm32\lib\kernel32.lib
include \masm32\include\masm32.inc
includelib \masm32\lib\masm32.lib

.data

.code
_start:
	mov eax, 0
	mov ecx ,100
	
lp:
	add eax, ecx
	loop lp
	mov x, eax
	
end_program:
	mov eax, 0
	push eax
	call ExitProcess

end _start

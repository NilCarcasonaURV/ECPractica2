# Pràctica 2 Estructura de computadors
## Objectiu de la pràctica
Aquesta pràctica consisteix en el disseny d'un processador mononucli amb ISA MIPS bàsic. 
## Restriccions
1. Els retards de totes les portes lògiques no se'n poden modificar
2. La unitat de control ha de ser microprogramada
3. Només hi pot haver un sol rellotge sense modificar l'ona (el mateix temps d'alt i baix)
## Estructura de referència
1. Hi ha dues memòries, una pel codi i l'altre per les dades
2. S'ha de fer amb tkgate 1.8
## Requisits
### Operacions
1. slt: set if lower than
2. beq: branch if equal
3. add
4. sw: store
5. lw: load
6. j: jump
7. xorni: xorni $a, $b, inm16 a = b ^ (~ext32(inm16)); 
8. paddm: paddm $a, label($b) si a > 0: a = a + Memòria[b + label]
9. and
10. or
11. sub
### TTY
TTY funcional tant entrada com sortida.
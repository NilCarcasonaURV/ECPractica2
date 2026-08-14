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
## Configuració
### Unitat de control
inst.mem -> memòria de dalt
funct.mem -> memòria de baix
### Processador
codi.mem -> memòria de l'esquerra
mem_principal.mem -> memòria de la dreta
### Scripts d'automatitzacions (.gss)
Hi ha proves automatitzades que carga tots els .mem a on toca
## Mòduls personalitzats
- add: Calculant els retards amb Excel combinant CPA, CLA, CSA
- OPTOR i OPTAND: Són operacions que afecten a tota una paraula on he optimitzat la mida de les portes lògiques segons el retard afegit per entrada
- Retard172: Com no puc modificar els retards de portes lògiques ni el temps de la part alta ni baixa del rellotge he creat aquest retard per fer un rellotge virtual desfasat del real i així compactar el càlcul de l'adreça a l'hora d'escriure i llegir de memòria. 
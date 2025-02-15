<!-- # [ zrfisaac ] -->

<!-- # [ about ] -->
<!-- # - author : Isaac Caires -->
<!-- # . - email : zrfisaac@gmail.com -->
<!-- # . - site : zrfisaac.github.io -->
<!-- # - version : zrfisaac.wiki.es.delphi : 0.0.1 -->

<!-- # [ markdown ] -->

<!-- # - : http://blong.com/Conferences/DCon2001/Debugging/Debugging.htm -->

<!-- # [ markdown ] -->
# Delphi

## Descripción
Delphi es un lenguaje de programación orientado a objetos de alto nivel y un entorno de desarrollo integrado (IDE) para el desarrollo rápido de aplicaciones (RAD). Desarrollado originalmente por Borland y ahora mantenido por Embarcadero, Delphi se utiliza principalmente para crear aplicaciones para Windows, macOS, iOS, Android y Linux. Se basa en Object Pascal y cuenta con un potente marco de componentes visuales (VCL y FireMonkey) que permite a los desarrolladores crear aplicaciones con una interfaz gráfica de usuario enriquecida. Delphi es conocido por su sólido soporte de bases de datos, rendimiento y facilidad de uso, lo que lo hace popular para aplicaciones empresariales y de negocios.

---

## Índice
- [Depuración](#depuración)
  - [CPU](#cpu)
    - [Registros de la CPU](#registros-de-la-cpu)
    - [Flags de la CPU](#flags-de-la-cpu)
    - [Instrucciones de ensamblaje de la CPU](#instrucciones-de-ensamblaje-de-la-cpu)
- Descargas
  - CodeGear :
    [`2007`](https://altd.codegear.com/download/radstudio2007/CodeGearRADStudio2007_Dec2007.iso)
  - Embarcadero :
    [`12.2 Athens`](https://altd.embarcadero.com/download/radstudio/12.0/RADStudio_12_2_i_0329_C2CC.iso)
    [`11.3 Alexandria`](https://altd.embarcadero.com/download/radstudio/11.0/RADStudio_11_3_61_3236a.iso)
    [`10.4.2 Sydney`](https://altd.embarcadero.com/download/radstudio/10.4/RADStudio-1042-4203.iso)
    [`10.3.3 Rio`](https://altd.embarcadero.com/download/radstudio/10.3/delphicbuilder10_3_3_7899_nt.iso)
    [`10.2.3 Tokyo`](https://altd.embarcadero.com/download/radstudio/10.2/delphicbuilder10_2_3_2631.iso)
    [`10.1 Berlin`](https://altd.embarcadero.com/download/radstudio/10.1/delphicbuilder10_1_upd1.iso)
    [`10 Seattle`](https://altd.embarcadero.com/download/radstudio/10/delphicbuilder10___upd1.iso)
    [`XE8`](http://altd.embarcadero.com/download/radstudio/xe8/delphicbuilder_xe8_upd1_subscription.iso)
    [`XE7`](https://altd.embarcadero.com/download/radstudio/xe7/delphicbuilder_xe7_upd1_win.iso)
    [`XE6`](https://altd.embarcadero.com/download/radstudio/xe6/delphicbuilder_xe6_upd1_win.iso)
    [`XE5`](https://altd.embarcadero.com/download/radstudio/xe5/delphicbuilder_xe5_upd2_win.iso)
    [`XE4`](https://altd.embarcadero.com/download/radstudio/xe4/delphicbuilder_xe4_upd1_win.iso)
    [`XE2`](https://altd.embarcadero.com/download/radstudio/xe2/delphicbuilder_xe2_4429_win_dl.iso)
    [`XE`](https://altd.embarcadero.com/download/RADStudioXE/delphicbuilder_xe_3953B_win.iso)
    [`2010`](https://altd.embarcadero.com/download/RADStudio2010/delphicbuilder_2010_3615_win.iso)
    [`2009`](https://altd.embarcadero.com/download/Delphi_C++Builder2009/Delphi_C++Builder2009_ISO_June2009.iso)
    [`7`](https://altd.embarcadero.com/download/delphi/d7/english/ent/delphi_7_ent_en.iso)
  - WinWorld :
    [`7`](https://winworldpc.com/product/delphi/70)
    [`6`](https://winworldpc.com/product/delphi/60)
    [`4`](https://winworldpc.com/product/delphi/4x)
    [`3`](https://winworldpc.com/product/delphi/3x)
    [`2`](https://winworldpc.com/product/delphi/2x)
    [`1`](https://winworldpc.com/product/delphi/1x)
- [Versión](#versión)

---

## [Depuración](#índice)

### [CPU](#índice)

#### [Registros de la CPU](#índice)

| Registro | Nombre del registro | Tamaño | Comentarios |
|---|---|---|---|
| EAX | Acumulador extendido | 32 bits | Registro de propósito general |
| EBX | Base extendida | 32 bits | Registro de propósito general |
| ECX | Contador extendido | 32 bits | Registro de propósito general |
| EDX | Datos extendidos | 32 bits | Registro de propósito general |
| ESI | Indicador de origen extendido | 32 bits | Registro de propósito general |
| EDI | Indicador de destino extendido | 32 bits | Registro de propósito general |
| EBP | Puntero de base extendido | 32 bits | Registro de propósito general |
| ESP | Puntero de pila extendido | 32 bits | Registro de propósito general |
| EIP | Puntero de instrucción extendido | 32 bits | Registro de estado/control |
| EFL | Flags extendidos | 32 bits | Registro de estado/control |
| CS | Segmento de código | 16 bits | Para contener un selector de segmento |
| DS | Segmento de datos | 16 bits | Para contener un selector de segmento |
| SS | Segmento de pila | 16 bits | Para contener un selector de segmento |
| ES | Segmento extra | 16 bits | Para contener un selector de segmento |
| FS | Otro segmento extra | 16 bits | Para contener un selector de segmento |
| GS | Otro segmento extra | 16 bits | Para contener un selector de segmento |
| AX | Acumulador | 16 bits | Palabra baja de EAX |
| AH | Acumulador alto | 8 bits | Byte alto de AX |
| AL | Acumulador bajo | 8 bits | Byte bajo de AX |
| BX | Base | 16 bits | Palabra baja de EBX |
| BH | Base alto | 8 bits | Byte alto de BX |
| BL | Base bajo | 8 bits | Byte bajo de BX |
| CX | Contador | 16 bits | Palabra baja de ECX |
| CH | Contador alto | 8 bits | Byte alto de CX |
| CL | Contador bajo | 8 bits | Byte bajo de CX |
| DX | Datos | 16 bits | Palabra baja de EDX |
| DH | Datos altos | 8 bits | Byte alto de DX |
| DL | Datos bajos | 8 bits | Byte bajo de DX |

#### [Flags de la CPU](#índice)

| Valor | Bit(s) del registro EFL | Nombre del flag/bit | Tipo de flag |
|---|---|---|---|
| CF | 0 | Flag de acarreo | Estado |
| PF | 2 | Flag de paridad | Estado |
| AF | 4 | Flag de ajuste | Estado |
| ZF | 6 | Flag de cero | Estado |
| SF | 7 | Flag de signo | Estado |
| TF | 8 | Flag de trampa | Sistema |
| IF | 9 | Flag de interrupción | Sistema |
| DF | 10 | Flag de dirección | Control |
| OF | 11 | Flag de desbordamiento | Estado |
| IO | 12 y 13 | Campo de nivel de privilegio de E/S | Sistema |
| NF | 14 | Flag de tarea anidada | Sistema |
| RF | 16 | Flag de reanudación | Sistema |
| VM | 17 | Flag de modo virtual 8086 | Sistema |
| AC | 18 | Flag de verificación de alineación | Sistema |
| VF | 19 | Flag de interrupción virtual | Sistema |

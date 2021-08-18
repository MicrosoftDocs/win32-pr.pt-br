---
description: No MOF, os números são dígitos que descrevem valores numéricos. O MOF fornece uma variedade de tipos de dados que são convertidos em automação e também permite que esses números estejam em formatos diferentes. A tabela a seguir lista os valores numéricos que o MOF suporta.
ms.assetid: 7a18ed36-9c12-42be-a4ee-0f6c0097b130
ms.tgt_platform: multiple
title: Números (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f3441988bb91d4bb2f3742016f01cb69996e3dcb55081a6723d851ed74cc1cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555126"
---
# <a name="numbers-wmi"></a>Números (WMI)

No MOF, os números são dígitos que descrevem valores numéricos. O MOF fornece uma variedade de tipos de dados que são convertidos em automação e também permite que esses números estejam em formatos diferentes. A tabela a seguir lista os valores numéricos que o MOF suporta.



| Tipo de dados  | Tipo de automação | Descrição                                                                                                                                                             |
|------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **sint8**  | **\_I2 VT**      | Inteiro de 8 bits assinado.<br/>                                                                                                                                        |
| **sint16** | **\_I2 VT**      | Inteiro de 16 bits assinado.<br/>                                                                                                                                       |
| **sint32** | \_I4 VT          | Inteiro de 32 bits assinado.<br/>                                                                                                                                       |
| **sint64** | **VT \_ BSTR**    | Número inteiro de 64 bits assinado no formulário de cadeia de caracteres. Esse tipo segue o formato hexadecimal ou decimal de acordo com as regras C de American National Standards Institute (ANSI).<br/> |
| **real32** | **VT \_ R4**      | valor de ponto flutuante de 4 bytes que segue o padrão IEEE (Institute of Electrical and Electronics Engineers, Inc.).<br/>                                        |
| **real64** | **R8 de VT \_**      | valor de ponto flutuante de 8 bytes que segue o padrão IEEE.<br/>                                                                                                  |
| **uint8**  | **\_UI1 VT**     | Inteiro de 8 bits não assinado.<br/>                                                                                                                                      |
| **UInt16** | **\_I4 VT**      | Inteiro de 16 bits sem sinal.<br/>                                                                                                                                     |
| **uint32** | **\_I4 VT**      | Inteiro de 32 bits sem sinal.<br/>                                                                                                                                     |
| **uint64** | **VT \_ BSTR**    | Inteiro de 64 bits sem sinal no formulário de cadeia de caracteres. Esse tipo segue o formato hexadecimal ou decimal de acordo com as regras ANSI C.<br/>                                           |



 

Embora seja flexível, o código MOF encontra algumas alterações ao lidar com a automação:

-   Você deve codificar inteiros de 64 bits como cadeias de caracteres.

    A automação não dá suporte a um tipo integral de 64 bits.

-   Os tipos de automação nem sempre correspondem em tamanho de bits a tipos de dados MOF.

    Por exemplo, a automação usa VT \_ i4 para retornar um valor de 16 bits não assinado. Essa discrepância existe devido a problemas de extensão de conexão. Se a automação usou VT \_ i2 em vez de VT \_ I4, 65.536 pareceria ser o valor 1, causando problemas de tipo e intervalo. Da mesma forma, a automação representa o tipo **UInt32** como VT \_ i4 porque não existe nenhum tipo inteiro maior para conter **UInt32**.

-   Você não precisa alterar nenhuma representação para tipos de numeral de 8 bits.

    A automação dá suporte \_ a VT UI1, um tipo de 8 bits não assinado.

O MOF dá suporte a constantes longas. Você declara uma constante longa usando uma série simples de dígitos com um sinal negativo opcional. Uma constante longa não pode exceder o tamanho da variável que está declarada para contê-la. Alguns exemplos de constantes longas são 1000 e 12310.

O MOF também dá suporte a formatos numéricos alternativos. A tabela a seguir lista os caracteres especiais que você deve usar para descrever as constantes hexadecimal, binária e octal.



| Constante               | Caractere especial     | Exemplo                   |
|------------------------|-----------------------|---------------------------|
| Decimal<br/>     | Nenhum<br/>       | Val = 65<br/>       |
| Hexadecimal<br/> | prefixo 0x<br/>  | Val = 0x41<br/>     |
| Octais<br/>       | 0 à esquerda<br/>  | Val = 0101<br/>     |
| Binário<br/>      | B à direita<br/> | Val = 1000001B<br/> |



 

Você pode usar uma constante de ponto flutuante para representar notação científica, bem como frações, conforme mostrado a seguir:

``` syntax
3.14
-3.14
-1.2778E+02
```

O WMI considera constantes de ponto flutuante como tipos de **\_ R8 de VT** para automação.

O exemplo a seguir descreve as declarações de classe e de instância que ilustram como usar cada um dos tipos de dados numéricos para definir propriedades:

``` syntax
Class NumericDataClass
 {
   [key] uint8 Duint8;
   SInt8       Dchar;
   UInt16      Dtword;
   Sint16      Dinst16;
   UInt32      Ddword;
   Sint32      Dinst1;
   Sint32      Dinst2;
   Sint32      Dinst3;
   Sint32      Dinst4;
   Sint32      Dinst5;
   Real32      Dfloat;
   Real64      Ddouble1;
   Real64      Ddouble2;
 };

instance of NumericDataClass
 {
   Duint8   =  122;
   Dchar    = -128;
   Dtword   =  30;
   Dinst16  = -1445;
   Ddword   =  6987777;
   Dinst1   = -455589;
   Dinst2   =  23;
   Dinst3   =  03;         // Base 8
   Dinst4   =  0xFe;       // Base 16
   Dinst5   =  11b;        // Base 2
   Dfloat   =  3.1478;
   Ddouble1 =  99987.3654;
   Ddouble2 =  2.3e-2;
 };
```

 

 





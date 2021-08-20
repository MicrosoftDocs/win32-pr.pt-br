---
title: Gramática
description: As instruções HLSL são construídas usando as regras a seguir para gramática.
ms.assetid: 683248e9-6fc7-451a-906b-6e0aab1b0c8c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 86549f441752e72fd11a741a061fcaf839eca0140f4766b0932094d74dc78085
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855066"
---
# <a name="grammar"></a>Gramática

As instruções HLSL são construídas usando as regras a seguir para gramática.

-   [Espaço em branco](#whitespace)
-   [Números de ponto flutuante](#floating-point-numbers)
-   [Números inteiros](#integer-numbers)
-   [Characters](#characters)
-   [Cadeias de caracteres](#strings)
-   [Identificadores](#identifiers)
-   [Operadores](#operators)
-   [Tópicos relacionados](#related-topics)

## <a name="whitespace"></a>Espaço em branco

Os caracteres a seguir são reconhecidos como espaços em branco.

- SPACE
- TAB
- MERCADO
- Comentários de estilo C (/ \* \* /)
- Comentários de estilo C++ (//)

## <a name="floating-point-numbers"></a>Números de ponto flutuante

Os números de ponto flutuante são representados em HLSL da seguinte maneira:

-   fração fracionária-parte do expoente (opt) de sufixo flutuante (opcional)

    expoente de sequência de dígitos – sufixo de parte flutuante (opt)

-   fração fracionária:

    sequência de dígitos (opt). digit-sequence

    sequência de dígitos.

-   expoente – parte:

    sequência de dígitos de sinal e (opt)

    Sequência de dígitos de sinal E (opt)

-   sign : one of

    \+ -

-   sequência de dígitos:

    {1&gt;digit&lt;1}

    digit-sequence digit

-   floating-suffix : one of

    h H f F l

    Use o sufixo "L" para especificar um literal de ponto flutuante de precisão de 64 bits completo. Um literal de float de 32 bits é o padrão.

    Por exemplo, o compilador reconhece o valor literal a seguir como um literal de ponto flutuante de precisão de 32 bits e ignora os bits inferiores:

    ```
    double x = -0.6473313946860445;
    ```

    

    O compilador reconhece o seguinte valor literal como um literal de ponto flutuante de precisão de 64 bits:

    ```
    double x = -0.6473313946860445L;
    ```

    

## <a name="integer-numbers"></a>Números inteiros

Os números inteiros são representados em HLSL da seguinte maneira:

-   Integer-inteiro constante-sufixo (opt)
-   inteiro-constante: uma das

    \# (número decimal)

    0 \# (número octal)

    0x \# (número hexadecimal)

-   o sufixo inteiro pode ser qualquer um dos seguintes:

    u U l l

## <a name="characters"></a>Characters

Os caracteres são representados em HLSL da seguinte maneira:



| Caractere                                          | Descrição                                                                |
|-------------------------------------------|-----------------------------------------------------------------|
| 'c'                                       | espaço                                                     |
| ' \\ a ' ' \\ b ' ' \\ f ' ' \\ b ' ' \\ r ' ' \\ t ' ' \\ v ' | ignora                                                       |
| '\\\#\#\#'                                | (escape octal, cada \# um é um dígito octal)                       |
| ' \\ x \# '                                   | (escape Hex, \# é número hexadecimal, qualquer número de dígitos)            |
| ' \\ C'                                     | (c é outro caractere, incluindo barra invertida e aspas) |



 

Não há suporte para escapes em expressões de pré-processador.

## <a name="strings"></a>Cadeias de caracteres

As cadeias de caracteres são representadas em HLSL da seguinte maneira:

"s" (s é qualquer cadeia de caracteres com escapes).

## <a name="identifiers"></a>Identificadores

Os identificadores são representados em HLSL da seguinte maneira:


```
    [A-Za-z_][A-Za-z0-9_]*
```



## <a name="operators"></a>Operadores


```
##, #@, ++, --, &, &, &, ||, ==, ::, <<, <<=, >>, >>=, ..., 
<=, >=, !=, *=, /=, +=, -=, %=, &=, |=, ^=, ->
```



Também qualquer outro caractere único que não corresponde a outra regra.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Apêndice (DirectX HLSL)](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 





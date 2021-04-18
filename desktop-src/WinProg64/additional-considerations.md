---
title: Considerações adicionais
description: Ao portar seu código, considere os pontos a seguir.
ms.assetid: 2d649a09-b593-477a-9b4f-d2404784f4b0
keywords:
- Dicas de portamento-programação do Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7607685f4b4ba04b86da276c38090a48ce0fead
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105814028"
---
# <a name="additional-considerations"></a>Considerações adicionais

Ao portar seu código, considere os seguintes pontos:

- A suposição a seguir não é mais válida:

   ```syntax
   #ifdef _WIN32 // Win32 code
      ...
   #else         // Win16 code
      ...
   #endif
   ```

   No entanto, o compilador de 64 bits define o \_ Win32 para compatibilidade com versões anteriores.

- A suposição a seguir não é mais válida:

   ```syntax
   #ifdef _WIN16 // Win16 code
      ...
   #else         // Win32 code
      ...
   #endif
   ```

   Nesse caso, a cláusula else pode representar \_ Win32 ou \_ Win64.

- Tenha cuidado com o alinhamento do tipo de dados. A macro de **\_ alinhamento de tipo** retorna os requisitos de alinhamento de um tipo de dados. Por exemplo: `TYPE_ALIGNMENT( KFLOATING_SAVE )` = = 4 em x86, 8 no processador Intel Itanium `TYPE_ALIGNMENT( UCHAR )` = = 1 em qualquer lugar

    Por exemplo, o código do kernel que tem a seguinte aparência:

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, sizeof(ULONG) );
    ```

    Provavelmente deve ser alterado para:

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, TYPE_ALIGNMENT(IOCTL_STRUC) );
    ```

    As correções automáticas de exceções de alinhamento do modo kernel estão desabilitadas para sistemas Intel Itanium.

- Tenha cuidado com não operações. Considere o seguinte:

    ```syntax
    UINT_PTR a; 
    ULONG b;
    a = a & ~(b - 1);
    ```

    O problema é que ~ (b – 1) produz "0x0000 0000 xxxx xxxx" e não "0xFFFF FFFF xxxx xxxx". O compilador não detectará isso. Para corrigir isso, altere o código da seguinte maneira:

    ```syntax
    a = a & ~((UINT_PTR)b - 1);
    ```

- Tenha cuidado ao executar operações sem assinatura e assinadas. Considere o seguinte:

    ```syntax
    LONG a;
    ULONG b;
    LONG c;

    a = -10;
    b = 2;
    c = a / b;
    ```

    O resultado é inesperadamente grande. A regra é que se um dos operandos não estiver assinado, o resultado será não assinado. No exemplo anterior, um é convertido em um valor não assinado, dividido por b e o resultado armazenado em c. A conversão não envolve nenhuma manipulação numérica.

    Como outro exemplo, considere o seguinte:

    ```syntax
    ULONG x;
    LONG y;
    LONG *pVar1;
    LONG *pVar2;

    pVar2 = pVar1 + y * (x - 1);
    ```

    O problema ocorre porque x não é assinado, o que torna a expressão inteira não assinada. Isso funciona bem, a menos que y seja negativo. Nesse caso, y é convertido em um valor não assinado, a expressão é avaliada usando a precisão de 32 bits, dimensionada e adicionada a pVar1. Um número negativo sem sinal de 32 bits se torna um número positivo de 64 bits grande, que fornece o resultado incorreto. Para corrigir esse problema, declare x como um valor assinado ou explicitamente conversão-o ao **longo** da expressão.

- Tenha cuidado ao fazer alocações de tamanho gradativamente. Por exemplo:

    ```syntax
    struct xx {
       DWORD NumberOfPointers;
       PVOID Pointers[100];
    };
    ```

    O código a seguir está errado porque o compilador irá preencher a estrutura com um adicional de 4 bytes para fazer o alinhamento de 8 bytes:

    ```syntax
    malloc(sizeof(DWORD) + 100*sizeof(PVOID));
    ```

    O código a seguir está correto:

    ```syntax
    malloc(offsetof(struct xx, Pointers) + 100*sizeof(PVOID));
    ```

- Não passe `(HANDLE)0xFFFFFFFF` para funções como [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga). Em vez disso, use um **\_ \_ valor de identificador inválido**.
- Use os especificadores de formato apropriados ao imprimir uma cadeia de caracteres. Use% p para imprimir ponteiros em hexadecimal. Essa é a melhor opção para imprimir ponteiros. Microsoft Visual C++ dá suporte a% I para imprimir dados polimórficos. Visual C++ também dá suporte a% I64 para imprimir valores que são de 64 bits.

 

 
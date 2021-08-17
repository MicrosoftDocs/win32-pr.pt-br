---
title: Regras para vários pipes
description: Regras para vários pipes em uma única chamada em RPC (Chamada de Procedimento Remoto).
ms.assetid: 1d0b2aed-27cc-4e74-9307-ada86bda4596
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1fd2de7a44f63d5c943f1d6526ee328bbae3e63c99bac118ec843ad266d1f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925973"
---
# <a name="rules-for-multiple-pipes"></a>Regras para vários pipes

Você pode combinar os parâmetros de pipe de saída e de saída em qualquer combinação em uma única chamada, mas deve processar os pipes em uma ordem específica, conforme mostrado no seguinte exemplo de \[ [](/windows/desktop/Midl/in) \] \[ [](/windows/desktop/Midl/out-idl) \] \[  \] pseudocódigo:

> [!Note]  
> Não há mais suporte para esse recurso no Windows Vista e em plataformas posteriores.

 

-   Obter os dados de cada pipe de entrada, começando com o primeiro parâmetro (mais à esquerda) e continuando na ordem, esvaziando cada pipe antes de começar a \[  \] processar o próximo.
-   Depois que cada pipe de entrada for completamente processado, envie os dados para os pipes de saída, novamente começando com o primeiro parâmetro out e continuando na ordem, preenchendo cada pipe antes de começar a processar o \[  \] próximo.

``` syntax
//in .IDL file:
void InOutUCharPipe( [in,out] UCHAR_PIPE *uchar_pipe_1, 
                     [out] UCHAR_PIPE * uchar_pipe_2, 
                     [in] UCHAR_PIPE uchar_pipe_3);
 
//remote procedure:
void InOutUCharPipe( UCHAR_PIPE *param1,
                     UCHAR_PIPE *param2,
                     UCHAR_PIPE  param3)
{
    while(!END_OF_PIPE1)
    {
        param1->pull (. . .);
        . . .
    };

    while(!END_OF_PIPE3)
    {
        param3.pull (. . .);
        . . .
    };

    while(!END_OF_PIPE1)
    {
        param1->push (. . .);
        . . .
    };

    while(!END_OF_PIPE2)
    {
        param2->push(. . .);
        . . .
    };
} //end InOutUCharPipe
```

 

 
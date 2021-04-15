---
title: Regras para vários pipes
description: Regras para vários pipes em uma única chamada na RPC (chamada de procedimento remoto).
ms.assetid: 1d0b2aed-27cc-4e74-9307-ada86bda4596
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d804c132d7fc859906f065e4c9dc39dd3159519
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454257"
---
# <a name="rules-for-multiple-pipes"></a><span data-ttu-id="9fcf5-103">Regras para vários pipes</span><span class="sxs-lookup"><span data-stu-id="9fcf5-103">Rules for Multiple Pipes</span></span>

<span data-ttu-id="9fcf5-104">Você pode combinar \[ parâmetros [**de pipe de entrada**](/windows/desktop/Midl/in), \] \[ [**saída**](/windows/desktop/Midl/out-idl) \] e \[ **saída** em \] qualquer combinação em uma única chamada, mas você deve processar os pipes em uma ordem específica, conforme mostrado no exemplo de pseudocódigo a seguir:</span><span class="sxs-lookup"><span data-stu-id="9fcf5-104">You can combine \[[**in**](/windows/desktop/Midl/in)\], \[[**out**](/windows/desktop/Midl/out-idl)\], and \[**in, out**\] pipe parameters in any combination in a single call, but you must process the pipes in a specific order, as shown in the following pseudocode example:</span></span>

> [!Note]  
> <span data-ttu-id="9fcf5-105">Não há mais suporte para esse recurso no Windows Vista e em plataformas posteriores.</span><span class="sxs-lookup"><span data-stu-id="9fcf5-105">This feature is no longer supported in Windows Vista and later platforms.</span></span>

 

-   <span data-ttu-id="9fcf5-106">Obtenha os dados de cada pipe de entrada, começando pelo primeiro (mais à esquerda) \[ **no** \] parâmetro e continuando em ordem, esgotando cada pipe antes de começar a processar o próximo.</span><span class="sxs-lookup"><span data-stu-id="9fcf5-106">Get the data from every input pipe, starting with the first (leftmost) \[**in**\] parameter, and continuing in order, draining each pipe before beginning to process the next.</span></span>
-   <span data-ttu-id="9fcf5-107">Depois que cada pipe de entrada tiver sido completamente processado, envie os dados para os pipes de saída, começando novamente com o primeiro parâmetro de \[ **saída** \] e continuando em ordem, preenchendo cada pipe antes de começar a processar o próximo.</span><span class="sxs-lookup"><span data-stu-id="9fcf5-107">After every input pipe has been completely processed, send the data for the output pipes, again starting with the first \[**out**\] parameter, and continuing in order, filling each pipe before beginning to process the next.</span></span>

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

 

 
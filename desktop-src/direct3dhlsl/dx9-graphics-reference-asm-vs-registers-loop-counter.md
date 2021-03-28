---
title: Registro de contador de loop (referência de HLSL VS)
description: O único registro nesse banco é o registro do contador de loops atual (aL).
ms.assetid: b32fabf8-38d3-446c-bb80-c647d5aa028d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b12f57ba3fcfcb41aaff3827be39dbd1b6b07df1
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104365314"
---
# <a name="loop-counter-register-hlsl-vs-reference"></a><span data-ttu-id="92e22-103">Registro de contador de loop (referência de HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="92e22-103">Loop Counter Register (HLSL VS reference)</span></span>

<span data-ttu-id="92e22-104">O único registro nesse banco é o registro do contador de loops atual (aL).</span><span class="sxs-lookup"><span data-stu-id="92e22-104">The only register in this bank is the current loop counter (aL) register.</span></span> <span data-ttu-id="92e22-105">Ele é incrementado automaticamente em cada execução do [loop-vs](loop---vs.md)... bloco [ENDLOOP-vs](endloop---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="92e22-105">It automatically gets incremented in each execution of the [loop - vs](loop---vs.md)...[endloop - vs](endloop---vs.md) block.</span></span> <span data-ttu-id="92e22-106">Portanto, ele pode ser usado no bloco para endereçamento relativo, se necessário, e inválido para usá-lo fora do loop.</span><span class="sxs-lookup"><span data-stu-id="92e22-106">So it can be used in the block for relative addressing if needed and is invalid to use it outside the loop.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92e22-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="92e22-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92e22-108">Registros de sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="92e22-108">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 





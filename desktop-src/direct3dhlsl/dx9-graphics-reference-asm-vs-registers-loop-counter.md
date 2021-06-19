---
title: Registro de contador de loop (referência de HLSL VS)
description: Leia sobre o registro do contador de loop para sombreadores de vértice. O único registro nesse banco é o registro do contador de loops atual (aL).
ms.assetid: b32fabf8-38d3-446c-bb80-c647d5aa028d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8fb728420dc48c6cb67d5973085845b0eab742a2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405769"
---
# <a name="loop-counter-register-hlsl-vs-reference"></a><span data-ttu-id="62f8d-104">Registro de contador de loop (referência de HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="62f8d-104">Loop Counter Register (HLSL VS reference)</span></span>

<span data-ttu-id="62f8d-105">O único registro nesse banco é o registro do contador de loops atual (aL).</span><span class="sxs-lookup"><span data-stu-id="62f8d-105">The only register in this bank is the current loop counter (aL) register.</span></span> <span data-ttu-id="62f8d-106">Ele é incrementado automaticamente em cada execução do [loop-vs](loop---vs.md)... bloco [ENDLOOP-vs](endloop---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="62f8d-106">It automatically gets incremented in each execution of the [loop - vs](loop---vs.md)...[endloop - vs](endloop---vs.md) block.</span></span> <span data-ttu-id="62f8d-107">Portanto, ele pode ser usado no bloco para endereçamento relativo, se necessário, e inválido para usá-lo fora do loop.</span><span class="sxs-lookup"><span data-stu-id="62f8d-107">So it can be used in the block for relative addressing if needed and is invalid to use it outside the loop.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62f8d-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="62f8d-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62f8d-109">Registros de sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="62f8d-109">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 





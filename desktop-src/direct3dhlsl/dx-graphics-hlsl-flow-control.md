---
title: Controle de fluxo
description: A maioria dos hardwares foi projetada para executar o código do sombreador linha por linha, executando cada instrução HLSL uma vez.
ms.assetid: 94f22e39-8e71-424b-8ca1-bafc843f843f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 70bb7706e520818c86286947acfba6cae0759b4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292003"
---
# <a name="flow-control"></a><span data-ttu-id="06592-103">Controle de fluxo</span><span class="sxs-lookup"><span data-stu-id="06592-103">Flow Control</span></span>

<span data-ttu-id="06592-104">A maioria dos hardwares foi projetada para executar o código do sombreador linha por linha, executando cada instrução HLSL uma vez.</span><span class="sxs-lookup"><span data-stu-id="06592-104">Most hardware is designed to run shader code line by line, executing each HLSL statement once.</span></span> <span data-ttu-id="06592-105">Uma instrução de controle de fluxo determina em tempo de execução qual bloco de instruções HLSL executar em seguida.</span><span class="sxs-lookup"><span data-stu-id="06592-105">A flow-control statement determines at run time which block of HLSL statements to execute next.</span></span> <span data-ttu-id="06592-106">Usando uma instrução Flow-Control, um sombreador pode executar um loop por meio de um conjunto de instruções ou saltar (Branch) para uma instrução diferente daquela na próxima linha.</span><span class="sxs-lookup"><span data-stu-id="06592-106">Using a flow-control statement, a shader can loop through a set of statements, or jump (branch) to an instruction other than the one on the next line.</span></span> <span data-ttu-id="06592-107">Algumas instruções de controle de fluxo dão suporte ao controle estático que é especificado no momento da compilação; outros oferecem controle predicado, que é uma decisão por componente feita no tempo de execução, e ainda outros dão suporte a controle dinâmico, que é uma decisão feita em tempo de execução com base no conteúdo de uma variável.</span><span class="sxs-lookup"><span data-stu-id="06592-107">Some flow-control statements support static control that is specified at compile time; others offer predicated control which is a per-component decision made at runtime, and still others support dynamic control which is a decision made at run time based on the contents of a variable.</span></span>

<span data-ttu-id="06592-108">O HLSL dá suporte às seguintes instruções de controle de fluxo.</span><span class="sxs-lookup"><span data-stu-id="06592-108">HLSL supports the following flow-control statements.</span></span>

-   [<span data-ttu-id="06592-109">break</span><span class="sxs-lookup"><span data-stu-id="06592-109">break</span></span>](dx-graphics-hlsl-break.md)
-   [<span data-ttu-id="06592-110">continua</span><span class="sxs-lookup"><span data-stu-id="06592-110">continue</span></span>](dx-graphics-hlsl-continue.md)
-   [<span data-ttu-id="06592-111">carte</span><span class="sxs-lookup"><span data-stu-id="06592-111">discard</span></span>](dx-graphics-hlsl-discard.md)
-   [<span data-ttu-id="06592-112">do</span><span class="sxs-lookup"><span data-stu-id="06592-112">do</span></span>](dx-graphics-hlsl-do.md)
-   [<span data-ttu-id="06592-113">for</span><span class="sxs-lookup"><span data-stu-id="06592-113">for</span></span>](dx-graphics-hlsl-for.md)
-   [<span data-ttu-id="06592-114">if</span><span class="sxs-lookup"><span data-stu-id="06592-114">if</span></span>](dx-graphics-hlsl-if.md)
-   [<span data-ttu-id="06592-115">switch</span><span class="sxs-lookup"><span data-stu-id="06592-115">switch</span></span>](dx-graphics-hlsl-switch.md)
-   [<span data-ttu-id="06592-116">mesmo</span><span class="sxs-lookup"><span data-stu-id="06592-116">while</span></span>](dx-graphics-hlsl-while.md)

## <a name="related-topics"></a><span data-ttu-id="06592-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="06592-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06592-118">Sintaxe de linguagem (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="06592-118">Language Syntax (DirectX HLSL)</span></span>](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 





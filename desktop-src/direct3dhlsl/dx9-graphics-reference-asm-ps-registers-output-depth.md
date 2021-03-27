---
title: Registro de profundidade de saída
description: O oDepth (registro de profundidade de saída) do sombreador de pixel é um registro escalar somente gravação com o intervalo \ 0.. 1 \ que retorna um novo valor de profundidade para um teste de profundidade no buffer do estêncil de profundidade.
ms.assetid: 47b9afd9-4520-480d-b4a2-3d9a5569defb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9be825d6117cf1cc14464973146dbe176d696d25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292840"
---
# <a name="output-depth-register"></a><span data-ttu-id="8b8be-103">Registro de profundidade de saída</span><span class="sxs-lookup"><span data-stu-id="8b8be-103">Output Depth Register</span></span>

<span data-ttu-id="8b8be-104">O oDepth (registro de profundidade de saída) do sombreador de pixel é um registro escalar somente gravação com o intervalo \[ 0.. 1 \] que retorna um novo valor de profundidade para um teste de profundidade em relação ao buffer do estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="8b8be-104">The pixel shader output depth register (oDepth) is a write-only scalar register with the range \[0..1\] that returns a new depth value for a depth test against the depth-stencil buffer.</span></span>

<span data-ttu-id="8b8be-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b8be-105">Syntax</span></span>



| <span data-ttu-id="8b8be-106">oDepth</span><span class="sxs-lookup"><span data-stu-id="8b8be-106">oDepth</span></span> |
|--------|



 

<span data-ttu-id="8b8be-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="8b8be-107">Where:</span></span>



| <span data-ttu-id="8b8be-108">Name</span><span class="sxs-lookup"><span data-stu-id="8b8be-108">Name</span></span>   | <span data-ttu-id="8b8be-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="8b8be-109">Description</span></span>                                                       |
|--------|-------------------------------------------------------------------|
| <span data-ttu-id="8b8be-110">oDepth</span><span class="sxs-lookup"><span data-stu-id="8b8be-110">oDepth</span></span> | <span data-ttu-id="8b8be-111">Novo valor de profundidade para um teste de profundidade no buffer de estêncil de profundidade</span><span class="sxs-lookup"><span data-stu-id="8b8be-111">New depth value for a depth test against the depth-stencil buffer</span></span> |



 

<span data-ttu-id="8b8be-112">É importante estar ciente de que a gravação em oDepth causa a perda de qualquer algoritmo de otimização de buffer de profundidade específico do hardware (ou seja, a Z hierárquico) que acelera o desempenho do teste de profundidade.</span><span class="sxs-lookup"><span data-stu-id="8b8be-112">It is important to be aware that writing to oDepth causes the loss of any hardware-specific depth buffer optimization algorithms (i.e. hierarchical Z) which accelerate depth test performance.</span></span>

<span data-ttu-id="8b8be-113">Replicar swizzle de origem (. x \| . y \| . z \| . w) é necessário ao gravar em oDepth.</span><span class="sxs-lookup"><span data-stu-id="8b8be-113">Replicate source swizzle (.x \| .y \| .z \| .w) is required when writing to oDepth.</span></span> <span data-ttu-id="8b8be-114">Não são permitidas máscaras de gravação explícitas.</span><span class="sxs-lookup"><span data-stu-id="8b8be-114">Explicit write masks are not allowed.</span></span>

<span data-ttu-id="8b8be-115">Gravar no registro oDepth substitui o valor de profundidade interpolado (e ignora qualquer tendência de profundidade/slopescale renderstates).</span><span class="sxs-lookup"><span data-stu-id="8b8be-115">Writing to the oDepth register replaces the interpolated depth value (and ignores any depth bias/slopescale renderstates).</span></span> <span data-ttu-id="8b8be-116">Se nenhum buffer de profundidade tiver sido criado ou anexado ao dispositivo, então gravar em oDepth será ignorado.</span><span class="sxs-lookup"><span data-stu-id="8b8be-116">If no depth buffer has been created or attached to the device, then write to oDepth is ignored.</span></span>

<span data-ttu-id="8b8be-117">Se você for multiamostrar e gravar em oDepth, como o sombreador de pixel só é executado uma vez por pixel, o valor de profundidade é replicado para todos os locais de subamostras cobertos.</span><span class="sxs-lookup"><span data-stu-id="8b8be-117">If you are multisampling and write to oDepth, since the pixel shader only runs once per pixel, your depth value is replicated for all covered sub-sample locations.</span></span> <span data-ttu-id="8b8be-118">O teste de profundidade ainda acontece por exemplo, mas você não tem um valor de profundidade por amostra na comparação do sombreador de pixel como você teria se não escrever oDepth.</span><span class="sxs-lookup"><span data-stu-id="8b8be-118">The depth test still happens per-sample, but you don't have a per-sample depth value going into the comparison from the pixel shader like you would have if you didn't write oDepth.</span></span>

<span data-ttu-id="8b8be-119">Se um aplicativo tiver um conjunto de buffer w como seu buffer de profundidade, ele precisa levar isso em conta ao gravar no oDepth.</span><span class="sxs-lookup"><span data-stu-id="8b8be-119">If an application has a w-buffer set as its depth buffer, then it needs to take that into account while writing to oDepth.</span></span> <span data-ttu-id="8b8be-120">Ele potencialmente precisa enviar informações de intervalo w para o sombreador de pixel e calcular o intervalo w para dimensionar os valores w gravados em oDepth.</span><span class="sxs-lookup"><span data-stu-id="8b8be-120">It potentially needs to send w-range information to the pixel shader and compute the w-range to scale the w-values written out to oDepth.</span></span>

### <a name="ps_2_0-and-ps_2_x-restrictions"></a><span data-ttu-id="8b8be-121">\_restrições PS 2 \_ 0 e PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8b8be-121">ps\_2\_0 and ps\_2\_x Restrictions</span></span>

-   <span data-ttu-id="8b8be-122">oDepth só pode ser escrito com a instrução [Mov-PS](mov---ps.md) e só pode ser feito uma vez.</span><span class="sxs-lookup"><span data-stu-id="8b8be-122">oDepth can only be written with the [mov - ps](mov---ps.md) instruction and can only be done once.</span></span>
-   <span data-ttu-id="8b8be-123">Nenhum modificador de origem é permitido ao gravar em oDepth.</span><span class="sxs-lookup"><span data-stu-id="8b8be-123">No source modifier is allowed when writing to oDepth.</span></span>
-   <span data-ttu-id="8b8be-124">Nenhum modificador de instrução é permitido ao gravar em oDepth.</span><span class="sxs-lookup"><span data-stu-id="8b8be-124">No instruction modifier is allowed when writing to oDepth.</span></span>
-   <span data-ttu-id="8b8be-125">Não há gravação no oDepth de dentro de uma construção de controle de fluxo ou ao usar predicação.</span><span class="sxs-lookup"><span data-stu-id="8b8be-125">No writing to oDepth from within a flow control construct, or when using predication.</span></span>

### <a name="ps_3_0-restrictions"></a><span data-ttu-id="8b8be-126">Restrições do PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8b8be-126">ps\_3\_0 Restrictions</span></span>

-   <span data-ttu-id="8b8be-127">Para o PS \_ 3 \_ 0, os registros de saída OC # e OD \# podem ser gravados várias vezes.</span><span class="sxs-lookup"><span data-stu-id="8b8be-127">For ps\_3\_0, output registers oC# and oD\# can be written any number of times.</span></span> <span data-ttu-id="8b8be-128">A saída do sombreador de pixel é proveniente do conteúdo dos registros de saída no final da execução do sombreador.</span><span class="sxs-lookup"><span data-stu-id="8b8be-128">The output of the pixel shader comes from the contents of the output registers at the end of shader execution.</span></span> <span data-ttu-id="8b8be-129">Se uma gravação em um registro de saída não ocorrer, talvez devido ao controle de fluxo ou se o sombreador simplesmente não o escreveu, o destino de renderização correspondente também não será atualizado.</span><span class="sxs-lookup"><span data-stu-id="8b8be-129">If a write to an output register does not happen, perhaps due to flow control or if the shader just did not write it, the corresponding render target is also not updated.</span></span> <span data-ttu-id="8b8be-130">Se um subconjunto dos canais em um registro de saída for gravado, os valores indefinidos serão gravados nos canais restantes.</span><span class="sxs-lookup"><span data-stu-id="8b8be-130">If a subset of the channels in an output register are written, then undefined values will be written to the remaining channels.</span></span>
-   <span data-ttu-id="8b8be-131">Você pode gravar em oDepth no controle de fluxo ou predicação, desde que todos os caminhos possíveis eventualmente gravem no registro.</span><span class="sxs-lookup"><span data-stu-id="8b8be-131">You can write to oDepth within flow control or predication as long as all possible paths eventually write into the register.</span></span>
-   <span data-ttu-id="8b8be-132">Você não pode executar cálculos de gradiente (ou operações que invocam implicitamente cálculos de gradiente, como [texld-PS \_ 2 \_ 0 e up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)) dentro de instruções de controle de fluxo cujas condições de ramificação variam em uma base por primitiva (isto é: instruções de controle de fluxo dinâmico).</span><span class="sxs-lookup"><span data-stu-id="8b8be-132">You may not perform any gradient calculations (or operations that implicitly invoke gradient calculations such as [texld - ps\_2\_0 and up](texld---ps-2-0.md), [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)) inside of flow control statements whose branching conditions vary on a per-primitive basis (ie: dynamic flow control instructions).</span></span> <span data-ttu-id="8b8be-133">Instrução predicação não é considerada controle de fluxo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="8b8be-133">Instruction predication is not considered dynamic flow control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b8be-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8b8be-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b8be-135">Register</span><span class="sxs-lookup"><span data-stu-id="8b8be-135">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 





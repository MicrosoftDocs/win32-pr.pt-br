---
title: Limites de assinatura raiz
description: A assinatura raiz é a principal imobiliária e há limites e custos rígidos a serem considerados.
ms.assetid: 01121D3A-1926-4246-9C20-5E11F2E0B092
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25986da72cfcad7b714031e063341e1832d6ae68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104025"
---
# <a name="root-signature-limits"></a><span data-ttu-id="92156-103">Limites de assinatura raiz</span><span class="sxs-lookup"><span data-stu-id="92156-103">Root Signature Limits</span></span>

<span data-ttu-id="92156-104">A assinatura raiz é a principal imobiliária e há limites e custos rígidos a serem considerados.</span><span class="sxs-lookup"><span data-stu-id="92156-104">The root signature is prime real estate, and there are strict limits and costs to consider.</span></span>

-   [<span data-ttu-id="92156-105">Limites e custos de memória</span><span class="sxs-lookup"><span data-stu-id="92156-105">Memory limits and costs</span></span>](#memory-limits-and-costs)
-   [<span data-ttu-id="92156-106">Custos de desempenho</span><span class="sxs-lookup"><span data-stu-id="92156-106">Performance costs</span></span>](#performance-costs)
-   [<span data-ttu-id="92156-107">Amostras estáticas</span><span class="sxs-lookup"><span data-stu-id="92156-107">Static samplers</span></span>](#static-samplers)
-   [<span data-ttu-id="92156-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="92156-108">Related topics</span></span>](#related-topics)

## <a name="memory-limits-and-costs"></a><span data-ttu-id="92156-109">Limites e custos de memória</span><span class="sxs-lookup"><span data-stu-id="92156-109">Memory limits and costs</span></span>

<span data-ttu-id="92156-110">O tamanho máximo de uma assinatura raiz é de 64 DWORDs.</span><span class="sxs-lookup"><span data-stu-id="92156-110">The maximum size of a root signature is 64 DWORDs.</span></span>

<span data-ttu-id="92156-111">Esse tamanho máximo é escolhido para evitar o abuso da assinatura raiz como uma maneira de armazenar dados em massa.</span><span class="sxs-lookup"><span data-stu-id="92156-111">This maximum size is chosen to prevent abuse of the root signature as a way of storing bulk data.</span></span> <span data-ttu-id="92156-112">Cada entrada na assinatura raiz tem um custo em direção a este limite de 64 DWORD:</span><span class="sxs-lookup"><span data-stu-id="92156-112">Each entry in the root signature has a cost towards this 64 DWORD limit:</span></span>

-   <span data-ttu-id="92156-113">Tabelas de descritores custam 1 DWORD cada.</span><span class="sxs-lookup"><span data-stu-id="92156-113">Descriptor tables cost 1 DWORD each.</span></span>
-   <span data-ttu-id="92156-114">As constantes raiz custam 1 DWORD cada, pois são valores de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="92156-114">Root constants cost 1 DWORD each, since they are 32-bit values.</span></span>
-   <span data-ttu-id="92156-115">Os descritores de raiz (endereços virtuais de GPU de 64 bits) custam 2 DWORDs cada um.</span><span class="sxs-lookup"><span data-stu-id="92156-115">Root descriptors (64-bit GPU virtual addresses) cost 2 DWORDs each.</span></span>

<span data-ttu-id="92156-116">Os exemplos estáticos não têm nenhum custo no tamanho da assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="92156-116">Static samplers do not have any cost in the size of the root signature.</span></span>

## <a name="performance-costs"></a><span data-ttu-id="92156-117">Custos de desempenho</span><span class="sxs-lookup"><span data-stu-id="92156-117">Performance costs</span></span>

<span data-ttu-id="92156-118">O custo de desempenho (em termos de níveis de indireção) é zero para uma constante raiz, 1 para um descritor raiz e 2 para uma tabela de descritores.</span><span class="sxs-lookup"><span data-stu-id="92156-118">The performance cost (in terms of levels of indirection) are zero for a root constant, 1 for a root descriptor, and 2 for a descriptor table.</span></span> <span data-ttu-id="92156-119">Se uma assinatura raiz for grande e estourar a memória mais rápida em uma memória um pouco mais lenta (o que pode ocorrer em algum hardware), adicione 1 ao custo de desempenho para os itens de estouro no final da assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="92156-119">If a root signature is large and overflows out of the fastest memory into slightly slower memory (which can happen on some hardware), then add 1 to the performance cost for the overflowing items at the end of the root signature.</span></span>

<span data-ttu-id="92156-120">Um estouro pode ocorrer em hardware que pode ter, por exemplo, um tamanho fixo de 16 DWORDs para o espaço de argumento raiz.</span><span class="sxs-lookup"><span data-stu-id="92156-120">An overflow can occur on hardware that might have, for example, a fixed size of 16 DWORDs for root argument space.</span></span> <span data-ttu-id="92156-121">Esse limite pode ser mais reduzido em um se o montador de entrada for usado.</span><span class="sxs-lookup"><span data-stu-id="92156-121">This limit might be further reduced by one if the Input Assembler is used.</span></span> <span data-ttu-id="92156-122">Nesse caso, há um estouro na memória um pouco mais lenta se a assinatura raiz for muito grande para a memória nativa de 15 ou 16 DWORD.</span><span class="sxs-lookup"><span data-stu-id="92156-122">In this case there is overflow into slightly slower memory if the root signature is too large for the 15 or 16 DWORD native memory.</span></span> <span data-ttu-id="92156-123">Em outro hardware, não há memória de argumento de raiz nativa fixa (portanto, a situação de estouro nunca ocorre).</span><span class="sxs-lookup"><span data-stu-id="92156-123">In other hardware there is no fixed native root argument memory (so the overflow situation never occurs).</span></span>

<span data-ttu-id="92156-124">Para todo o hardware, se qualquer argumento raiz for alterado, o driver deverá manter uma versão de todos os argumentos raiz (ao contrário de outro armazenamento, como heaps de descritores e recursos de buffer, que não têm controle de versão do driver).</span><span class="sxs-lookup"><span data-stu-id="92156-124">For all hardware, if any root argument changes, the driver must maintain a version of all the root arguments (unlike other storage such as descriptor heaps and buffer resources, which are not versioned by the driver).</span></span> <span data-ttu-id="92156-125">No hardware em que ocorre uma situação de estouro, somente a área nativa ou de estouro precisa ter controle de versão, dependendo de onde a alteração ocorreu.</span><span class="sxs-lookup"><span data-stu-id="92156-125">In hardware that an overflow situation occurs, only the native or overflow area needs to be versioned, depending on where the change occurred.</span></span> <span data-ttu-id="92156-126">Obviamente, a quantidade de controle de versão deve ser mantida no mínimo necessário.</span><span class="sxs-lookup"><span data-stu-id="92156-126">The amount of versioning should obviously be kept to the necessary minimum.</span></span>

<span data-ttu-id="92156-127">Em geral, considere as seguintes diretrizes:</span><span class="sxs-lookup"><span data-stu-id="92156-127">Generally, consider the following guidelines:</span></span>

-   <span data-ttu-id="92156-128">Use uma assinatura de raiz pequena, conforme necessário, mas equilibre isso com a flexibilidade de uma assinatura raiz maior.</span><span class="sxs-lookup"><span data-stu-id="92156-128">Use a small a root signature as necessary, though balance this with the flexibility of a larger root signature.</span></span>
-   <span data-ttu-id="92156-129">Organize parâmetros em uma assinatura de raiz grande para que os parâmetros mais prováveis de serem alterados com frequência ou se a latência de acesso baixa de um determinado parâmetro for importante, ocorrer primeiro.</span><span class="sxs-lookup"><span data-stu-id="92156-129">Arrange parameters in a large root signature so that the parameters most likely to change often, or if low access latency for a given parameter is important, occur first.</span></span>
-   <span data-ttu-id="92156-130">Se conveniente, use as constantes raiz ou as exibições de buffer de constantes raiz ao colocar exibições de buffer constantes em um heap de descritor.</span><span class="sxs-lookup"><span data-stu-id="92156-130">If convenient, use root constants or root constant buffer views over putting constant buffer views in a descriptor heap.</span></span>

## <a name="static-samplers"></a><span data-ttu-id="92156-131">Amostras estáticas</span><span class="sxs-lookup"><span data-stu-id="92156-131">Static samplers</span></span>

<span data-ttu-id="92156-132">Os exemplos estáticos (os exemplos em que o estado é totalmente definido e imutável) fazem parte das assinaturas raiz, mas não contam para o limite de 64 DWORD.</span><span class="sxs-lookup"><span data-stu-id="92156-132">Static samplers (samplers where the state is fully defined and immutable) are part of root signatures, but do not count towards the 64 DWORD limit.</span></span> <span data-ttu-id="92156-133">Se uma amostra puder ser definida como estática, não será necessário que a amostra faça parte de um heap de descritor.</span><span class="sxs-lookup"><span data-stu-id="92156-133">If a sampler can be defined as static, there is no need for the sampler to be part of a descriptor heap.</span></span>

<span data-ttu-id="92156-134">Não há nenhum custo de desempenho no uso de amostras estáticas, e uma assinatura raiz pode conter uma mistura de amostras estáticas (armazenadas na assinatura raiz ou em espaço reservado em algum hardware) e amostras dinâmicas (armazenadas em um heap de descritor de amostra).</span><span class="sxs-lookup"><span data-stu-id="92156-134">There is no performance cost to using static samplers, and a root signature can contain a mix of static samplers (stored in the root signature, or in reserved space on some hardware) and dynamic samplers (stored in a sampler descriptor heap).</span></span> <span data-ttu-id="92156-135">Os exemplos de um heap de descritor podem ser atribuídos e indexados dinamicamente, quais amostras estáticas não podem.</span><span class="sxs-lookup"><span data-stu-id="92156-135">Samplers in a descriptor heap can be dynamically assigned and indexed, which static samplers cannot.</span></span>

<span data-ttu-id="92156-136">Os exemplos estáticos podem ser escritos como parte da assinatura raiz em sombreadores HLSL (consulte [especificando assinaturas raiz no HLSL](specifying-root-signatures-in-hlsl.md)).</span><span class="sxs-lookup"><span data-stu-id="92156-136">Static samplers can be written as part of the root signature in HLSL shaders (refer to [Specifying Root Signatures in HLSL](specifying-root-signatures-in-hlsl.md)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="92156-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="92156-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92156-138">Assinaturas raiz</span><span class="sxs-lookup"><span data-stu-id="92156-138">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 





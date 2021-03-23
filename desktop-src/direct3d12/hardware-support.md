---
title: Camadas de hardware
description: Os níveis de hardware da camada 1 para a camada 3 têm recursos crescentes disponíveis para o pipeline.
ms.assetid: 5A640BA9-3914-4481-9A0C-E18B52BD8AFE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38773412d135aa4068f0f843c1a6ef64af06a841
ms.sourcegitcommit: 9d7585cb0b840d0d1a2b7fd02135181e69d0dc9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/15/2020
ms.locfileid: "104548206"
---
# <a name="hardware-tiers"></a><span data-ttu-id="19813-103">Camadas de hardware</span><span class="sxs-lookup"><span data-stu-id="19813-103">Hardware Tiers</span></span>

<span data-ttu-id="19813-104">Os níveis de hardware da camada 1 para a camada 3 têm recursos crescentes disponíveis para o pipeline.</span><span class="sxs-lookup"><span data-stu-id="19813-104">The levels of hardware from Tier 1 to Tier 3 have increasing resources available to the pipeline.</span></span>

-   [<span data-ttu-id="19813-105">Limites dependentes de hardware</span><span class="sxs-lookup"><span data-stu-id="19813-105">Limits dependant on hardware</span></span>](#limits-dependant-on-hardware)
-   [<span data-ttu-id="19813-106">Limites de invariável</span><span class="sxs-lookup"><span data-stu-id="19813-106">Invariable limits</span></span>](#invariable-limits)
-   [<span data-ttu-id="19813-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="19813-107">Related topics</span></span>](#related-topics)

## <a name="limits-dependant-on-hardware"></a><span data-ttu-id="19813-108">Limites dependentes de hardware</span><span class="sxs-lookup"><span data-stu-id="19813-108">Limits dependant on hardware</span></span>



| <span data-ttu-id="19813-109">Recursos disponíveis para o pipeline</span><span class="sxs-lookup"><span data-stu-id="19813-109">Resources Available to the Pipeline</span></span>                                                                                                              | <span data-ttu-id="19813-110">Camada 1</span><span class="sxs-lookup"><span data-stu-id="19813-110">Tier 1</span></span>                                                                   | <span data-ttu-id="19813-111">Camada 2</span><span class="sxs-lookup"><span data-stu-id="19813-111">Tier 2</span></span>        | <span data-ttu-id="19813-112">Nível 3</span><span class="sxs-lookup"><span data-stu-id="19813-112">Tier 3</span></span>        |
|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------|---------------|
| <span data-ttu-id="19813-113">Níveis de recursos</span><span class="sxs-lookup"><span data-stu-id="19813-113">Feature levels</span></span>                                                                                                                                   | <span data-ttu-id="19813-114">11.0 +</span><span class="sxs-lookup"><span data-stu-id="19813-114">11.0+</span></span>                                                                    | <span data-ttu-id="19813-115">11.0 +</span><span class="sxs-lookup"><span data-stu-id="19813-115">11.0+</span></span>         | <span data-ttu-id="19813-116">11.1 +</span><span class="sxs-lookup"><span data-stu-id="19813-116">11.1+</span></span>         |
| <span data-ttu-id="19813-117">Número máximo de descritores em uma CBV (exibição de buffer constante), Modo de Exibição de Recursos de sombreador (SRV) ou heap de exibição de acesso não ordenado (UAV) usado para renderização</span><span class="sxs-lookup"><span data-stu-id="19813-117">Maximum number of descriptors in a Constant Buffer View (CBV), Shader Resource View (SRV), or Unordered Access View(UAV) heap used for rendering</span></span> | <span data-ttu-id="19813-118">1\.000.000</span><span class="sxs-lookup"><span data-stu-id="19813-118">1,000,000</span></span>                                                                | <span data-ttu-id="19813-119">1\.000.000</span><span class="sxs-lookup"><span data-stu-id="19813-119">1,000,000</span></span>     | <span data-ttu-id="19813-120">1000000 +</span><span class="sxs-lookup"><span data-stu-id="19813-120">1,000,000+</span></span>    |
| <span data-ttu-id="19813-121">Número máximo de exibições de buffer de constantes em todas as tabelas de descritores por estágio do sombreador</span><span class="sxs-lookup"><span data-stu-id="19813-121">Maximum number of Constant Buffer Views in all descriptor tables per shader stage</span></span>                                                                | <span data-ttu-id="19813-122">14</span><span class="sxs-lookup"><span data-stu-id="19813-122">14</span></span>                                                                       | <span data-ttu-id="19813-123">14</span><span class="sxs-lookup"><span data-stu-id="19813-123">14</span></span>            | <span data-ttu-id="19813-124">**heap completo**</span><span class="sxs-lookup"><span data-stu-id="19813-124">**full heap**</span></span> |
| <span data-ttu-id="19813-125">Número máximo de exibições de recurso de sombreador em todas as tabelas de descritores por estágio de sombrea</span><span class="sxs-lookup"><span data-stu-id="19813-125">Maximum number of Shader Resource Views in all descriptor tables per shader stage</span></span>                                                                | <span data-ttu-id="19813-126">128</span><span class="sxs-lookup"><span data-stu-id="19813-126">128</span></span>                                                                      | <span data-ttu-id="19813-127">**heap completo**</span><span class="sxs-lookup"><span data-stu-id="19813-127">**full heap**</span></span> | <span data-ttu-id="19813-128">heap completo</span><span class="sxs-lookup"><span data-stu-id="19813-128">full heap</span></span>     |
| <span data-ttu-id="19813-129">Número máximo de exibições de acesso não ordenado em todas as tabelas de descritores em todos os estágios</span><span class="sxs-lookup"><span data-stu-id="19813-129">Maximum number of Unordered Access Views in all descriptor tables across all stages</span></span>                                                              | <span data-ttu-id="19813-130">64 para os níveis de recurso 11.1 +</span><span class="sxs-lookup"><span data-stu-id="19813-130">64 for feature levels 11.1+</span></span><br/> <span data-ttu-id="19813-131">8 para nível de recurso 11</span><span class="sxs-lookup"><span data-stu-id="19813-131">8 for feature level 11</span></span><br/> | <span data-ttu-id="19813-132">64</span><span class="sxs-lookup"><span data-stu-id="19813-132">64</span></span>            | <span data-ttu-id="19813-133">**heap completo**</span><span class="sxs-lookup"><span data-stu-id="19813-133">**full heap**</span></span> |
| <span data-ttu-id="19813-134">Número máximo de amostras em todas as tabelas de descritores por estágio do sombreador</span><span class="sxs-lookup"><span data-stu-id="19813-134">Maximum number of Samplers in all descriptor tables per shader stage</span></span>                                                                             | <span data-ttu-id="19813-135">16</span><span class="sxs-lookup"><span data-stu-id="19813-135">16</span></span>                                                                       | <span data-ttu-id="19813-136">**2048**</span><span class="sxs-lookup"><span data-stu-id="19813-136">**2048**</span></span> | <span data-ttu-id="19813-137">2.048</span><span class="sxs-lookup"><span data-stu-id="19813-137">2048</span></span>     |



 

<span data-ttu-id="19813-138">As entradas em **negrito** realçam melhorias significativas na camada anterior.</span><span class="sxs-lookup"><span data-stu-id="19813-138">**Bold** entries highlight significant improvements over the previous tier.</span></span>

<span data-ttu-id="19813-139">Há uma restrição adicional para o hardware de camada 1 que se aplica a todos os heaps e para o hardware de camada 2 que se aplica a heaps CBV e UAV, que todas as entradas de heap de descritor cobertas por tabelas de descritores na assinatura raiz *devem* ser preenchidas com descritores quando o sombreador for executado, mesmo se o sombreador (talvez devido à ramificação) não</span><span class="sxs-lookup"><span data-stu-id="19813-139">There is an additional restriction for Tier 1 hardware that applies to all heaps, and to Tier 2 hardware that applies to CBV and UAV heaps, that all descriptor heap entries covered by descriptor tables in the root signature *must* be populated with descriptors by the time the shader executes, even if the shader (perhaps due to branching) does not need the descriptor.</span></span> <span data-ttu-id="19813-140">Não há nenhuma restrição para o hardware da camada 3.</span><span class="sxs-lookup"><span data-stu-id="19813-140">There is no such restriction for Tier 3 hardware.</span></span> <span data-ttu-id="19813-141">Uma mitigação para essa restrição é o uso cuidadoso de [descritores nulos](descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="19813-141">One mitigation for this restriction is the diligent use of [Null descriptors](descriptors.md).</span></span>

## <a name="invariable-limits"></a><span data-ttu-id="19813-142">Limites de invariável</span><span class="sxs-lookup"><span data-stu-id="19813-142">Invariable limits</span></span>

<span data-ttu-id="19813-143">O número máximo de amostras em um heap de descritor visível do sombreador é 2048.</span><span class="sxs-lookup"><span data-stu-id="19813-143">The maximum number of samplers in a shader visible descriptor heap is 2048.</span></span>

<span data-ttu-id="19813-144">O número máximo de amostras estáticas exclusivas entre assinaturas raiz dinâmicas é 2032 (que deixa 16 para drivers que precisam de seus próprios exemplos).</span><span class="sxs-lookup"><span data-stu-id="19813-144">The maximum number of unique static samplers across live root signatures is 2032 (which leaves 16 for drivers that need their own samplers).</span></span>

## <a name="related-topics"></a><span data-ttu-id="19813-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="19813-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19813-146">Heaps de descritores</span><span class="sxs-lookup"><span data-stu-id="19813-146">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> <dt>

[<span data-ttu-id="19813-147">Níveis de recursos de hardware</span><span class="sxs-lookup"><span data-stu-id="19813-147">Hardware Feature Levels</span></span>](hardware-feature-levels.md)
</dt> </dl>

 

 






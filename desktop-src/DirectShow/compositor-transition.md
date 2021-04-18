---
description: Transição de compositor
ms.assetid: 7903ecd7-88fb-4277-82ee-a7f71cae0412
title: Transição de compositor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75488e9dbdea4926c515f52352b42f68a2bfa679
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104563386"
---
# <a name="compositor-transition"></a><span data-ttu-id="5d6c1-103">Transição de compositor</span><span class="sxs-lookup"><span data-stu-id="5d6c1-103">Compositor Transition</span></span>

> [!Note]  
> <span data-ttu-id="5d6c1-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="5d6c1-104">\[Deprecated.</span></span> <span data-ttu-id="5d6c1-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5d6c1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5d6c1-106">A transição do compositor compõe um subretângulo do primeiro plano em um retângulo designado em segundo plano, sem alterar o restante do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="5d6c1-106">The Compositor transition composites a subrectangle from the foreground into a designated rectangle on the background, without altering the rest of the background.</span></span> <span data-ttu-id="5d6c1-107">Use essa transição para criar efeitos da tela de divisão ou imagem em imagem.</span><span class="sxs-lookup"><span data-stu-id="5d6c1-107">Use this transition to create split-screen or picture-in-picture effects.</span></span>

<span data-ttu-id="5d6c1-108">A imagem a seguir mostra a transição do compositor:</span><span class="sxs-lookup"><span data-stu-id="5d6c1-108">The following image shows the compositor transition:</span></span>

![transição de compositor](images/trans-compositor.png)

<span data-ttu-id="5d6c1-110">ID de classe (CLSID): {BB44391D-6ABD-422f-9E2E-385C9DFF51FC}</span><span class="sxs-lookup"><span data-stu-id="5d6c1-110">Class ID (CLSID): {BB44391D-6ABD-422f-9E2E-385C9DFF51FC}</span></span>

<span data-ttu-id="5d6c1-111">Nome da variável CLSID: CLSID \_ DxtCompositor</span><span class="sxs-lookup"><span data-stu-id="5d6c1-111">CLSID Variable Name: CLSID\_DxtCompositor</span></span>

<span data-ttu-id="5d6c1-112">Nome amigável: "DxtCompositor"</span><span class="sxs-lookup"><span data-stu-id="5d6c1-112">Friendly Name: "DxtCompositor"</span></span>

<span data-ttu-id="5d6c1-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5d6c1-113">Properties</span></span>



| <span data-ttu-id="5d6c1-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="5d6c1-114">Property</span></span>   | <span data-ttu-id="5d6c1-115">Type</span><span class="sxs-lookup"><span data-stu-id="5d6c1-115">Type</span></span> | <span data-ttu-id="5d6c1-116">Padrão</span><span class="sxs-lookup"><span data-stu-id="5d6c1-116">Default</span></span> | <span data-ttu-id="5d6c1-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d6c1-117">Description</span></span>                                                    |
|------------|------|---------|----------------------------------------------------------------|
| <span data-ttu-id="5d6c1-118">Altura</span><span class="sxs-lookup"><span data-stu-id="5d6c1-118">Height</span></span>     | <span data-ttu-id="5d6c1-119">long</span><span class="sxs-lookup"><span data-stu-id="5d6c1-119">long</span></span> | <span data-ttu-id="5d6c1-120">0</span><span class="sxs-lookup"><span data-stu-id="5d6c1-120">0</span></span>       | <span data-ttu-id="5d6c1-121">Altura do retângulo de destino, em pixels.</span><span class="sxs-lookup"><span data-stu-id="5d6c1-121">Height of the target rectangle, in pixels.</span></span>                     |
| <span data-ttu-id="5d6c1-122">OffsetX</span><span class="sxs-lookup"><span data-stu-id="5d6c1-122">OffsetX</span></span>    | <span data-ttu-id="5d6c1-123">long</span><span class="sxs-lookup"><span data-stu-id="5d6c1-123">long</span></span> | <span data-ttu-id="5d6c1-124">0</span><span class="sxs-lookup"><span data-stu-id="5d6c1-124">0</span></span>       | <span data-ttu-id="5d6c1-125">Deslocamento horizontal do retângulo de destino, em pixels.</span><span class="sxs-lookup"><span data-stu-id="5d6c1-125">Horizontal offset of the target rectangle, in pixels.</span></span>          |
| <span data-ttu-id="5d6c1-126">OffsetY</span><span class="sxs-lookup"><span data-stu-id="5d6c1-126">OffsetY</span></span>    | <span data-ttu-id="5d6c1-127">long</span><span class="sxs-lookup"><span data-stu-id="5d6c1-127">long</span></span> | <span data-ttu-id="5d6c1-128">0</span><span class="sxs-lookup"><span data-stu-id="5d6c1-128">0</span></span>       | <span data-ttu-id="5d6c1-129">Deslocamento vertical do retângulo de destino, em pixels.</span><span class="sxs-lookup"><span data-stu-id="5d6c1-129">Vertical offset of the target rectangle, in pixels.</span></span>            |
| <span data-ttu-id="5d6c1-130">SrcHeight</span><span class="sxs-lookup"><span data-stu-id="5d6c1-130">SrcHeight</span></span>  | <span data-ttu-id="5d6c1-131">long</span><span class="sxs-lookup"><span data-stu-id="5d6c1-131">long</span></span> | <span data-ttu-id="5d6c1-132">0</span><span class="sxs-lookup"><span data-stu-id="5d6c1-132">0</span></span>       | <span data-ttu-id="5d6c1-133">A altura do subretângulo na origem, em pixels.</span><span class="sxs-lookup"><span data-stu-id="5d6c1-133">The height of the subrectangle on the source, in pixels.</span></span>       |
| <span data-ttu-id="5d6c1-134">SrcOffsetX</span><span class="sxs-lookup"><span data-stu-id="5d6c1-134">SrcOffsetX</span></span> | <span data-ttu-id="5d6c1-135">long</span><span class="sxs-lookup"><span data-stu-id="5d6c1-135">long</span></span> | <span data-ttu-id="5d6c1-136">0</span><span class="sxs-lookup"><span data-stu-id="5d6c1-136">0</span></span>       | <span data-ttu-id="5d6c1-137">A coordenada x do subretângulo na origem, em pixels.</span><span class="sxs-lookup"><span data-stu-id="5d6c1-137">The x-coordinate of the subrectangle on the source, in pixels.</span></span> |
| <span data-ttu-id="5d6c1-138">SrcOffsetY</span><span class="sxs-lookup"><span data-stu-id="5d6c1-138">SrcOffsetY</span></span> | <span data-ttu-id="5d6c1-139">long</span><span class="sxs-lookup"><span data-stu-id="5d6c1-139">long</span></span> | <span data-ttu-id="5d6c1-140">0</span><span class="sxs-lookup"><span data-stu-id="5d6c1-140">0</span></span>       | <span data-ttu-id="5d6c1-141">A coordenada y do subretângulo na origem, em pixels.</span><span class="sxs-lookup"><span data-stu-id="5d6c1-141">The y-coordinate of the subrectangle on the source, in pixels.</span></span> |
| <span data-ttu-id="5d6c1-142">SrcWidth</span><span class="sxs-lookup"><span data-stu-id="5d6c1-142">SrcWidth</span></span>   | <span data-ttu-id="5d6c1-143">long</span><span class="sxs-lookup"><span data-stu-id="5d6c1-143">long</span></span> | <span data-ttu-id="5d6c1-144">0</span><span class="sxs-lookup"><span data-stu-id="5d6c1-144">0</span></span>       | <span data-ttu-id="5d6c1-145">A largura do subretângulo na origem, em pixels.</span><span class="sxs-lookup"><span data-stu-id="5d6c1-145">The width of the subrectangle on the source, in pixels.</span></span>        |
| <span data-ttu-id="5d6c1-146">Largura</span><span class="sxs-lookup"><span data-stu-id="5d6c1-146">Width</span></span>      | <span data-ttu-id="5d6c1-147">long</span><span class="sxs-lookup"><span data-stu-id="5d6c1-147">long</span></span> | <span data-ttu-id="5d6c1-148">0</span><span class="sxs-lookup"><span data-stu-id="5d6c1-148">0</span></span>       | <span data-ttu-id="5d6c1-149">Largura do retângulo de destino, em pixels.</span><span class="sxs-lookup"><span data-stu-id="5d6c1-149">Width of the target rectangle, in pixels.</span></span>                      |



 

<span data-ttu-id="5d6c1-150">O diagrama a seguir ilustra essas propriedades:</span><span class="sxs-lookup"><span data-stu-id="5d6c1-150">The following diagram illustrates these properties:</span></span>

![Propriedades do compositor](images/compmeasure.png)

## <a name="related-topics"></a><span data-ttu-id="5d6c1-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5d6c1-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d6c1-153">Transições e efeitos</span><span class="sxs-lookup"><span data-stu-id="5d6c1-153">Transitions and Effects</span></span>](transitions-and-effects.md)
</dt> </dl>

 

 




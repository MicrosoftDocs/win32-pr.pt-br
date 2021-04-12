---
description: ICE95 verifica a tabela de controle e a tabela BBControl para verificar se os controles de mural se encaixam em todas as suas murals.
ms.assetid: 8ba73536-65a5-4658-846c-76356f16b81c
title: ICE95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14144c7739dfcc1f1b5e66d92d8e6c1c46ed49fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171137"
---
# <a name="ice95"></a><span data-ttu-id="c605a-103">ICE95</span><span class="sxs-lookup"><span data-stu-id="c605a-103">ICE95</span></span>

<span data-ttu-id="c605a-104">ICE95 verifica a [tabela de controle](control-table.md) e a [tabela BBControl](bbcontrol-table.md) para verificar se os controles de mural se encaixam em todas as suas murals.</span><span class="sxs-lookup"><span data-stu-id="c605a-104">ICE95 checks the [Control table](control-table.md) and [BBControl table](bbcontrol-table.md) to verify that the billboard controls fit onto all the billboards.</span></span>

## <a name="result"></a><span data-ttu-id="c605a-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="c605a-105">Result</span></span>

<span data-ttu-id="c605a-106">Se qualquer uma das seguintes opções for verdadeira, um controle de mensagem não caberá em um mural.</span><span class="sxs-lookup"><span data-stu-id="c605a-106">If any of the following are true, a billboard control fails to fit on a billboard.</span></span> <span data-ttu-id="c605a-107">ICE95 posta os seguintes avisos.</span><span class="sxs-lookup"><span data-stu-id="c605a-107">ICE95 posts the following warnings.</span></span>



| <span data-ttu-id="c605a-108">Aviso de ICE95</span><span class="sxs-lookup"><span data-stu-id="c605a-108">ICE95 warning</span></span>                                                                                                                                                                                                              | <span data-ttu-id="c605a-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c605a-109">Description</span></span>                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c605a-110">O item de BBControl ' \[ 1 \] . \[ 2 \] ' na tabela BBControl não cabe em todos os controles de mensagem na tabela de controle.</span><span class="sxs-lookup"><span data-stu-id="c605a-110">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="c605a-111">A coordenada X excede o limite da largura mínima do controle do mural% s</span><span class="sxs-lookup"><span data-stu-id="c605a-111">The X coordinate exceeds the boundary of the minimum billboard control width %s</span></span>                   | <span data-ttu-id="c605a-112">A coordenada X do controle está fora da largura do mural.</span><span class="sxs-lookup"><span data-stu-id="c605a-112">The control's X coordinate is outside the width of the billboard.</span></span>                          |
| <span data-ttu-id="c605a-113">O item de BBControl ' \[ 1 \] . \[ 2 \] ' na tabela BBControl não cabe em todos os controles de mensagem na tabela de controle.</span><span class="sxs-lookup"><span data-stu-id="c605a-113">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="c605a-114">A coordenada Y excede o limite da altura mínima do controle do mural% s</span><span class="sxs-lookup"><span data-stu-id="c605a-114">The Y coordinate exceeds the boundary of the minimum billboard control height %s</span></span>                  | <span data-ttu-id="c605a-115">A coordenada Y do controle está abaixo da parte inferior do mural.</span><span class="sxs-lookup"><span data-stu-id="c605a-115">The control's Y coordinate is below the bottom of the billboard.</span></span>                           |
| <span data-ttu-id="c605a-116">O item de BBControl ' \[ 1 \] . \[ 2 \] ' na tabela BBControl não cabe em todos os controles de mensagem na tabela de controle.</span><span class="sxs-lookup"><span data-stu-id="c605a-116">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="c605a-117">A coordenada X e a largura combinadas em conjunto excedem a largura mínima do controle do mural% s</span><span class="sxs-lookup"><span data-stu-id="c605a-117">The X coordinate and the width combined together exceeds the minimum billboard control width %s</span></span>   | <span data-ttu-id="c605a-118">A coordenada X do controle mais a largura do controle está fora da largura do mural.</span><span class="sxs-lookup"><span data-stu-id="c605a-118">The control's X coordinate plus the control's width is outside the width of the billboard.</span></span> |
| <span data-ttu-id="c605a-119">O item de BBControl ' \[ 1 \] . \[ 2 \] ' na tabela BBControl não cabe em todos os controles de mensagem na tabela de controle.</span><span class="sxs-lookup"><span data-stu-id="c605a-119">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="c605a-120">A coordenada Y e a altura combinadas em conjunto excedem a altura mínima de controle do mural% s</span><span class="sxs-lookup"><span data-stu-id="c605a-120">The Y coordinate and the height combined together exceeds the minimum billboard control height %s</span></span> | <span data-ttu-id="c605a-121">A coordenada Y do controle mais a altura do controle está abaixo da parte inferior do mural.</span><span class="sxs-lookup"><span data-stu-id="c605a-121">The control's Y coordinate plus the control's height is below the bottom of the billboard.</span></span> |



 

## <a name="example"></a><span data-ttu-id="c605a-122">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c605a-122">Example</span></span>

<span data-ttu-id="c605a-123">ICE95 relata os seguintes avisos para o exemplo:</span><span class="sxs-lookup"><span data-stu-id="c605a-123">ICE95 reports the following warnings for the example:</span></span>

``` syntax
The BBControl item 'billboard1.bbcontrol1' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate exceeds the boundary of the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol2' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate exceeds the boundary of the minimum billboard control height 100
The BBControl item 'billboard1.bbcontrol3' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate and the width combined together exceeds the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol4' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate and the height combined together exceeds the minimum billboard control height 100
```

<span data-ttu-id="c605a-124">Tabela de controle (parcial) (parcial)</span><span class="sxs-lookup"><span data-stu-id="c605a-124">Control Table (partial) (partial)</span></span>



| <span data-ttu-id="c605a-125">Control</span><span class="sxs-lookup"><span data-stu-id="c605a-125">Control</span></span>  | <span data-ttu-id="c605a-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="c605a-126">Type</span></span>      | <span data-ttu-id="c605a-127">Largura</span><span class="sxs-lookup"><span data-stu-id="c605a-127">Width</span></span> | <span data-ttu-id="c605a-128">Altura</span><span class="sxs-lookup"><span data-stu-id="c605a-128">Height</span></span> |
|----------|-----------|-------|--------|
| <span data-ttu-id="c605a-129">Control1</span><span class="sxs-lookup"><span data-stu-id="c605a-129">control1</span></span> | <span data-ttu-id="c605a-130">Mensagem</span><span class="sxs-lookup"><span data-stu-id="c605a-130">Billboard</span></span> | <span data-ttu-id="c605a-131">300</span><span class="sxs-lookup"><span data-stu-id="c605a-131">300</span></span>   | <span data-ttu-id="c605a-132">100</span><span class="sxs-lookup"><span data-stu-id="c605a-132">100</span></span>    |
| <span data-ttu-id="c605a-133">Control2</span><span class="sxs-lookup"><span data-stu-id="c605a-133">Control2</span></span> | <span data-ttu-id="c605a-134">Mensagem</span><span class="sxs-lookup"><span data-stu-id="c605a-134">Billboard</span></span> | <span data-ttu-id="c605a-135">100</span><span class="sxs-lookup"><span data-stu-id="c605a-135">100</span></span>   | <span data-ttu-id="c605a-136">300</span><span class="sxs-lookup"><span data-stu-id="c605a-136">300</span></span>    |



 

[<span data-ttu-id="c605a-137">Tabela BBControl</span><span class="sxs-lookup"><span data-stu-id="c605a-137">BBControl table</span></span>](bbcontrol-table.md)



| <span data-ttu-id="c605a-138">Mensagem\_</span><span class="sxs-lookup"><span data-stu-id="c605a-138">Billboard\_</span></span> | <span data-ttu-id="c605a-139">BBControl</span><span class="sxs-lookup"><span data-stu-id="c605a-139">BBControl</span></span>  | <span data-ttu-id="c605a-140">X</span><span class="sxs-lookup"><span data-stu-id="c605a-140">X</span></span>   | <span data-ttu-id="c605a-141">S</span><span class="sxs-lookup"><span data-stu-id="c605a-141">Y</span></span>   | <span data-ttu-id="c605a-142">Largura</span><span class="sxs-lookup"><span data-stu-id="c605a-142">Width</span></span> | <span data-ttu-id="c605a-143">Altura</span><span class="sxs-lookup"><span data-stu-id="c605a-143">Height</span></span> |
|-------------|------------|-----|-----|-------|--------|
| <span data-ttu-id="c605a-144">billboard1</span><span class="sxs-lookup"><span data-stu-id="c605a-144">billboard1</span></span>  | <span data-ttu-id="c605a-145">bbcontrol1</span><span class="sxs-lookup"><span data-stu-id="c605a-145">bbcontrol1</span></span> | <span data-ttu-id="c605a-146">200</span><span class="sxs-lookup"><span data-stu-id="c605a-146">200</span></span> | <span data-ttu-id="c605a-147">0</span><span class="sxs-lookup"><span data-stu-id="c605a-147">0</span></span>   | <span data-ttu-id="c605a-148">100</span><span class="sxs-lookup"><span data-stu-id="c605a-148">100</span></span>   | <span data-ttu-id="c605a-149">100</span><span class="sxs-lookup"><span data-stu-id="c605a-149">100</span></span>    |
| <span data-ttu-id="c605a-150">billboard1</span><span class="sxs-lookup"><span data-stu-id="c605a-150">billboard1</span></span>  | <span data-ttu-id="c605a-151">bbcontrol2</span><span class="sxs-lookup"><span data-stu-id="c605a-151">bbcontrol2</span></span> | <span data-ttu-id="c605a-152">0</span><span class="sxs-lookup"><span data-stu-id="c605a-152">0</span></span>   | <span data-ttu-id="c605a-153">200</span><span class="sxs-lookup"><span data-stu-id="c605a-153">200</span></span> | <span data-ttu-id="c605a-154">100</span><span class="sxs-lookup"><span data-stu-id="c605a-154">100</span></span>   | <span data-ttu-id="c605a-155">100</span><span class="sxs-lookup"><span data-stu-id="c605a-155">100</span></span>    |
| <span data-ttu-id="c605a-156">billboard1</span><span class="sxs-lookup"><span data-stu-id="c605a-156">billboard1</span></span>  | <span data-ttu-id="c605a-157">bbcontrol3</span><span class="sxs-lookup"><span data-stu-id="c605a-157">bbcontrol3</span></span> | <span data-ttu-id="c605a-158">50</span><span class="sxs-lookup"><span data-stu-id="c605a-158">50</span></span>  | <span data-ttu-id="c605a-159">0</span><span class="sxs-lookup"><span data-stu-id="c605a-159">0</span></span>   | <span data-ttu-id="c605a-160">100</span><span class="sxs-lookup"><span data-stu-id="c605a-160">100</span></span>   | <span data-ttu-id="c605a-161">50</span><span class="sxs-lookup"><span data-stu-id="c605a-161">50</span></span>     |
| <span data-ttu-id="c605a-162">billboard1</span><span class="sxs-lookup"><span data-stu-id="c605a-162">billboard1</span></span>  | <span data-ttu-id="c605a-163">bbcontrol4</span><span class="sxs-lookup"><span data-stu-id="c605a-163">bbcontrol4</span></span> | <span data-ttu-id="c605a-164">0</span><span class="sxs-lookup"><span data-stu-id="c605a-164">0</span></span>   | <span data-ttu-id="c605a-165">50</span><span class="sxs-lookup"><span data-stu-id="c605a-165">50</span></span>  | <span data-ttu-id="c605a-166">50</span><span class="sxs-lookup"><span data-stu-id="c605a-166">50</span></span>    | <span data-ttu-id="c605a-167">100</span><span class="sxs-lookup"><span data-stu-id="c605a-167">100</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="c605a-168">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c605a-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c605a-169">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="c605a-169">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




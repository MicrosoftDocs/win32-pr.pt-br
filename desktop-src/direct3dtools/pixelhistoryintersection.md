---
description: Representa informações sobre um específico.
MS-HAID: vspixengine.PixelHistoryIntersection
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura PixelHistoryIntersection
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D67A116D-B1D0-4E88-A2FF-611CDF4003B2
api_name:
- PixelHistoryIntersection
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 735adc5396551a18b5e2e2dfba781b358289475e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105760640"
---
# <a name="span-idvspixenginepixelhistoryintersectionspanpixelhistoryintersection-structure"></a><span data-ttu-id="40943-103"><span id="vspixengine.pixelhistoryintersection"></span>Estrutura PixelHistoryIntersection</span><span class="sxs-lookup"><span data-stu-id="40943-103"><span id="vspixengine.pixelhistoryintersection"></span>PixelHistoryIntersection structure</span></span>

<span data-ttu-id="40943-104">Representa informações sobre um determinado</span><span class="sxs-lookup"><span data-stu-id="40943-104">Represents information about a particular</span></span>

## <a name="syntax"></a><span data-ttu-id="40943-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40943-105">Syntax</span></span>


```C++
} PixelHistoryIntersection;
```

## <a name="members"></a><span data-ttu-id="40943-106">Membros</span><span class="sxs-lookup"><span data-stu-id="40943-106">Members</span></span>

<span data-ttu-id="40943-107">**frameNumber**</span><span class="sxs-lookup"><span data-stu-id="40943-107">**frameNumber**</span></span>  
<span data-ttu-id="40943-108">O quadro do evento de gráficos assocaited com esta operação.</span><span class="sxs-lookup"><span data-stu-id="40943-108">The frame of the graphics event assocaited with this operation.</span></span>

<span data-ttu-id="40943-109">**Eid**</span><span class="sxs-lookup"><span data-stu-id="40943-109">**eid**</span></span>  
<span data-ttu-id="40943-110">A ID do evento de gráficos associado a esta operação.</span><span class="sxs-lookup"><span data-stu-id="40943-110">The ID of the graphics event associated with this operation.</span></span>

<span data-ttu-id="40943-111">**renderTargetPtr**</span><span class="sxs-lookup"><span data-stu-id="40943-111">**renderTargetPtr**</span></span>  
<span data-ttu-id="40943-112">O destino de renderização originalmente associado (dentro do aplicativo capturado) com esta operação.</span><span class="sxs-lookup"><span data-stu-id="40943-112">The render target originally associated (inside the captured application) with this operation.</span></span>

<span data-ttu-id="40943-113">**eventType**</span><span class="sxs-lookup"><span data-stu-id="40943-113">**eventType**</span></span>  
<span data-ttu-id="40943-114">O tipo de evento associado a essa operação (especificamente, se esse evento é uma chamada de desenho).</span><span class="sxs-lookup"><span data-stu-id="40943-114">The kind of event associated with this operation (specifically, whether this event is a draw call).</span></span>

<span data-ttu-id="40943-115">**empresas**</span><span class="sxs-lookup"><span data-stu-id="40943-115">**point**</span></span>  
<span data-ttu-id="40943-116">As coordenadas do pixel no framebuffer.</span><span class="sxs-lookup"><span data-stu-id="40943-116">The coordinates of the pixel in the framebuffer.</span></span>

<span data-ttu-id="40943-117">**bAssemblerStageGeneratesInstanceID**</span><span class="sxs-lookup"><span data-stu-id="40943-117">**bAssemblerStageGeneratesInstanceID**</span></span>  
<span data-ttu-id="40943-118">true se o montador de entrada gerar IDs de instância; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="40943-118">true if the input assembler generates instance IDs; otherwise false.</span></span>

<span data-ttu-id="40943-119">**sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="40943-119">**flags**</span></span>  
<span data-ttu-id="40943-120">Uma combinação de valores PIXELHISTORYFLAGS.</span><span class="sxs-lookup"><span data-stu-id="40943-120">A combination of PIXELHISTORYFLAGS values.</span></span> <span data-ttu-id="40943-121">Para obter mais informações, consulte a enumeração PIXELHISTORYFLAGS.</span><span class="sxs-lookup"><span data-stu-id="40943-121">For more information, see the PIXELHISTORYFLAGS enumeration.</span></span>

<span data-ttu-id="40943-122">**fbInitialRed**</span><span class="sxs-lookup"><span data-stu-id="40943-122">**fbInitialRed**</span></span>  
<span data-ttu-id="40943-123">Framebuffer: valor do componente de cor vermelha de framebuffer antes de qualquer saída de sombreador de pixel ser mesclada; ou seja, no início deste quadro.</span><span class="sxs-lookup"><span data-stu-id="40943-123">Framebuffer: value of red color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="40943-124">**fbInitialGreen**</span><span class="sxs-lookup"><span data-stu-id="40943-124">**fbInitialGreen**</span></span>  
<span data-ttu-id="40943-125">Framebuffer: valor do componente de cor verde de framebuffer antes de qualquer saída de sombreador de pixel ser mesclada; ou seja, no início deste quadro.</span><span class="sxs-lookup"><span data-stu-id="40943-125">Framebuffer: value of green color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="40943-126">**fbInitialBlue**</span><span class="sxs-lookup"><span data-stu-id="40943-126">**fbInitialBlue**</span></span>  
<span data-ttu-id="40943-127">Framebuffer: valor do componente de cor azul de framebuffer antes de qualquer saída de sombreador de pixel ser mesclada; ou seja, no início deste quadro.</span><span class="sxs-lookup"><span data-stu-id="40943-127">Framebuffer: value of blue color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="40943-128">**fbInitialAlpha**</span><span class="sxs-lookup"><span data-stu-id="40943-128">**fbInitialAlpha**</span></span>  
<span data-ttu-id="40943-129">Framebuffer: o valor do componente de cor alfa de framebuffer antes que qualquer saída de sombreador de pixel seja mesclada; ou seja, no início deste quadro.</span><span class="sxs-lookup"><span data-stu-id="40943-129">Framebuffer: value of alpha color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="40943-130">**LabelFBInitialRed**</span><span class="sxs-lookup"><span data-stu-id="40943-130">**LabelFBInitialRed**</span></span>  
<span data-ttu-id="40943-131">Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor vermelha do framebuffer antes de qualquer sombreamento de pixel; ou seja, no início deste quadro.</span><span class="sxs-lookup"><span data-stu-id="40943-131">A COM string containing the name of the label associated with the red color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="40943-132">**LabelFBInitialGreen**</span><span class="sxs-lookup"><span data-stu-id="40943-132">**LabelFBInitialGreen**</span></span>  
<span data-ttu-id="40943-133">Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor verde do framebuffer antes de qualquer sombreamento de pixel; ou seja, no início deste quadro.</span><span class="sxs-lookup"><span data-stu-id="40943-133">A COM string containing the name of the label associated with the green color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="40943-134">**LabelFBInitialBlue**</span><span class="sxs-lookup"><span data-stu-id="40943-134">**LabelFBInitialBlue**</span></span>  
<span data-ttu-id="40943-135">Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor azul do framebuffer antes de qualquer sombreamento de pixel; ou seja, no início deste quadro.</span><span class="sxs-lookup"><span data-stu-id="40943-135">A COM string containing the name of the label associated with the blue color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="40943-136">**LabelFBInitialAlpha**</span><span class="sxs-lookup"><span data-stu-id="40943-136">**LabelFBInitialAlpha**</span></span>  
<span data-ttu-id="40943-137">Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor alfa do framebuffer antes de qualquer sombreamento de pixel; ou seja, no início deste quadro.</span><span class="sxs-lookup"><span data-stu-id="40943-137">A COM string containing the name of the label associated with the alpha color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="40943-138">**fbRed**</span><span class="sxs-lookup"><span data-stu-id="40943-138">**fbRed**</span></span>  
<span data-ttu-id="40943-139">Framebuffer: valor do componente de cor vermelha de framebuffer depois que a saída do sombreador de pixel é mesclada; ou seja, a cor final do framebuffer.</span><span class="sxs-lookup"><span data-stu-id="40943-139">Framebuffer: value of red color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="40943-140">**fbGreen**</span><span class="sxs-lookup"><span data-stu-id="40943-140">**fbGreen**</span></span>  
<span data-ttu-id="40943-141">Framebuffer: valor do componente de cor verde de framebuffer depois que a saída do sombreador de pixel é mesclada; ou seja, a cor final do framebuffer.</span><span class="sxs-lookup"><span data-stu-id="40943-141">Framebuffer: value of green color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="40943-142">**fbBlue**</span><span class="sxs-lookup"><span data-stu-id="40943-142">**fbBlue**</span></span>  
<span data-ttu-id="40943-143">Framebuffer: valor do componente de cor azul de framebuffer depois que a saída do sombreador de pixel é mesclada; ou seja, a cor final do framebuffer.</span><span class="sxs-lookup"><span data-stu-id="40943-143">Framebuffer: value of blue color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="40943-144">**fbAlpha**</span><span class="sxs-lookup"><span data-stu-id="40943-144">**fbAlpha**</span></span>  
<span data-ttu-id="40943-145">Framebuffer: o valor do componente de cor alfa de framebuffer depois que a saída do sombreador de pixel é mesclada; ou seja, a cor final do framebuffer.</span><span class="sxs-lookup"><span data-stu-id="40943-145">Framebuffer: value of alpha color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="40943-146">**LabelFBRed**</span><span class="sxs-lookup"><span data-stu-id="40943-146">**LabelFBRed**</span></span>  
<span data-ttu-id="40943-147">Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor vermelha do framebuffer após todo o sombreamento de pixel; ou seja, a cor final do framebuffer.</span><span class="sxs-lookup"><span data-stu-id="40943-147">A COM string containing the name of the label associated with the red color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="40943-148">**LabelFBGreen**</span><span class="sxs-lookup"><span data-stu-id="40943-148">**LabelFBGreen**</span></span>  
<span data-ttu-id="40943-149">Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor verde do framebuffer após todo o sombreamento de pixel; ou seja, a cor final do framebuffer.</span><span class="sxs-lookup"><span data-stu-id="40943-149">A COM string containing the name of the label associated with the green color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="40943-150">**LabelFBBlue**</span><span class="sxs-lookup"><span data-stu-id="40943-150">**LabelFBBlue**</span></span>  
<span data-ttu-id="40943-151">Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor azul do framebuffer após todo o sombreamento de pixel; ou seja, a cor final do framebuffer.</span><span class="sxs-lookup"><span data-stu-id="40943-151">A COM string containing the name of the label associated with the blue color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="40943-152">**LabelFBAlpha**</span><span class="sxs-lookup"><span data-stu-id="40943-152">**LabelFBAlpha**</span></span>  
<span data-ttu-id="40943-153">Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor alfa do framebuffer após todo o sombreamento de pixel; ou seja, a cor final do framebuffer.</span><span class="sxs-lookup"><span data-stu-id="40943-153">A COM string containing the name of the label associated with the alpha color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="40943-154">**pixelKillReason**</span><span class="sxs-lookup"><span data-stu-id="40943-154">**pixelKillReason**</span></span>  
<span data-ttu-id="40943-155">Especifica o motivo pelo qual a contribuição de cores do pixel foi interrompida.</span><span class="sxs-lookup"><span data-stu-id="40943-155">Specifies the reason that the pixel's color contribution was killed.</span></span>

<span data-ttu-id="40943-156">**Resultado**</span><span class="sxs-lookup"><span data-stu-id="40943-156">**HResult**</span></span>  
<span data-ttu-id="40943-157">Se ocorreu um erro, contém o HRESULT do DirectX que especifica o erro.</span><span class="sxs-lookup"><span data-stu-id="40943-157">If an error occurred, contains the DirectX HRESULT that specifies the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="40943-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40943-158">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="40943-159">parâmetro</span><span class="sxs-lookup"><span data-stu-id="40943-159">Header</span></span></p></td><td><span data-ttu-id="40943-160">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="40943-160">Vspixengine.h</span></span></td></tr></tbody></table>

 

 




---
description: Uma enumeração usada para indicar por que um pixel foi rejeitado.
MS-HAID: vspixengine.PIXELKILLREASON
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeração PIXELKILLREASON
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 43836288-554B-430C-861D-AAC58DE3B282
api_name:
- PIXELKILLREASON
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f87b072eec1ac98ca68171593765567f5e77e70e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104296013"
---
# <a name="span-idvspixenginepixelkillreasonspanpixelkillreason-enumeration"></a><span data-ttu-id="071b4-103"><span id="vspixengine.pixelkillreason"></span>Enumeração PIXELKILLREASON</span><span class="sxs-lookup"><span data-stu-id="071b4-103"><span id="vspixengine.pixelkillreason"></span>PIXELKILLREASON enumeration</span></span>

<span data-ttu-id="071b4-104">Uma enumeração usada para indicar por que um pixel foi rejeitado.</span><span class="sxs-lookup"><span data-stu-id="071b4-104">An enum used to indicate why a pixel was rejected.</span></span>

## <a name="syntax"></a><span data-ttu-id="071b4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="071b4-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="071b4-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="071b4-106">Constants</span></span>

<span data-ttu-id="071b4-107"><span id="PKR_NONE"></span><span id="pkr_none"></span>**PKR \_ nenhum**</span><span class="sxs-lookup"><span data-stu-id="071b4-107"><span id="PKR_NONE"></span><span id="pkr_none"></span>**PKR\_NONE**</span></span>  
<span data-ttu-id="071b4-108">Um valor que indica que o pixel não foi rejeitado.</span><span class="sxs-lookup"><span data-stu-id="071b4-108">A value that indicates that the pixel was not rejected.</span></span>

<span data-ttu-id="071b4-109"><span id="PKR_SHADERKILL"></span><span id="pkr_shaderkill"></span>**PKR \_ SHADERKILL**</span><span class="sxs-lookup"><span data-stu-id="071b4-109"><span id="PKR_SHADERKILL"></span><span id="pkr_shaderkill"></span>**PKR\_SHADERKILL**</span></span>  
<span data-ttu-id="071b4-110">Um valor que indica que o pixel foi rejeitado porque o sombreador não foi executado.</span><span class="sxs-lookup"><span data-stu-id="071b4-110">A value that indicates that the pixel was rejected because the shader didn't run.</span></span>

<span data-ttu-id="071b4-111"><span id="PKR_SCISSORTEST"></span><span id="pkr_scissortest"></span>**PKR \_ SCISSORTEST**</span><span class="sxs-lookup"><span data-stu-id="071b4-111"><span id="PKR_SCISSORTEST"></span><span id="pkr_scissortest"></span>**PKR\_SCISSORTEST**</span></span>  
<span data-ttu-id="071b4-112">Um valor que indica que o pixel foi rejeitado porque houve falha no teste de tesoura.</span><span class="sxs-lookup"><span data-stu-id="071b4-112">A value that indicates that the pixel was rejected because the scissor test failed.</span></span>

<span data-ttu-id="071b4-113"><span id="PKR_ALPHATEST"></span><span id="pkr_alphatest"></span>**PKR \_ ALPHATEST**</span><span class="sxs-lookup"><span data-stu-id="071b4-113"><span id="PKR_ALPHATEST"></span><span id="pkr_alphatest"></span>**PKR\_ALPHATEST**</span></span>  
<span data-ttu-id="071b4-114">Um valor que indica que o pixel foi rejeitado porque o teste alfa falhou.</span><span class="sxs-lookup"><span data-stu-id="071b4-114">A value that indicates that the pixel was rejected because the alpha test failed.</span></span>

<span data-ttu-id="071b4-115"><span id="PKR_STENCILTEST"></span><span id="pkr_stenciltest"></span>**PKR \_ STENCILTEST**</span><span class="sxs-lookup"><span data-stu-id="071b4-115"><span id="PKR_STENCILTEST"></span><span id="pkr_stenciltest"></span>**PKR\_STENCILTEST**</span></span>  
<span data-ttu-id="071b4-116">Um valor que indica que o pixel foi rejeitado porque o teste de estêncil falhou.</span><span class="sxs-lookup"><span data-stu-id="071b4-116">A value that indicates that the pixel was rejected because the stencil test failed.</span></span>

<span data-ttu-id="071b4-117"><span id="PKR_DEPTHTEST"></span><span id="pkr_depthtest"></span>**PKR \_ DEPTHTEST**</span><span class="sxs-lookup"><span data-stu-id="071b4-117"><span id="PKR_DEPTHTEST"></span><span id="pkr_depthtest"></span>**PKR\_DEPTHTEST**</span></span>  
<span data-ttu-id="071b4-118">Um valor que indica que o pixel foi rejeitado porque o teste de profundidade falhou.</span><span class="sxs-lookup"><span data-stu-id="071b4-118">A value that indicates that the pixel was rejected because the depth test failed.</span></span>

<span data-ttu-id="071b4-119"><span id="PKR_NOTCOMPUTABLE"></span><span id="pkr_notcomputable"></span>**PKR \_ NOTCOMPUTABLE**</span><span class="sxs-lookup"><span data-stu-id="071b4-119"><span id="PKR_NOTCOMPUTABLE"></span><span id="pkr_notcomputable"></span>**PKR\_NOTCOMPUTABLE**</span></span>  
<span data-ttu-id="071b4-120">Um valor que indica que o histórico de pixels não pode ser computado.</span><span class="sxs-lookup"><span data-stu-id="071b4-120">A value that indicates that the pixel history can't be computed.</span></span>

<span data-ttu-id="071b4-121"><span id="PKR_ERROR"></span><span id="pkr_error"></span>**erro de PKR \_**</span><span class="sxs-lookup"><span data-stu-id="071b4-121"><span id="PKR_ERROR"></span><span id="pkr_error"></span>**PKR\_ERROR**</span></span>  
<span data-ttu-id="071b4-122">Um valor que indica que o pixel foi rejeitado devido a um erro geral.</span><span class="sxs-lookup"><span data-stu-id="071b4-122">A value that indicates that the pixel was rejected because of a general error.</span></span>

<span data-ttu-id="071b4-123"><span id="PKR_NOINTERSECTION"></span><span id="pkr_nointersection"></span>**PKR sem \_ INTERseção**</span><span class="sxs-lookup"><span data-stu-id="071b4-123"><span id="PKR_NOINTERSECTION"></span><span id="pkr_nointersection"></span>**PKR\_NOINTERSECTION**</span></span>  
<span data-ttu-id="071b4-124">Um valor que indica que o pixel foi rejeitado porque a chamada de desenho não cruza o pixel.</span><span class="sxs-lookup"><span data-stu-id="071b4-124">A value that indicates that the pixel was rejected because the draw call does not intersect the pixel.</span></span>

<span data-ttu-id="071b4-125"><span id="PKR_OCCLUDED"></span><span id="pkr_occluded"></span>**PKR \_ obstruído**</span><span class="sxs-lookup"><span data-stu-id="071b4-125"><span id="PKR_OCCLUDED"></span><span id="pkr_occluded"></span>**PKR\_OCCLUDED**</span></span>  
<span data-ttu-id="071b4-126">Um valor que indica que o pixel foi rejeitado porque o desenho foi obstruído.</span><span class="sxs-lookup"><span data-stu-id="071b4-126">A value that indicates that the pixel was rejected because the draw was occluded.</span></span>

<span data-ttu-id="071b4-127"><span id="PKR_DEPTHSTENCILTEST"></span><span id="pkr_depthstenciltest"></span>**PKR \_ DEPTHSTENCILTEST**</span><span class="sxs-lookup"><span data-stu-id="071b4-127"><span id="PKR_DEPTHSTENCILTEST"></span><span id="pkr_depthstenciltest"></span>**PKR\_DEPTHSTENCILTEST**</span></span>  
<span data-ttu-id="071b4-128">Um valor que indica que o pixel foi rejeitado porque a profundidade e o teste de estêncil falharam.</span><span class="sxs-lookup"><span data-stu-id="071b4-128">A value that indicates that the pixel was rejected because the depth and stencil test failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="071b4-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="071b4-129">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="071b4-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="071b4-130">Header</span></span></p></td><td><span data-ttu-id="071b4-131">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="071b4-131">Vspixengine.h</span></span></td></tr></tbody></table>

 

 




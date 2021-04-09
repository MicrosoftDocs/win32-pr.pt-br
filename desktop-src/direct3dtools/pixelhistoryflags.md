---
description: Um enum que contém sinalizadores usados para descrever um resultado de histórico de pixel. Consulte PixelHistoryOperation.
MS-HAID: vspixengine.PIXELHISTORYFLAGS
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeração PIXELHISTORYFLAGS
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BDB88A2D-016A-4E15-B47A-870A2959E943
api_name:
- PIXELHISTORYFLAGS
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2a1b4b0e5b3df84af04d5533ec9d53b15ebe5057
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087485"
---
# <a name="span-idvspixenginepixelhistoryflagsspanpixelhistoryflags-enumeration"></a><span data-ttu-id="135eb-104"><span id="vspixengine.pixelhistoryflags"></span>Enumeração PIXELHISTORYFLAGS</span><span class="sxs-lookup"><span data-stu-id="135eb-104"><span id="vspixengine.pixelhistoryflags"></span>PIXELHISTORYFLAGS enumeration</span></span>

<span data-ttu-id="135eb-105">Um enum que contém sinalizadores usados para descrever um resultado de histórico de pixel.</span><span class="sxs-lookup"><span data-stu-id="135eb-105">An enum containing flags used to describe a pixel history result.</span></span> <span data-ttu-id="135eb-106">Consulte PixelHistoryOperation.</span><span class="sxs-lookup"><span data-stu-id="135eb-106">See PixelHistoryOperation.</span></span>

## <a name="syntax"></a><span data-ttu-id="135eb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="135eb-107">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="135eb-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="135eb-108">Constants</span></span>

<span data-ttu-id="135eb-109"><span id="PHF_INITIALVALUE"></span><span id="phf_initialvalue"></span>**PHF \_ inicialvalue**</span><span class="sxs-lookup"><span data-stu-id="135eb-109"><span id="PHF_INITIALVALUE"></span><span id="phf_initialvalue"></span>**PHF\_INITIALVALUE**</span></span>  
<span data-ttu-id="135eb-110">Um sinalizador que corresponde ao valor de cor inicial (antes do quadro).</span><span class="sxs-lookup"><span data-stu-id="135eb-110">A flag that corresponds to the initial color value (prior to frame).</span></span>

<span data-ttu-id="135eb-111"><span id="PHF_CLEAR"></span><span id="phf_clear"></span>**PHF \_ limpar**</span><span class="sxs-lookup"><span data-stu-id="135eb-111"><span id="PHF_CLEAR"></span><span id="phf_clear"></span>**PHF\_CLEAR**</span></span>  
<span data-ttu-id="135eb-112">Um sinalizador que corresponde ao resultado da cor clara.</span><span class="sxs-lookup"><span data-stu-id="135eb-112">A flag that corresponds to the clear color result.</span></span>

<span data-ttu-id="135eb-113"><span id="PHF_DRAW"></span><span id="phf_draw"></span>**PHF \_ desenho**</span><span class="sxs-lookup"><span data-stu-id="135eb-113"><span id="PHF_DRAW"></span><span id="phf_draw"></span>**PHF\_DRAW**</span></span>  
<span data-ttu-id="135eb-114">Um sinalizador que corresponde ao resultado da cor de desenho.</span><span class="sxs-lookup"><span data-stu-id="135eb-114">A flag that corresponds to the draw color result.</span></span>

<span data-ttu-id="135eb-115"><span id="PHF_FINALVALUE"></span><span id="phf_finalvalue"></span>**\_FinalValue de PHF**</span><span class="sxs-lookup"><span data-stu-id="135eb-115"><span id="PHF_FINALVALUE"></span><span id="phf_finalvalue"></span>**PHF\_FINALVALUE**</span></span>  
<span data-ttu-id="135eb-116">Um sinalizador que corresponde ao resultado da cor final.</span><span class="sxs-lookup"><span data-stu-id="135eb-116">A flag that corresponds to the final color result.</span></span>

<span data-ttu-id="135eb-117"><span id="PHF_HASCOLOR"></span><span id="phf_hascolor"></span>**PHF \_ HASCOLOR**</span><span class="sxs-lookup"><span data-stu-id="135eb-117"><span id="PHF_HASCOLOR"></span><span id="phf_hascolor"></span>**PHF\_HASCOLOR**</span></span>  
<span data-ttu-id="135eb-118">Um sinalizador que corresponde a se o resultado da cor está presente no struct PixelHistoryOperation.</span><span class="sxs-lookup"><span data-stu-id="135eb-118">A flag that corresponds to whether the color result is present in the PixelHistoryOperation struct.</span></span>

<span data-ttu-id="135eb-119"><span id="PHF_HASFBCOLOR"></span><span id="phf_hasfbcolor"></span>**PHF \_ HASFBCOLOR**</span><span class="sxs-lookup"><span data-stu-id="135eb-119"><span id="PHF_HASFBCOLOR"></span><span id="phf_hasfbcolor"></span>**PHF\_HASFBCOLOR**</span></span>  
<span data-ttu-id="135eb-120">Um sinalizador que corresponde a se o resultado da cor do buffer final está presente no struct PixelHistoryOperation.</span><span class="sxs-lookup"><span data-stu-id="135eb-120">A flag that corresponds to whether the final buffer color result is present in the PixelHistoryOperation struct.</span></span>

<span data-ttu-id="135eb-121"><span id="PHF_ERROR"></span><span id="phf_error"></span>**erro de PHF \_**</span><span class="sxs-lookup"><span data-stu-id="135eb-121"><span id="PHF_ERROR"></span><span id="phf_error"></span>**PHF\_ERROR**</span></span>  

<span data-ttu-id="135eb-122"><span id="PHF_VERTEXPROCESSINGSKIPPED"></span><span id="phf_vertexprocessingskipped"></span>**PHF \_ VERTEXPROCESSINGSKIPPED**</span><span class="sxs-lookup"><span data-stu-id="135eb-122"><span id="PHF_VERTEXPROCESSINGSKIPPED"></span><span id="phf_vertexprocessingskipped"></span>**PHF\_VERTEXPROCESSINGSKIPPED**</span></span>  
<span data-ttu-id="135eb-123">Não usado.</span><span class="sxs-lookup"><span data-stu-id="135eb-123">Not used.</span></span>

<span data-ttu-id="135eb-124"><span id="PHF_MODIFYRESOURCE"></span><span id="phf_modifyresource"></span>**PHF \_ MODIFYRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="135eb-124"><span id="PHF_MODIFYRESOURCE"></span><span id="phf_modifyresource"></span>**PHF\_MODIFYRESOURCE**</span></span>  

<span data-ttu-id="135eb-125"><span id="PHF_CANNOTRUNFULLDEPTHSTENCILTEST"></span><span id="phf_cannotrunfulldepthstenciltest"></span>**PHF \_ CANNOTRUNFULLDEPTHSTENCILTEST**</span><span class="sxs-lookup"><span data-stu-id="135eb-125"><span id="PHF_CANNOTRUNFULLDEPTHSTENCILTEST"></span><span id="phf_cannotrunfulldepthstenciltest"></span>**PHF\_CANNOTRUNFULLDEPTHSTENCILTEST**</span></span>  
<span data-ttu-id="135eb-126">Um sinalizador que corresponde a não ser capaz de executar o teste de profundidade ou de estêncil.</span><span class="sxs-lookup"><span data-stu-id="135eb-126">A flag that corresponds to not being able to run the depth or stencil test.</span></span>

## <a name="requirements"></a><span data-ttu-id="135eb-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="135eb-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="135eb-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="135eb-128">Header</span></span></p></td><td><span data-ttu-id="135eb-129">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="135eb-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 




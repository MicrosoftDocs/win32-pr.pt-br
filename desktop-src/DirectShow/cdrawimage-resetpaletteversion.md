---
description: O método ResetPaletteVersion redefine a versão da paleta. Chame esse método se o PIN do filtro de propriedade for reconectado.
ms.assetid: c9e5588c-5501-4356-bdec-a339d33f9eb5
title: Método CDrawImage. ResetPaletteVersion (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.ResetPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a94cd04de428a29308ead8fa33ccfe1792e021a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747390"
---
# <a name="cdrawimageresetpaletteversion-method"></a><span data-ttu-id="4ee3d-104">Método CDrawImage. ResetPaletteVersion</span><span class="sxs-lookup"><span data-stu-id="4ee3d-104">CDrawImage.ResetPaletteVersion method</span></span>

<span data-ttu-id="4ee3d-105">O `ResetPaletteVersion` método redefine a versão da paleta.</span><span class="sxs-lookup"><span data-stu-id="4ee3d-105">The `ResetPaletteVersion` method resets the palette version.</span></span> <span data-ttu-id="4ee3d-106">Chame esse método se o PIN do filtro de propriedade for reconectado.</span><span class="sxs-lookup"><span data-stu-id="4ee3d-106">Call this method if the owning filter's pin reconnects.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ee3d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ee3d-107">Syntax</span></span>


```C++
void ResetPaletteVersion();
```



## <a name="parameters"></a><span data-ttu-id="4ee3d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ee3d-108">Parameters</span></span>

<span data-ttu-id="4ee3d-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4ee3d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4ee3d-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4ee3d-110">Return value</span></span>

<span data-ttu-id="4ee3d-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4ee3d-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ee3d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ee3d-112">Remarks</span></span>

<span data-ttu-id="4ee3d-113">Esse método define o valor de **m \_ PaletteVersion** como uma constante predefinida **, \_ versão da paleta**.</span><span class="sxs-lookup"><span data-stu-id="4ee3d-113">This method sets the value of **m\_PaletteVersion** to a predefined constant, **PALETTE\_VERSION**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ee3d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ee3d-114">Requirements</span></span>



| <span data-ttu-id="4ee3d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ee3d-115">Requirement</span></span> | <span data-ttu-id="4ee3d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="4ee3d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ee3d-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4ee3d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4ee3d-118"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ee3d-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4ee3d-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4ee3d-119">Library</span></span><br/> | <dl> <span data-ttu-id="4ee3d-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4ee3d-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ee3d-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ee3d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ee3d-122">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="4ee3d-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="4ee3d-123">**CDrawImage::GetPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="4ee3d-123">**CDrawImage::GetPaletteVersion**</span></span>](cdrawimage-getpaletteversion.md)
</dt> <dt>

[<span data-ttu-id="4ee3d-124">**CDrawImage::IncrementPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="4ee3d-124">**CDrawImage::IncrementPaletteVersion**</span></span>](cdrawimage-incrementpaletteversion.md)
</dt> </dl>

 

 





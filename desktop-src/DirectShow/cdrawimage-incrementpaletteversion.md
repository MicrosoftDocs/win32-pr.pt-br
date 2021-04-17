---
description: O método IncrementPaletteVersion incrementa a versão da paleta. Chame esse método se o tipo de mídia for alterado para um novo formato palettized.
ms.assetid: 1ce77f97-d225-45f5-a259-1dcca1272d15
title: Método CDrawImage. IncrementPaletteVersion (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.IncrementPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21b4220ec98c5b083913e92f5749866f629a4854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769222"
---
# <a name="cdrawimageincrementpaletteversion-method"></a><span data-ttu-id="40ede-104">Método CDrawImage. IncrementPaletteVersion</span><span class="sxs-lookup"><span data-stu-id="40ede-104">CDrawImage.IncrementPaletteVersion method</span></span>

<span data-ttu-id="40ede-105">O `IncrementPaletteVersion` método incrementa a versão da paleta.</span><span class="sxs-lookup"><span data-stu-id="40ede-105">The `IncrementPaletteVersion` method increments the palette version.</span></span> <span data-ttu-id="40ede-106">Chame esse método se o tipo de mídia for alterado para um novo formato palettized.</span><span class="sxs-lookup"><span data-stu-id="40ede-106">Call this method if the media type changes to a new palettized format.</span></span>

## <a name="syntax"></a><span data-ttu-id="40ede-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40ede-107">Syntax</span></span>


```C++
void IncrementPaletteVersion();
```



## <a name="parameters"></a><span data-ttu-id="40ede-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40ede-108">Parameters</span></span>

<span data-ttu-id="40ede-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="40ede-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="40ede-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="40ede-110">Return value</span></span>

<span data-ttu-id="40ede-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="40ede-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="40ede-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="40ede-112">Remarks</span></span>

<span data-ttu-id="40ede-113">Esse método incrementa o valor da variável de membro **m \_ PaletteVersion** .</span><span class="sxs-lookup"><span data-stu-id="40ede-113">This method increments the value of the **m\_PaletteVersion** member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="40ede-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40ede-114">Requirements</span></span>



| <span data-ttu-id="40ede-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="40ede-115">Requirement</span></span> | <span data-ttu-id="40ede-116">Valor</span><span class="sxs-lookup"><span data-stu-id="40ede-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40ede-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="40ede-117">Header</span></span><br/>  | <dl> <span data-ttu-id="40ede-118"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="40ede-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="40ede-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="40ede-119">Library</span></span><br/> | <dl> <span data-ttu-id="40ede-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="40ede-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40ede-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="40ede-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40ede-122">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="40ede-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="40ede-123">**CDrawImage::GetPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="40ede-123">**CDrawImage::GetPaletteVersion**</span></span>](cdrawimage-getpaletteversion.md)
</dt> <dt>

[<span data-ttu-id="40ede-124">**CDrawImage::ResetPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="40ede-124">**CDrawImage::ResetPaletteVersion**</span></span>](cdrawimage-resetpaletteversion.md)
</dt> </dl>

 

 





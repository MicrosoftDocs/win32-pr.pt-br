---
description: O método GetPaletteVersion recupera a versão atual da paleta.
ms.assetid: 9f97a810-04a4-4ea3-8918-416e9cd8e5e4
title: Método CDrawImage. GetPaletteVersion (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c86f1a0dad8d33913a52962dfe2ec09b7b8244db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754267"
---
# <a name="cdrawimagegetpaletteversion-method"></a><span data-ttu-id="f01a6-103">Método CDrawImage. GetPaletteVersion</span><span class="sxs-lookup"><span data-stu-id="f01a6-103">CDrawImage.GetPaletteVersion method</span></span>

<span data-ttu-id="f01a6-104">O `GetPaletteVersion` método recupera a versão atual da paleta.</span><span class="sxs-lookup"><span data-stu-id="f01a6-104">The `GetPaletteVersion` method retrieves the current palette version.</span></span>

## <a name="syntax"></a><span data-ttu-id="f01a6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f01a6-105">Syntax</span></span>


```C++
LONG GetPaletteVersion();
```



## <a name="parameters"></a><span data-ttu-id="f01a6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f01a6-106">Parameters</span></span>

<span data-ttu-id="f01a6-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f01a6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f01a6-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f01a6-108">Return value</span></span>

<span data-ttu-id="f01a6-109">Retorna o valor da variável de membro **m \_ PaletteVersion** .</span><span class="sxs-lookup"><span data-stu-id="f01a6-109">Returns the value of the **m\_PaletteVersion** member variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="f01a6-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="f01a6-110">Remarks</span></span>

<span data-ttu-id="f01a6-111">O valor retornado por esse método se aplica somente quando o alocador é um objeto [**CImageAllocator**](cimageallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="f01a6-111">The value returned by this method applies only when the allocator is a [**CImageAllocator**](cimageallocator.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="f01a6-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f01a6-112">Requirements</span></span>



| <span data-ttu-id="f01a6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f01a6-113">Requirement</span></span> | <span data-ttu-id="f01a6-114">Valor</span><span class="sxs-lookup"><span data-stu-id="f01a6-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f01a6-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f01a6-115">Header</span></span><br/>  | <dl> <span data-ttu-id="f01a6-116"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f01a6-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f01a6-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f01a6-117">Library</span></span><br/> | <dl> <span data-ttu-id="f01a6-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f01a6-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f01a6-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="f01a6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f01a6-120">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="f01a6-120">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="f01a6-121">**CDrawImage::IncrementPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="f01a6-121">**CDrawImage::IncrementPaletteVersion**</span></span>](cdrawimage-incrementpaletteversion.md)
</dt> <dt>

[<span data-ttu-id="f01a6-122">**CDrawImage::ResetPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="f01a6-122">**CDrawImage::ResetPaletteVersion**</span></span>](cdrawimage-resetpaletteversion.md)
</dt> </dl>

 

 





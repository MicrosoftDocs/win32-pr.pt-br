---
description: O método UsingImageAllocator indica se o alocador atual é um objeto CImageAllocator.
ms.assetid: 842bbcbc-2cc8-4e9d-b6c0-e07f7e472ca1
title: Método CDrawImage. UsingImageAllocator (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.UsingImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a61b4ece94c9c52a0f769a29ec32a26c08b33ee0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752498"
---
# <a name="cdrawimageusingimageallocator-method"></a><span data-ttu-id="71caa-103">Método CDrawImage. UsingImageAllocator</span><span class="sxs-lookup"><span data-stu-id="71caa-103">CDrawImage.UsingImageAllocator method</span></span>

<span data-ttu-id="71caa-104">O `UsingImageAllocator` método indica se o alocador atual é um objeto [**CImageAllocator**](cimageallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="71caa-104">The `UsingImageAllocator` method indicates whether the current allocator is a [**CImageAllocator**](cimageallocator.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="71caa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71caa-105">Syntax</span></span>


```C++
BOOL UsingImageAllocator();
```



## <a name="parameters"></a><span data-ttu-id="71caa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71caa-106">Parameters</span></span>

<span data-ttu-id="71caa-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="71caa-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="71caa-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="71caa-108">Return value</span></span>

<span data-ttu-id="71caa-109">Retornará **true** se o alocador atual for um objeto **CImageAllocator** ou **false** , caso contrário.</span><span class="sxs-lookup"><span data-stu-id="71caa-109">Returns **TRUE** if the current allocator is a **CImageAllocator** object, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="71caa-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71caa-110">Requirements</span></span>



| <span data-ttu-id="71caa-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="71caa-111">Requirement</span></span> | <span data-ttu-id="71caa-112">Valor</span><span class="sxs-lookup"><span data-stu-id="71caa-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71caa-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="71caa-113">Header</span></span><br/>  | <dl> <span data-ttu-id="71caa-114"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71caa-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="71caa-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="71caa-115">Library</span></span><br/> | <dl> <span data-ttu-id="71caa-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="71caa-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71caa-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="71caa-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71caa-118">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="71caa-118">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="71caa-119">**CDrawImage::NotifyAllocator**</span><span class="sxs-lookup"><span data-stu-id="71caa-119">**CDrawImage::NotifyAllocator**</span></span>](cdrawimage-notifyallocator.md)
</dt> </dl>

 

 





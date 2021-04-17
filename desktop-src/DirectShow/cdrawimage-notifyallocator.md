---
description: O método NotifyAllocator informa ao objeto CDrawImage se o alocador da conexão é um objeto CImageAllocator.
ms.assetid: cc1604e7-f755-4a7a-9294-6fd06bb434d4
title: Método CDrawImage. NotifyAllocator (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7bab7d1d00b70317a7cbb0b79f8a430a603a757
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789978"
---
# <a name="cdrawimagenotifyallocator-method"></a><span data-ttu-id="1ee7f-103">Método CDrawImage. NotifyAllocator</span><span class="sxs-lookup"><span data-stu-id="1ee7f-103">CDrawImage.NotifyAllocator method</span></span>

<span data-ttu-id="1ee7f-104">O `NotifyAllocator` método informa ao objeto **CDrawImage** se o alocador da conexão é um objeto [**CImageAllocator**](cimageallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="1ee7f-104">The `NotifyAllocator` method informs the **CDrawImage** object whether the allocator for the connection is a [**CImageAllocator**](cimageallocator.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ee7f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ee7f-105">Syntax</span></span>


```C++
void NotifyAllocator(
   BOOL bUsingImageAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="1ee7f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ee7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ee7f-107">*bUsingImageAllocator*</span><span class="sxs-lookup"><span data-stu-id="1ee7f-107">*bUsingImageAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="1ee7f-108">Valor booliano que indica que tipo de alocador está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="1ee7f-108">Boolean value that indicates what kind of allocator is being used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ee7f-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ee7f-109">Return value</span></span>

<span data-ttu-id="1ee7f-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1ee7f-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ee7f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ee7f-111">Remarks</span></span>

<span data-ttu-id="1ee7f-112">O filtro proprietário deve chamar esse método depois que os Pins concordarem com um alocador.</span><span class="sxs-lookup"><span data-stu-id="1ee7f-112">The owning filter should call this method after the pins agree to an allocator.</span></span> <span data-ttu-id="1ee7f-113">Se o filtro souber que o alocador é um objeto **CImageAllocator** , ele deverá chamar esse método com o valor **true**.</span><span class="sxs-lookup"><span data-stu-id="1ee7f-113">If the filter knows the allocator is a **CImageAllocator** object, it should call this method with the value **TRUE**.</span></span> <span data-ttu-id="1ee7f-114">(Normalmente, o filtro saberá isso somente se ele for proprietário do alocador em questão.) Caso contrário, ele deve chamar esse método com o valor **false**.</span><span class="sxs-lookup"><span data-stu-id="1ee7f-114">(Typically, the filter will know this only if it owns the allocator in question.) Otherwise, it should call this method with the value **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ee7f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ee7f-115">Requirements</span></span>



| <span data-ttu-id="1ee7f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ee7f-116">Requirement</span></span> | <span data-ttu-id="1ee7f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1ee7f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ee7f-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ee7f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1ee7f-119"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ee7f-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1ee7f-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1ee7f-120">Library</span></span><br/> | <dl> <span data-ttu-id="1ee7f-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1ee7f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ee7f-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ee7f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ee7f-123">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="1ee7f-123">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="1ee7f-124">**CDrawImage::D rawImage**</span><span class="sxs-lookup"><span data-stu-id="1ee7f-124">**CDrawImage::DrawImage**</span></span>](cdrawimage-drawimage.md)
</dt> </dl>

 

 





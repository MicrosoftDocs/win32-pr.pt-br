---
description: A \_ variável de membro m bUsingImageAllocator indica se o alocador para a conexão de PIN é um objeto CImageAllocator. Se o valor for TRUE, o alocador será um objeto CImageAllocator (ou derivado dessa classe).
ms.assetid: 8eddcab6-77b9-4c8f-be74-33e91661430d
title: 'Membro CDrawImage:: m_bUsingImageAllocator (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bUsingImageAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e08d1e8217f42c6855759cefeef40e56949156fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756603"
---
# <a name="cdrawimagem_busingimageallocator-member"></a><span data-ttu-id="d952a-104">Membro de CDrawImage:: m \_ bUsingImageAllocator</span><span class="sxs-lookup"><span data-stu-id="d952a-104">CDrawImage::m\_bUsingImageAllocator member</span></span>

<span data-ttu-id="d952a-105">A `m_bUsingImageAllocator` variável de membro indica se o alocador para a conexão de PIN é um objeto **CImageAllocator** .</span><span class="sxs-lookup"><span data-stu-id="d952a-105">The `m_bUsingImageAllocator` member variable indicates whether the allocator for the pin connection is a **CImageAllocator** object.</span></span> <span data-ttu-id="d952a-106">Se o valor for **true**, o alocador será um objeto **CImageAllocator** (ou derivado dessa classe).</span><span class="sxs-lookup"><span data-stu-id="d952a-106">If the value is **TRUE**, the allocator is a **CImageAllocator** object (or is derived from that class).</span></span>

## <a name="syntax"></a><span data-ttu-id="d952a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d952a-107">Syntax</span></span>


```C++
BOOL m_bUsingImageAllocator;
```



## <a name="remarks"></a><span data-ttu-id="d952a-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="d952a-108">Remarks</span></span>

<span data-ttu-id="d952a-109">Quando o valor for **true**, o objeto **CDrawImage** poderá usar as funções **BitBlt** e **StretchBlt** do GDI para renderizar a imagem, em vez das funções de **SetDIBitsToDevice** e **StretchDIBits** mais lentas.</span><span class="sxs-lookup"><span data-stu-id="d952a-109">When the value is **TRUE**, the **CDrawImage** object can use the GDI **BitBlt** and **StretchBlt** functions to render the image, rather than the slower **SetDIBitsToDevice** and **StretchDIBits** functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d952a-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d952a-110">Requirements</span></span>



| <span data-ttu-id="d952a-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="d952a-111">Requirement</span></span> | <span data-ttu-id="d952a-112">Valor</span><span class="sxs-lookup"><span data-stu-id="d952a-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d952a-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d952a-113">Header</span></span><br/>  | <dl> <span data-ttu-id="d952a-114"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d952a-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d952a-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d952a-115">Library</span></span><br/> | <dl> <span data-ttu-id="d952a-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d952a-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d952a-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="d952a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d952a-118">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="d952a-118">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="d952a-119">**CDrawImage::NotifyAllocator**</span><span class="sxs-lookup"><span data-stu-id="d952a-119">**CDrawImage::NotifyAllocator**</span></span>](cdrawimage-notifyallocator.md)
</dt> <dt>

[<span data-ttu-id="d952a-120">**CDrawImage::UsingImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="d952a-120">**CDrawImage::UsingImageAllocator**</span></span>](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 





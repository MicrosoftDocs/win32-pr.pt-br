---
description: Sinalizador que indica se os requisitos de buffer foram alterados.
ms.assetid: 34d946f9-125c-40fb-b09e-82457add07d6
title: 'Membro CBaseAllocator:: m_bChanged (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 86c700f3c0ee820206613bcf3147652b1826b57a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768410"
---
# <a name="cbaseallocatorm_bchanged-member"></a><span data-ttu-id="5a669-103">Membro de CBaseAllocator:: m \_ bChanged</span><span class="sxs-lookup"><span data-stu-id="5a669-103">CBaseAllocator::m\_bChanged member</span></span>

<span data-ttu-id="5a669-104">Sinalizador que indica se os requisitos de buffer foram alterados.</span><span class="sxs-lookup"><span data-stu-id="5a669-104">Flag indicating whether the buffer requirements have changed.</span></span> <span data-ttu-id="5a669-105">O método [**CBaseAllocator:: SetProperties**](cbaseallocator-setproperties.md) define o valor como **true**.</span><span class="sxs-lookup"><span data-stu-id="5a669-105">The [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method sets the value to **TRUE**.</span></span> <span data-ttu-id="5a669-106">Em uma classe derivada, o método virtual puro [**CBaseAllocator:: Alloc**](cbaseallocator-alloc.md) deve definir o valor de volta como **false**.</span><span class="sxs-lookup"><span data-stu-id="5a669-106">In a derived class, the pure virtual method [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md) should set the value back to **FALSE**.</span></span> <span data-ttu-id="5a669-107">Depois que os buffers forem alocados, não será necessário realocá-los enquanto *m \_ BChanged* for **false**.</span><span class="sxs-lookup"><span data-stu-id="5a669-107">Once buffers have been allocated, there is no need to re-allocate them while *m\_bChanged* is **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a669-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a669-108">Syntax</span></span>


```C++
BOOL m_bChanged;
```



## <a name="requirements"></a><span data-ttu-id="5a669-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a669-109">Requirements</span></span>



| <span data-ttu-id="5a669-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a669-110">Requirement</span></span> | <span data-ttu-id="5a669-111">Valor</span><span class="sxs-lookup"><span data-stu-id="5a669-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a669-112">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5a669-112">Header</span></span><br/>  | <dl> <span data-ttu-id="5a669-113"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5a669-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5a669-114">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5a669-114">Library</span></span><br/> | <dl> <span data-ttu-id="5a669-115"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5a669-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a669-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a669-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a669-117">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="5a669-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 





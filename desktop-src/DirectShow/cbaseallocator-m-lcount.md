---
description: Número de buffers a serem fornecidos.
ms.assetid: 73f87b14-4346-4909-bd1e-c4981cde403d
title: 'Membro CBaseAllocator:: m_lCount (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16ab469db1d50007bd3aa55ab692c51aa7600452
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749052"
---
# <a name="cbaseallocatorm_lcount-member"></a><span data-ttu-id="000c0-103">Membro de CBaseAllocator:: m \_ lCount</span><span class="sxs-lookup"><span data-stu-id="000c0-103">CBaseAllocator::m\_lCount member</span></span>

<span data-ttu-id="000c0-104">Número de buffers a serem fornecidos.</span><span class="sxs-lookup"><span data-stu-id="000c0-104">Number of buffers to provide.</span></span> <span data-ttu-id="000c0-105">O método [**CBaseAllocator:: SetProperties**](cbaseallocator-setproperties.md) define esse valor.</span><span class="sxs-lookup"><span data-stu-id="000c0-105">The [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method sets this value.</span></span> <span data-ttu-id="000c0-106">Os buffers não são alocados até que o método [**CBaseAllocator:: Commit**](cbaseallocator-commit.md) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="000c0-106">The buffers are not allocated until the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method is called.</span></span> <span data-ttu-id="000c0-107">O número atual de buffers alocados é especificado pela variável de membro [**CBaseAllocator:: m \_ lAllocated**](cbaseallocator-m-lallocated.md) .</span><span class="sxs-lookup"><span data-stu-id="000c0-107">The current number of allocated buffers is specified by the [**CBaseAllocator::m\_lAllocated**](cbaseallocator-m-lallocated.md) member variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="000c0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="000c0-108">Syntax</span></span>


```C++
long m_lCount;
```



## <a name="requirements"></a><span data-ttu-id="000c0-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="000c0-109">Requirements</span></span>



| <span data-ttu-id="000c0-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="000c0-110">Requirement</span></span> | <span data-ttu-id="000c0-111">Valor</span><span class="sxs-lookup"><span data-stu-id="000c0-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="000c0-112">parâmetro</span><span class="sxs-lookup"><span data-stu-id="000c0-112">Header</span></span><br/>  | <dl> <span data-ttu-id="000c0-113"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="000c0-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="000c0-114">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="000c0-114">Library</span></span><br/> | <dl> <span data-ttu-id="000c0-115"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="000c0-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="000c0-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="000c0-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="000c0-117">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="000c0-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 





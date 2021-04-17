---
description: Sinalizador que indica se uma operação de desconfirmação está em andamento.
ms.assetid: aa008be1-8faa-4dc1-9641-37dcc59ce6c7
title: 'Membro CBaseAllocator:: m_bDecommitInProgress (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDecommitInProgress
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27aaf2766f67ebb77250522346cfe5c76acdf6d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755367"
---
# <a name="cbaseallocatorm_bdecommitinprogress-member"></a><span data-ttu-id="b58ca-103">Membro de CBaseAllocator:: m \_ bDecommitInProgress</span><span class="sxs-lookup"><span data-stu-id="b58ca-103">CBaseAllocator::m\_bDecommitInProgress member</span></span>

<span data-ttu-id="b58ca-104">Sinalizador que indica se uma operação de desconfirmação está em andamento.</span><span class="sxs-lookup"><span data-stu-id="b58ca-104">Flag indicating whether a decommit operation is in progress.</span></span> <span data-ttu-id="b58ca-105">O valor é **true** após o método [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) ser chamado, mas antes de todos os buffers terem sido liberados.</span><span class="sxs-lookup"><span data-stu-id="b58ca-105">The value is **TRUE** after the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method is called, but before all the buffers have been released.</span></span> <span data-ttu-id="b58ca-106">Se o valor for **true**, o método [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md) falhará.</span><span class="sxs-lookup"><span data-stu-id="b58ca-106">If the value is **TRUE**, the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method fails.</span></span> <span data-ttu-id="b58ca-107">Além disso, o alocador não deve ser excluído a si mesmo enquanto o valor é **true**.</span><span class="sxs-lookup"><span data-stu-id="b58ca-107">Also, the allocator should not deleted itself while the value is **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b58ca-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b58ca-108">Syntax</span></span>


```C++
BOOL m_bDecommitInProgress;
```



## <a name="requirements"></a><span data-ttu-id="b58ca-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b58ca-109">Requirements</span></span>



| <span data-ttu-id="b58ca-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="b58ca-110">Requirement</span></span> | <span data-ttu-id="b58ca-111">Valor</span><span class="sxs-lookup"><span data-stu-id="b58ca-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b58ca-112">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b58ca-112">Header</span></span><br/>  | <dl> <span data-ttu-id="b58ca-113"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b58ca-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b58ca-114">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b58ca-114">Library</span></span><br/> | <dl> <span data-ttu-id="b58ca-115"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b58ca-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b58ca-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="b58ca-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b58ca-117">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="b58ca-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 





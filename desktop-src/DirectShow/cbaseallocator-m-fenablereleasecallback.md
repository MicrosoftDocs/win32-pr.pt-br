---
description: 'Sinalizador que indica se o retorno de chamada de versão está habilitado. Esse sinalizador é definido no método do construtor. Se o valor for FALSE, chamar o método CBaseAllocator:: setnotificar fará com que uma asserção seja acionada (em compilações de depuração).'
ms.assetid: cc9adc7c-ec44-41e7-875a-b3e553120804
title: 'Membro CBaseAllocator:: m_fEnableReleaseCallback (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fEnableReleaseCallback
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 626f1e8f4101eb48e79bc1cf679d1b91be9b2b31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768409"
---
# <a name="cbaseallocatorm_fenablereleasecallback-member"></a><span data-ttu-id="3ede8-105">Membro de CBaseAllocator:: m \_ fEnableReleaseCallback</span><span class="sxs-lookup"><span data-stu-id="3ede8-105">CBaseAllocator::m\_fEnableReleaseCallback member</span></span>

<span data-ttu-id="3ede8-106">Sinalizador que indica se o retorno de chamada de versão está habilitado.</span><span class="sxs-lookup"><span data-stu-id="3ede8-106">Flag indicating whether the release callback is enabled.</span></span> <span data-ttu-id="3ede8-107">Esse sinalizador é definido no método do construtor.</span><span class="sxs-lookup"><span data-stu-id="3ede8-107">This flag is set in the constructor method.</span></span> <span data-ttu-id="3ede8-108">Se o valor for **false**, chamar o método [**CBaseAllocator:: setnotificar**](cbaseallocator-setnotify.md) fará com que uma asserção seja acionada (em compilações de depuração).</span><span class="sxs-lookup"><span data-stu-id="3ede8-108">If the value is **FALSE**, calling the [**CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) method causes an assertion to fire (in debug builds).</span></span>

## <a name="syntax"></a><span data-ttu-id="3ede8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ede8-109">Syntax</span></span>


```C++
BOOL m_fEnableReleaseCallback;
```



## <a name="requirements"></a><span data-ttu-id="3ede8-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ede8-110">Requirements</span></span>



| <span data-ttu-id="3ede8-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ede8-111">Requirement</span></span> | <span data-ttu-id="3ede8-112">Valor</span><span class="sxs-lookup"><span data-stu-id="3ede8-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ede8-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3ede8-113">Header</span></span><br/>  | <dl> <span data-ttu-id="3ede8-114"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3ede8-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3ede8-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3ede8-115">Library</span></span><br/> | <dl> <span data-ttu-id="3ede8-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3ede8-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ede8-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ede8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ede8-118">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="3ede8-118">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 





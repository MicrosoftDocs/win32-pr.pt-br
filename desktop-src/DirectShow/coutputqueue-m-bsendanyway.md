---
description: 'Sinalizador para substituir o processamento em lotes. Definir esse sinalizador como TRUE substitui o sinalizador COutputQueue:: m \_ bBatchExact e entrega todas as amostras pendentes.'
ms.assetid: 95ea6973-65c0-40c9-be22-c2a20a60b459
title: 'Membro COutputQueue:: m_bSendAnyway (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bSendAnyway
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57019ee8844f73fdb6cf6e7943e7e22f72d2c98b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755586"
---
# <a name="coutputqueuem_bsendanyway-member"></a><span data-ttu-id="06225-104">Membro de COutputQueue:: m \_ bSendAnyway</span><span class="sxs-lookup"><span data-stu-id="06225-104">COutputQueue::m\_bSendAnyway member</span></span>

<span data-ttu-id="06225-105">Sinalizador para substituir o processamento em lotes.</span><span class="sxs-lookup"><span data-stu-id="06225-105">Flag to override batch processing.</span></span> <span data-ttu-id="06225-106">Definir esse sinalizador como **true** substitui o sinalizador [**COutputQueue:: m \_ bBatchExact**](coutputqueue-m-bbatchexact.md) e entrega todas as amostras pendentes.</span><span class="sxs-lookup"><span data-stu-id="06225-106">Setting this flag to **TRUE** overrides the [**COutputQueue::m\_bBatchExact**](coutputqueue-m-bbatchexact.md) flag and delivers all pending samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="06225-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="06225-107">Syntax</span></span>


```C++
BOOL m_bSendAnyway;
```



## <a name="requirements"></a><span data-ttu-id="06225-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06225-108">Requirements</span></span>



| <span data-ttu-id="06225-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="06225-109">Requirement</span></span> | <span data-ttu-id="06225-110">Valor</span><span class="sxs-lookup"><span data-stu-id="06225-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06225-111">parâmetro</span><span class="sxs-lookup"><span data-stu-id="06225-111">Header</span></span><br/>  | <dl> <span data-ttu-id="06225-112"><dt>Outputq. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06225-112"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="06225-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="06225-113">Library</span></span><br/> | <dl> <span data-ttu-id="06225-114"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="06225-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06225-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="06225-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06225-116">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="06225-116">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 





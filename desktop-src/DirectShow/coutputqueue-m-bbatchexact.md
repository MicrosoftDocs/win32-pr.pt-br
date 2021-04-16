---
description: Sinalizador que especifica se o objeto fornece amostras em lotes exatos.
ms.assetid: 1a37c78f-4499-4ebb-92b4-b71ba3ff1a02
title: 'Membro COutputQueue:: m_bBatchExact (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bBatchExact
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5f38d8a0e7335025688f52015ff9ed4d4892820
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750470"
---
# <a name="coutputqueuem_bbatchexact-member"></a><span data-ttu-id="9fef3-103">Membro de COutputQueue:: m \_ bBatchExact</span><span class="sxs-lookup"><span data-stu-id="9fef3-103">COutputQueue::m\_bBatchExact member</span></span>

<span data-ttu-id="9fef3-104">Sinalizador que especifica se o objeto fornece amostras em lotes exatos.</span><span class="sxs-lookup"><span data-stu-id="9fef3-104">Flag that specifies whether the object delivers samples in exact batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fef3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9fef3-105">Syntax</span></span>


```C++
const BOOL m_bBatchExact;
```



## <a name="remarks"></a><span data-ttu-id="9fef3-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="9fef3-106">Remarks</span></span>

<span data-ttu-id="9fef3-107">Se o valor for **true**, o objeto aguardará até que ele tenha um lote completo de amostras de mídia antes de entregar qualquer.</span><span class="sxs-lookup"><span data-stu-id="9fef3-107">If the value is **TRUE**, the object waits until it has a complete batch of media samples before delivering any.</span></span> <span data-ttu-id="9fef3-108">Caso contrário, ele fornece exemplos à medida que eles chegam.</span><span class="sxs-lookup"><span data-stu-id="9fef3-108">Otherwise, it delivers samples as they arrive.</span></span> <span data-ttu-id="9fef3-109">A variável de membro [**COutputQueue:: m \_ lBatchSize**](coutputqueue-m-lbatchsize.md) define o tamanho do lote.</span><span class="sxs-lookup"><span data-stu-id="9fef3-109">The [**COutputQueue::m\_lBatchSize**](coutputqueue-m-lbatchsize.md) member variable defines the batch size.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fef3-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fef3-110">Requirements</span></span>



| <span data-ttu-id="9fef3-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fef3-111">Requirement</span></span> | <span data-ttu-id="9fef3-112">Valor</span><span class="sxs-lookup"><span data-stu-id="9fef3-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fef3-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9fef3-113">Header</span></span><br/>  | <dl> <span data-ttu-id="9fef3-114"><dt>Outputq. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9fef3-114"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9fef3-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9fef3-115">Library</span></span><br/> | <dl> <span data-ttu-id="9fef3-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="9fef3-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fef3-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="9fef3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fef3-118">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="9fef3-118">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 





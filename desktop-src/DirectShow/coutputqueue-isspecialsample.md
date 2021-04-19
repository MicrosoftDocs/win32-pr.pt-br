---
description: O método IsSpecialSample determina se os dados em fila são uma mensagem de controle.
ms.assetid: 33d9c7a2-3046-45a5-a9f5-8f33a03bbcdd
title: Método COutputQueue. IsSpecialSample (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsSpecialSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc57847d6a977c740bbf50bae220a89b0ed6fab1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811322"
---
# <a name="coutputqueueisspecialsample-method"></a><span data-ttu-id="4c00b-103">Método COutputQueue. IsSpecialSample</span><span class="sxs-lookup"><span data-stu-id="4c00b-103">COutputQueue.IsSpecialSample method</span></span>

<span data-ttu-id="4c00b-104">O `IsSpecialSample` método determina se os dados em fila são uma mensagem de controle.</span><span class="sxs-lookup"><span data-stu-id="4c00b-104">The `IsSpecialSample` method determines whether queued data is a control message.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c00b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c00b-105">Syntax</span></span>


```C++
BOOL IsSpecialSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="4c00b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c00b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c00b-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="4c00b-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="4c00b-108">Ponteiro para um item na fila.</span><span class="sxs-lookup"><span data-stu-id="4c00b-108">Pointer to an item in the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c00b-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4c00b-109">Return value</span></span>

<span data-ttu-id="4c00b-110">Retornará **true** se *pSample* for uma mensagem de controle ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="4c00b-110">Returns **TRUE** if *pSample* is a control message, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c00b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c00b-111">Remarks</span></span>

<span data-ttu-id="4c00b-112">O método [**COutputQueue:: QueueSample**](coutputqueue-queuesample.md) pode receber mensagens de controle além dos exemplos de mídia.</span><span class="sxs-lookup"><span data-stu-id="4c00b-112">The [**COutputQueue::QueueSample**](coutputqueue-queuesample.md) method can receive control messages in addition to media samples.</span></span> <span data-ttu-id="4c00b-113">Uma mensagem de controle é uma constante definida (conversão para um \_ tipo PTR longo) que instrui o thread a executar uma ação.</span><span class="sxs-lookup"><span data-stu-id="4c00b-113">A control message is a defined constant (cast to a LONG\_PTR type) that instructs the thread to perform an action.</span></span> <span data-ttu-id="4c00b-114">As mensagens de controle não contêm dados de mídia.</span><span class="sxs-lookup"><span data-stu-id="4c00b-114">Control messages do not contain media data.</span></span> <span data-ttu-id="4c00b-115">Para obter mais informações, consulte **COutputQueue:: QueueSample**.</span><span class="sxs-lookup"><span data-stu-id="4c00b-115">For more information, see **COutputQueue::QueueSample**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c00b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c00b-116">Requirements</span></span>



| <span data-ttu-id="4c00b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c00b-117">Requirement</span></span> | <span data-ttu-id="4c00b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4c00b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c00b-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4c00b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4c00b-120"><dt>Outputq. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4c00b-120"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4c00b-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4c00b-121">Library</span></span><br/> | <dl> <span data-ttu-id="4c00b-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4c00b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c00b-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c00b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c00b-124">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="4c00b-124">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 





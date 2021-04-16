---
description: O método SendAnyway entrega quaisquer exemplos pendentes.
ms.assetid: b4e3a0c6-0f72-4a00-963e-65ceed265f01
title: Método COutputQueue. SendAnyway (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SendAnyway
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6fa5495371e020310e2367aea7e7bed9ef113f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779549"
---
# <a name="coutputqueuesendanyway-method"></a><span data-ttu-id="9f02f-103">Método COutputQueue. SendAnyway</span><span class="sxs-lookup"><span data-stu-id="9f02f-103">COutputQueue.SendAnyway method</span></span>

<span data-ttu-id="9f02f-104">O `SendAnyway` método entrega quaisquer exemplos pendentes.</span><span class="sxs-lookup"><span data-stu-id="9f02f-104">The `SendAnyway` method delivers any pending samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f02f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f02f-105">Syntax</span></span>


```C++
void SendAnyway();
```



## <a name="parameters"></a><span data-ttu-id="9f02f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f02f-106">Parameters</span></span>

<span data-ttu-id="9f02f-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9f02f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9f02f-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9f02f-108">Return value</span></span>

<span data-ttu-id="9f02f-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9f02f-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f02f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f02f-110">Remarks</span></span>

<span data-ttu-id="9f02f-111">Se a variável de membro [**COutputQueue:: m \_ BBatchExact**](coutputqueue-m-bbatchexact.md) for **true**, o objeto preencherá a matriz [**COutputQueue:: m \_ ppSamples**](coutputqueue-m-ppsamples.md) antes de fornecer um lote de amostras.</span><span class="sxs-lookup"><span data-stu-id="9f02f-111">If the [**COutputQueue::m\_bBatchExact**](coutputqueue-m-bbatchexact.md) member variable is **TRUE**, the object fills the [**COutputQueue::m\_ppSamples**](coutputqueue-m-ppsamples.md) array before it delivers a batch of samples.</span></span> <span data-ttu-id="9f02f-112">Chame esse método para entregar um lote parcial.</span><span class="sxs-lookup"><span data-stu-id="9f02f-112">Call this method to deliver a partial batch.</span></span> <span data-ttu-id="9f02f-113">Por exemplo, o método [**COutputQueue:: EOS**](coutputqueue-eos.md) chama `SendAnyway` para serializar mensagens de fim de fluxo.</span><span class="sxs-lookup"><span data-stu-id="9f02f-113">For example, the [**COutputQueue::EOS**](coutputqueue-eos.md) method calls `SendAnyway` to serialize end-of-stream messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f02f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f02f-114">Requirements</span></span>



| <span data-ttu-id="9f02f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f02f-115">Requirement</span></span> | <span data-ttu-id="9f02f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="9f02f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f02f-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9f02f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="9f02f-118"><dt>Outputq. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f02f-118"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9f02f-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9f02f-119">Library</span></span><br/> | <dl> <span data-ttu-id="9f02f-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="9f02f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f02f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f02f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f02f-122">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="9f02f-122">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 





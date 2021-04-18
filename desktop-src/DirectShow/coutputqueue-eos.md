---
description: O método EOS fornece uma chamada de fim de fluxo para o pino de entrada.
ms.assetid: 65e8db14-6ca8-4c4f-8bd8-2442f743499e
title: Método COutputQueue. EOS (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab05d4ab3f2620c11bd62d566be851e16b28cecd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785359"
---
# <a name="coutputqueueeos-method"></a><span data-ttu-id="4a993-103">Método COutputQueue. EOS</span><span class="sxs-lookup"><span data-stu-id="4a993-103">COutputQueue.EOS method</span></span>

<span data-ttu-id="4a993-104">O `EOS` método fornece uma chamada de fim de fluxo para o pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="4a993-104">The `EOS` method delivers an end-of-stream call to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a993-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a993-105">Syntax</span></span>


```C++
void EOS();
```



## <a name="parameters"></a><span data-ttu-id="4a993-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a993-106">Parameters</span></span>

<span data-ttu-id="4a993-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4a993-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4a993-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4a993-108">Return value</span></span>

<span data-ttu-id="4a993-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4a993-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a993-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a993-110">Remarks</span></span>

<span data-ttu-id="4a993-111">Se o objeto estiver usando um thread, ele enfileira uma mensagem de \_ controle de pacote EOS.</span><span class="sxs-lookup"><span data-stu-id="4a993-111">If the object is using a thread, it queues an EOS\_PACKET control message.</span></span> <span data-ttu-id="4a993-112">O thread entrega quaisquer exemplos pendentes e chama o método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) no pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="4a993-112">The thread delivers any pending samples and calls the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method on the input pin.</span></span>

<span data-ttu-id="4a993-113">Se o objeto não estiver usando um thread, ele chamará o método [**COutputQueue:: SendAnyway**](coutputqueue-sendanyway.md) para entregar quaisquer exemplos pendentes.</span><span class="sxs-lookup"><span data-stu-id="4a993-113">If the object is not using a thread, it calls the [**COutputQueue::SendAnyway**](coutputqueue-sendanyway.md) method to deliver any pending samples.</span></span> <span data-ttu-id="4a993-114">Em seguida, ele chama **IPin:: EndOfStream** no pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="4a993-114">Then it calls **IPin::EndOfStream** on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a993-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a993-115">Requirements</span></span>



| <span data-ttu-id="4a993-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a993-116">Requirement</span></span> | <span data-ttu-id="4a993-117">Valor</span><span class="sxs-lookup"><span data-stu-id="4a993-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a993-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4a993-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4a993-119"><dt>Outputq. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a993-119"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4a993-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4a993-120">Library</span></span><br/> | <dl> <span data-ttu-id="4a993-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4a993-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a993-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a993-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a993-123">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="4a993-123">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 





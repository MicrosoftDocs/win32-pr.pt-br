---
description: O método ReceiveMultiple entrega um lote de amostras de mídia para o pino de entrada.
ms.assetid: e9c7d6ed-fbf9-4c90-8e1e-3bad66cb5d4f
title: Método COutputQueue. ReceiveMultiple (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e17e0a8a4856b067907622ec3c8437f5e73a7e38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766320"
---
# <a name="coutputqueuereceivemultiple-method"></a><span data-ttu-id="b73b6-103">Método COutputQueue. ReceiveMultiple</span><span class="sxs-lookup"><span data-stu-id="b73b6-103">COutputQueue.ReceiveMultiple method</span></span>

<span data-ttu-id="b73b6-104">O `ReceiveMultiple` método entrega um lote de amostras de mídia para o pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="b73b6-104">The `ReceiveMultiple` method delivers a batch of media samples to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="b73b6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b73b6-105">Syntax</span></span>


```C++
HRESULT ReceiveMultiple(
   IMediaSample **ppSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a><span data-ttu-id="b73b6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b73b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b73b6-107">*ppSamples*</span><span class="sxs-lookup"><span data-stu-id="b73b6-107">*ppSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="b73b6-108">Endereço de um ponteiro para uma matriz de amostras.</span><span class="sxs-lookup"><span data-stu-id="b73b6-108">Address of a pointer to an array of samples.</span></span>

</dd> <dt>

<span data-ttu-id="b73b6-109">*nSamples*</span><span class="sxs-lookup"><span data-stu-id="b73b6-109">*nSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="b73b6-110">Número de amostras na matriz.</span><span class="sxs-lookup"><span data-stu-id="b73b6-110">Number of samples in the array.</span></span>

</dd> <dt>

<span data-ttu-id="b73b6-111">*nSamplesProcessed*</span><span class="sxs-lookup"><span data-stu-id="b73b6-111">*nSamplesProcessed*</span></span> 
</dt> <dd>

<span data-ttu-id="b73b6-112">Ponteiro para uma variável que recebe o número de amostras entregues com êxito.</span><span class="sxs-lookup"><span data-stu-id="b73b6-112">Pointer to a variable that receives the number of samples delivered successfully.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b73b6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b73b6-113">Return value</span></span>

<span data-ttu-id="b73b6-114">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b73b6-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b73b6-115">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b73b6-115">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="b73b6-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b73b6-116">Return code</span></span>                                                                             | <span data-ttu-id="b73b6-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="b73b6-117">Description</span></span>                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b73b6-118"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="b73b6-118"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="b73b6-119">Notificação de fim de fluxo recebida antes do processamento deste exemplo.</span><span class="sxs-lookup"><span data-stu-id="b73b6-119">End-of-stream notification received before processing this sample.</span></span><br/> |
| <dl> <span data-ttu-id="b73b6-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b73b6-120"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="b73b6-121">Êxito.</span><span class="sxs-lookup"><span data-stu-id="b73b6-121">Success.</span></span><br/>                                                           |



 

## <a name="remarks"></a><span data-ttu-id="b73b6-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="b73b6-122">Remarks</span></span>

<span data-ttu-id="b73b6-123">Se o objeto estiver usando um thread, esse método enfileirará todos os exemplos passados na matriz.</span><span class="sxs-lookup"><span data-stu-id="b73b6-123">If the object is using a thread, this method queues all of the samples passed in the array.</span></span> <span data-ttu-id="b73b6-124">Caso contrário, o método chama o método [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) no pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="b73b6-124">Otherwise, the method calls the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="b73b6-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b73b6-125">Requirements</span></span>



| <span data-ttu-id="b73b6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b73b6-126">Requirement</span></span> | <span data-ttu-id="b73b6-127">Valor</span><span class="sxs-lookup"><span data-stu-id="b73b6-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b73b6-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b73b6-128">Header</span></span><br/>  | <dl> <span data-ttu-id="b73b6-129"><dt>Outputq. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b73b6-129"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b73b6-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b73b6-130">Library</span></span><br/> | <dl> <span data-ttu-id="b73b6-131"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b73b6-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b73b6-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="b73b6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b73b6-133">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="b73b6-133">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 





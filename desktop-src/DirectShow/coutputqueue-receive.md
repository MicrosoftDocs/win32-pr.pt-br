---
description: O método Receive fornece um exemplo de mídia para o pino de entrada.
ms.assetid: a8ee0988-8955-48d0-be1b-24eea72d560d
title: Método COutputQueue. Receive (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ce8a0d44730fa35b38cf6d738edd26168284a46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770279"
---
# <a name="coutputqueuereceive-method"></a><span data-ttu-id="ab1cf-103">Método COutputQueue. Receive</span><span class="sxs-lookup"><span data-stu-id="ab1cf-103">COutputQueue.Receive method</span></span>

<span data-ttu-id="ab1cf-104">O `Receive` método entrega um exemplo de mídia para o pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="ab1cf-104">The `Receive` method delivers a media sample to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab1cf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab1cf-105">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="ab1cf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab1cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab1cf-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="ab1cf-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="ab1cf-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.</span><span class="sxs-lookup"><span data-stu-id="ab1cf-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab1cf-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ab1cf-109">Return value</span></span>

<span data-ttu-id="ab1cf-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ab1cf-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ab1cf-111">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ab1cf-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="ab1cf-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ab1cf-112">Return code</span></span>                                                                             | <span data-ttu-id="ab1cf-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab1cf-113">Description</span></span>                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ab1cf-114"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="ab1cf-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="ab1cf-115">Notificação de fim de fluxo recebida antes do processamento deste exemplo.</span><span class="sxs-lookup"><span data-stu-id="ab1cf-115">End-of-stream notification received before processing this sample.</span></span><br/> |
| <dl> <span data-ttu-id="ab1cf-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ab1cf-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="ab1cf-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="ab1cf-117">Success.</span></span><br/>                                                           |



 

## <a name="remarks"></a><span data-ttu-id="ab1cf-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab1cf-118">Remarks</span></span>

<span data-ttu-id="ab1cf-119">Esse método chama o método [**COutputQueue:: ReceiveMultiple**](coutputqueue-receivemultiple.md) .</span><span class="sxs-lookup"><span data-stu-id="ab1cf-119">This method calls the [**COutputQueue::ReceiveMultiple**](coutputqueue-receivemultiple.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab1cf-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab1cf-120">Requirements</span></span>



| <span data-ttu-id="ab1cf-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab1cf-121">Requirement</span></span> | <span data-ttu-id="ab1cf-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ab1cf-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab1cf-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ab1cf-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ab1cf-124"><dt>Outputq. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab1cf-124"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ab1cf-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab1cf-125">Library</span></span><br/> | <dl> <span data-ttu-id="ab1cf-126"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ab1cf-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab1cf-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab1cf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab1cf-128">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="ab1cf-128">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 





---
description: O método Reply responde a uma solicitação.
ms.assetid: 90e91b99-6a1c-46a2-b83d-eba483f1832a
title: Método CAMThread. Reply (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Reply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e86e0bc0155e527aa11c26531ae5608e6828362
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812996"
---
# <a name="camthreadreply-method"></a><span data-ttu-id="d002f-103">Método CAMThread. Reply</span><span class="sxs-lookup"><span data-stu-id="d002f-103">CAMThread.Reply method</span></span>

<span data-ttu-id="d002f-104">O `Reply` método responde a uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="d002f-104">The `Reply` method replies to a request.</span></span>

## <a name="syntax"></a><span data-ttu-id="d002f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d002f-105">Syntax</span></span>


```C++
void Reply(
   DWORD dw
);
```



## <a name="parameters"></a><span data-ttu-id="d002f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d002f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d002f-107">*dw*</span><span class="sxs-lookup"><span data-stu-id="d002f-107">*dw*</span></span> 
</dt> <dd>

<span data-ttu-id="d002f-108">Valor a ser retornado no método [**CAMThread:: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="d002f-108">Value to return in the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d002f-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d002f-109">Return value</span></span>

<span data-ttu-id="d002f-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d002f-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d002f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d002f-111">Remarks</span></span>

<span data-ttu-id="d002f-112">O método CallWorker é bloqueado até que esse método seja chamado.</span><span class="sxs-lookup"><span data-stu-id="d002f-112">The CallWorker method blocks until this method is called.</span></span> <span data-ttu-id="d002f-113">O parâmetro *DW* fornece o valor de retorno para CallWorker.</span><span class="sxs-lookup"><span data-stu-id="d002f-113">The *dw* parameter supplies the return value for CallWorker.</span></span> <span data-ttu-id="d002f-114">Chame esse método em seu procedimento de thread depois de recuperar uma solicitação, para liberar o thread solicitante.</span><span class="sxs-lookup"><span data-stu-id="d002f-114">Call this method in your thread procedure after you retrieve a request, to release the requesting thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="d002f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d002f-115">Requirements</span></span>



| <span data-ttu-id="d002f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d002f-116">Requirement</span></span> | <span data-ttu-id="d002f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d002f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d002f-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d002f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d002f-119"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d002f-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d002f-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d002f-120">Library</span></span><br/> | <dl> <span data-ttu-id="d002f-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d002f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d002f-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="d002f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d002f-123">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="d002f-123">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 





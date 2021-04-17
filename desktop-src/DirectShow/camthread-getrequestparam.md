---
description: O método GetRequestParam recupera a solicitação mais recente.
ms.assetid: f5bf4935-29ea-45b9-a57e-9fdcd9cde20a
title: Método CAMThread. GetRequestParam (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestParam
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2dd6584123663bb36f1db4771fb3f86d7ac4f5cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780064"
---
# <a name="camthreadgetrequestparam-method"></a><span data-ttu-id="d70ce-103">Método CAMThread. GetRequestParam</span><span class="sxs-lookup"><span data-stu-id="d70ce-103">CAMThread.GetRequestParam method</span></span>

<span data-ttu-id="d70ce-104">O `GetRequestParam` método recupera a solicitação mais recente.</span><span class="sxs-lookup"><span data-stu-id="d70ce-104">The `GetRequestParam` method retrieves the latest request.</span></span>

## <a name="syntax"></a><span data-ttu-id="d70ce-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d70ce-105">Syntax</span></span>


```C++
DWORD GetRequestParam() const;
```



## <a name="parameters"></a><span data-ttu-id="d70ce-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d70ce-106">Parameters</span></span>

<span data-ttu-id="d70ce-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d70ce-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d70ce-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d70ce-108">Return value</span></span>

<span data-ttu-id="d70ce-109">Retorna o valor do parâmetro que foi passado mais recentemente para o método [**CAMThread:: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="d70ce-109">Returns the value of the parameter that was passed most recently to the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d70ce-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d70ce-110">Requirements</span></span>



| <span data-ttu-id="d70ce-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="d70ce-111">Requirement</span></span> | <span data-ttu-id="d70ce-112">Valor</span><span class="sxs-lookup"><span data-stu-id="d70ce-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d70ce-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d70ce-113">Header</span></span><br/>  | <dl> <span data-ttu-id="d70ce-114"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d70ce-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d70ce-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d70ce-115">Library</span></span><br/> | <dl> <span data-ttu-id="d70ce-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d70ce-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d70ce-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="d70ce-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d70ce-118">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="d70ce-118">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 





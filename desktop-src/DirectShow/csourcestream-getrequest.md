---
description: O método GetRequest aguarda a próxima solicitação de thread.
ms.assetid: 2938374b-174f-4276-98a2-20a084bd9bbd
title: Método CSourceStream. GetRequest (origem. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.GetRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f45e6f6cf269f7aca6741d8e1c150c7054b07f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748802"
---
# <a name="csourcestreamgetrequest-method"></a><span data-ttu-id="ec466-103">Método CSourceStream. GetRequest</span><span class="sxs-lookup"><span data-stu-id="ec466-103">CSourceStream.GetRequest method</span></span>

<span data-ttu-id="ec466-104">O `GetRequest` método aguarda a próxima solicitação de thread.</span><span class="sxs-lookup"><span data-stu-id="ec466-104">The `GetRequest` method waits for the next thread request.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec466-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec466-105">Syntax</span></span>


```C++
Command GetRequest();
```



## <a name="parameters"></a><span data-ttu-id="ec466-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec466-106">Parameters</span></span>

<span data-ttu-id="ec466-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ec466-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ec466-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ec466-108">Return value</span></span>

<span data-ttu-id="ec466-109">Retorna a próxima solicitação de thread.</span><span class="sxs-lookup"><span data-stu-id="ec466-109">Returns the next thread request.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec466-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec466-110">Remarks</span></span>

<span data-ttu-id="ec466-111">Esse método substitui o método [**CAMThread:: GetRequest**](camthread-getrequest.md) .</span><span class="sxs-lookup"><span data-stu-id="ec466-111">This method overrides the [**CAMThread::GetRequest**](camthread-getrequest.md) method.</span></span> <span data-ttu-id="ec466-112">O valor de retorno é convertido para o seguinte tipo enumerado:</span><span class="sxs-lookup"><span data-stu-id="ec466-112">The return value is cast to the following enumerated type:</span></span>


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a><span data-ttu-id="ec466-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec466-113">Requirements</span></span>



| <span data-ttu-id="ec466-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec466-114">Requirement</span></span> | <span data-ttu-id="ec466-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ec466-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec466-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ec466-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ec466-117"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec466-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ec466-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ec466-118">Library</span></span><br/> | <dl> <span data-ttu-id="ec466-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ec466-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec466-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec466-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec466-121">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="ec466-121">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 





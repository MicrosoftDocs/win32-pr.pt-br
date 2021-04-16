---
description: O método OnThreadCreate é chamado quando o thread de streaming é inicializado.
ms.assetid: eeaa0d12-3185-4c97-b481-fc420cfc0897
title: Método CSourceStream. OnThreadCreate (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadCreate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5ae3c210ca81eafa1951fc51301eaf50491357f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750654"
---
# <a name="csourcestreamonthreadcreate-method"></a><span data-ttu-id="6d912-103">Método CSourceStream. OnThreadCreate</span><span class="sxs-lookup"><span data-stu-id="6d912-103">CSourceStream.OnThreadCreate method</span></span>

<span data-ttu-id="6d912-104">O `OnThreadCreate` método é chamado quando o thread de streaming é inicializado.</span><span class="sxs-lookup"><span data-stu-id="6d912-104">The `OnThreadCreate` method is called when the streaming thread is initialized.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d912-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d912-105">Syntax</span></span>


```C++
virtual HRESULT OnThreadCreate();
```



## <a name="parameters"></a><span data-ttu-id="6d912-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d912-106">Parameters</span></span>

<span data-ttu-id="6d912-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6d912-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6d912-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6d912-108">Return value</span></span>

<span data-ttu-id="6d912-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6d912-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d912-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d912-110">Remarks</span></span>

<span data-ttu-id="6d912-111">O procedimento de thread, [**CSourceStream:: ThreadProc**](csourcestream-threadproc.md), chama esse método quando recebe pela primeira vez uma solicitação [**CSourceStream:: init**](csourcestream-init.md) .</span><span class="sxs-lookup"><span data-stu-id="6d912-111">The thread procedure, [**CSourceStream::ThreadProc**](csourcestream-threadproc.md), calls this method when it first receives a [**CSourceStream::Init**](csourcestream-init.md) request.</span></span> <span data-ttu-id="6d912-112">O método não faz nada na classe base.</span><span class="sxs-lookup"><span data-stu-id="6d912-112">The method does nothing in the base class.</span></span> <span data-ttu-id="6d912-113">A classe derivada pode substituir esse método para executar inicializações de thread.</span><span class="sxs-lookup"><span data-stu-id="6d912-113">The derived class can override this method to perform thread initializations.</span></span> <span data-ttu-id="6d912-114">Se a classe derivada retornar um código de erro, o thread será encerrado com um erro.</span><span class="sxs-lookup"><span data-stu-id="6d912-114">If the derived class returns an error code, the thread exits with an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d912-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d912-115">Requirements</span></span>



| <span data-ttu-id="6d912-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d912-116">Requirement</span></span> | <span data-ttu-id="6d912-117">Valor</span><span class="sxs-lookup"><span data-stu-id="6d912-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d912-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6d912-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6d912-119"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6d912-119"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6d912-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6d912-120">Library</span></span><br/> | <dl> <span data-ttu-id="6d912-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6d912-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d912-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d912-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d912-123">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="6d912-123">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 





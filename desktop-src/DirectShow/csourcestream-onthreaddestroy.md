---
description: O método OnThreadDestroy é chamado quando o thread de streaming está prestes a sair.
ms.assetid: a484b6d2-bce6-4a42-9176-2a6ce374e28b
title: Método CSourceStream. OnThreadDestroy (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadDestroy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e7377ce11955d7121a33311d390464e042b98f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750280"
---
# <a name="csourcestreamonthreaddestroy-method"></a><span data-ttu-id="8de20-103">Método CSourceStream. OnThreadDestroy</span><span class="sxs-lookup"><span data-stu-id="8de20-103">CSourceStream.OnThreadDestroy method</span></span>

<span data-ttu-id="8de20-104">O `OnThreadDestroy` método é chamado quando o thread de streaming está prestes a sair.</span><span class="sxs-lookup"><span data-stu-id="8de20-104">The `OnThreadDestroy` method is called when the streaming thread is about to exit.</span></span>

## <a name="syntax"></a><span data-ttu-id="8de20-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8de20-105">Syntax</span></span>


```C++
virtual HRESULT OnThreadDestroy();
```



## <a name="parameters"></a><span data-ttu-id="8de20-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8de20-106">Parameters</span></span>

<span data-ttu-id="8de20-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8de20-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8de20-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8de20-108">Return value</span></span>

<span data-ttu-id="8de20-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8de20-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8de20-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="8de20-110">Remarks</span></span>

<span data-ttu-id="8de20-111">O procedimento de thread, [**CSourceStream:: ThreadProc**](csourcestream-threadproc.md), chama esse método antes de sair.</span><span class="sxs-lookup"><span data-stu-id="8de20-111">The thread procedure, [**CSourceStream::ThreadProc**](csourcestream-threadproc.md), calls this method before it exits.</span></span> <span data-ttu-id="8de20-112">O método não faz nada na classe base; Ele está disponível para a classe derivada substituir.</span><span class="sxs-lookup"><span data-stu-id="8de20-112">The method does nothing in the base class; it is available for the derived class to override.</span></span> <span data-ttu-id="8de20-113">Se a classe derivada retornar um código de erro, o thread será encerrado com um erro.</span><span class="sxs-lookup"><span data-stu-id="8de20-113">If the derived class returns an error code, the thread exits with an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="8de20-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8de20-114">Requirements</span></span>



| <span data-ttu-id="8de20-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8de20-115">Requirement</span></span> | <span data-ttu-id="8de20-116">Valor</span><span class="sxs-lookup"><span data-stu-id="8de20-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8de20-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8de20-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8de20-118"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8de20-118"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="8de20-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8de20-119">Library</span></span><br/> | <dl> <span data-ttu-id="8de20-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="8de20-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8de20-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="8de20-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8de20-122">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="8de20-122">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 





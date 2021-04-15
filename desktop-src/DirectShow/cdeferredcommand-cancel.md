---
description: 'O método Cancel cancela uma solicitação CDeferredCommand:: Invoke enfileirada anteriormente.'
ms.assetid: 77671f6b-db50-4d8a-b727-aeed365f0303
title: Método CDeferredCommand. Cancel (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Cancel
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 524300da374b10eaac884161bb0195d88f45476d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747393"
---
# <a name="cdeferredcommandcancel-method"></a><span data-ttu-id="b9d68-103">Método CDeferredCommand. Cancel</span><span class="sxs-lookup"><span data-stu-id="b9d68-103">CDeferredCommand.Cancel method</span></span>

<span data-ttu-id="b9d68-104">O `Cancel` método cancela uma solicitação [**CDeferredCommand:: Invoke**](cdeferredcommand-invoke.md) enfileirada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b9d68-104">The `Cancel` method cancels a previously queued [**CDeferredCommand::Invoke**](cdeferredcommand-invoke.md) request.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9d68-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9d68-105">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="b9d68-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9d68-106">Parameters</span></span>

<span data-ttu-id="b9d68-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b9d68-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b9d68-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b9d68-108">Return value</span></span>

<span data-ttu-id="b9d68-109">Retornará VFW \_ E \_ já \_ cancelado se **m \_ pQueue** for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b9d68-109">Returns VFW\_E\_ALREADY\_CANCELLED if **m\_pQueue** is **NULL**.</span></span> <span data-ttu-id="b9d68-110">Retorna um **HRESULT** de [**CCmdQueue:: Remove**](ccmdqueue-remove.md) se a chamada gerar um erro.</span><span class="sxs-lookup"><span data-stu-id="b9d68-110">Returns an **HRESULT** from [**CCmdQueue::Remove**](ccmdqueue-remove.md) if the call generates an error.</span></span> <span data-ttu-id="b9d68-111">Retornará S \_ OK se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b9d68-111">Returns S\_OK if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9d68-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9d68-112">Remarks</span></span>

<span data-ttu-id="b9d68-113">Essa função de membro implementa o método [**IDeferredCommand:: Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) .</span><span class="sxs-lookup"><span data-stu-id="b9d68-113">This member function implements the [**IDeferredCommand::Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9d68-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9d68-114">Requirements</span></span>



| <span data-ttu-id="b9d68-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9d68-115">Requirement</span></span> | <span data-ttu-id="b9d68-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b9d68-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9d68-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b9d68-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b9d68-118"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b9d68-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b9d68-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b9d68-119">Library</span></span><br/> | <dl> <span data-ttu-id="b9d68-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b9d68-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9d68-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9d68-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9d68-122">**Classe CDeferredCommand**</span><span class="sxs-lookup"><span data-stu-id="b9d68-122">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 





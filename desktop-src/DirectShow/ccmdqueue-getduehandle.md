---
description: O método GetDueHandle recupera o identificador de evento a ser sinalizado.
ms.assetid: 495ea76d-8b94-48a9-8025-06ab18b66693
title: Método CCmdQueue. GetDueHandle (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4cb7c8c965c72abe6343a8a75863e0e6969dc5c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778507"
---
# <a name="ccmdqueuegetduehandle-method"></a><span data-ttu-id="bdd75-103">Método CCmdQueue. GetDueHandle</span><span class="sxs-lookup"><span data-stu-id="bdd75-103">CCmdQueue.GetDueHandle method</span></span>

<span data-ttu-id="bdd75-104">O `GetDueHandle` método recupera o identificador de evento a ser sinalizado.</span><span class="sxs-lookup"><span data-stu-id="bdd75-104">The `GetDueHandle` method retrieves the event handle to be signaled.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdd75-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bdd75-105">Syntax</span></span>


```C++
HANDLE GetDueHandle();
```



## <a name="parameters"></a><span data-ttu-id="bdd75-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bdd75-106">Parameters</span></span>

<span data-ttu-id="bdd75-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="bdd75-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bdd75-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bdd75-108">Return value</span></span>

<span data-ttu-id="bdd75-109">Retorna o identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="bdd75-109">Returns the event handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdd75-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="bdd75-110">Remarks</span></span>

<span data-ttu-id="bdd75-111">Retornar o identificador de evento sempre que houver comandos adiados que são devidos à execução (quando [**CCmdQueue:: GetDueCommand**](ccmdqueue-getduecommand.md) não será bloqueado).</span><span class="sxs-lookup"><span data-stu-id="bdd75-111">Return the event handle whenever there are deferred commands that are due for execution (when [**CCmdQueue::GetDueCommand**](ccmdqueue-getduecommand.md) will not block).</span></span>

## <a name="requirements"></a><span data-ttu-id="bdd75-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdd75-112">Requirements</span></span>



| <span data-ttu-id="bdd75-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdd75-113">Requirement</span></span> | <span data-ttu-id="bdd75-114">Valor</span><span class="sxs-lookup"><span data-stu-id="bdd75-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdd75-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bdd75-115">Header</span></span><br/>  | <dl> <span data-ttu-id="bdd75-116"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bdd75-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bdd75-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bdd75-117">Library</span></span><br/> | <dl> <span data-ttu-id="bdd75-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="bdd75-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdd75-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="bdd75-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdd75-120">**Classe CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="bdd75-120">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 





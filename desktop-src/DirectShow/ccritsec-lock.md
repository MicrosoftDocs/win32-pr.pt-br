---
description: O método Lock bloqueia o objeto da seção crítica.
ms.assetid: b08be5ec-3f02-4ed8-8791-20e4d2a0c55f
title: Método CCritSec. Lock (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.Lock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 19599e9cd3c3b8fa913bd07d22fe743aaaa1382f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778506"
---
# <a name="ccritseclock-method"></a><span data-ttu-id="5c393-103">Método CCritSec. Lock</span><span class="sxs-lookup"><span data-stu-id="5c393-103">CCritSec.Lock method</span></span>

<span data-ttu-id="5c393-104">O método **Lock** bloqueia o objeto da seção crítica.</span><span class="sxs-lookup"><span data-stu-id="5c393-104">The **Lock** method locks the critical section object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c393-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c393-105">Syntax</span></span>


```C++
void Lock();
```



## <a name="parameters"></a><span data-ttu-id="5c393-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5c393-106">Parameters</span></span>

<span data-ttu-id="5c393-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5c393-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5c393-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5c393-108">Return value</span></span>

<span data-ttu-id="5c393-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5c393-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c393-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c393-110">Remarks</span></span>

<span data-ttu-id="5c393-111">Esse método chama a função [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) .</span><span class="sxs-lookup"><span data-stu-id="5c393-111">This method calls the [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) function.</span></span>

<span data-ttu-id="5c393-112">Chame a função de membro [**CCritSec:: Unlock**](ccritsec-unlock.md) para desbloquear a seção crítica.</span><span class="sxs-lookup"><span data-stu-id="5c393-112">Call the [**CCritSec::Unlock**](ccritsec-unlock.md) member function to unlock the critical section.</span></span> <span data-ttu-id="5c393-113">Você pode fazer várias chamadas para o método **Lock** no mesmo thread; Não se esqueça de chamar **desbloquear** um número de vezes correspondente.</span><span class="sxs-lookup"><span data-stu-id="5c393-113">You can make multiple calls to the **Lock** method on the same thread; be sure to call **Unlock** a corresponding number of times.</span></span>

<span data-ttu-id="5c393-114">Se o objeto já estiver bloqueado por outro thread, o método **CCritSec:: Lock** bloqueará até que o objeto seja liberado ou até que ocorra uma exceção de deadlock possível.</span><span class="sxs-lookup"><span data-stu-id="5c393-114">If the object is already locked by another thread, the **CCritSec::Lock** method blocks until the object is released, or until a possible-deadlock exception occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c393-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c393-115">Requirements</span></span>



| <span data-ttu-id="5c393-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c393-116">Requirement</span></span> | <span data-ttu-id="5c393-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5c393-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c393-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5c393-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5c393-119"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5c393-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="5c393-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5c393-120">Library</span></span><br/> | <dl> <span data-ttu-id="5c393-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5c393-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c393-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c393-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c393-123">**Classe CCritSec**</span><span class="sxs-lookup"><span data-stu-id="5c393-123">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 


---
description: Método de construtor.
ms.assetid: e8e9138a-6c39-41de-a7f8-d9e9c4fe5ab6
title: Construtor CCritSec. CCritSec (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6baeadace7c1f8d8d3ad5dee1ff5c9dace1c6907
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751693"
---
# <a name="ccritsecccritsec-constructor"></a><span data-ttu-id="c5abc-103">Construtor CCritSec. CCritSec</span><span class="sxs-lookup"><span data-stu-id="c5abc-103">CCritSec.CCritSec constructor</span></span>

<span data-ttu-id="c5abc-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="c5abc-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5abc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5abc-105">Syntax</span></span>


```C++
CCritSec();
```



## <a name="parameters"></a><span data-ttu-id="c5abc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5abc-106">Parameters</span></span>

<span data-ttu-id="c5abc-107">Este construtor não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c5abc-107">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5abc-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5abc-108">Remarks</span></span>

<span data-ttu-id="c5abc-109">Esse método chama a função [**InitializeCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) para inicializar a seção crítica.</span><span class="sxs-lookup"><span data-stu-id="c5abc-109">This method calls the [**InitializeCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) function to initialize the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5abc-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5abc-110">Requirements</span></span>



| <span data-ttu-id="c5abc-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5abc-111">Requirement</span></span> | <span data-ttu-id="c5abc-112">Valor</span><span class="sxs-lookup"><span data-stu-id="c5abc-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5abc-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c5abc-113">Header</span></span><br/>  | <dl> <span data-ttu-id="c5abc-114"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c5abc-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c5abc-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c5abc-115">Library</span></span><br/> | <dl> <span data-ttu-id="c5abc-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c5abc-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5abc-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5abc-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5abc-118">**Classe CCritSec**</span><span class="sxs-lookup"><span data-stu-id="c5abc-118">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 


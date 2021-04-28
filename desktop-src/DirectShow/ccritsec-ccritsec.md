---
description: Construtor de CCritSec. CCritSec-método de construtor.
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
ms.openlocfilehash: de2b852ffc9a12622a4560ae834a3347b1e07552
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119794"
---
# <a name="ccritsecccritsec-constructor"></a><span data-ttu-id="609ad-103">Construtor CCritSec. CCritSec</span><span class="sxs-lookup"><span data-stu-id="609ad-103">CCritSec.CCritSec constructor</span></span>

<span data-ttu-id="609ad-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="609ad-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="609ad-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="609ad-105">Syntax</span></span>


```C++
CCritSec();
```



## <a name="parameters"></a><span data-ttu-id="609ad-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="609ad-106">Parameters</span></span>

<span data-ttu-id="609ad-107">Este construtor não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="609ad-107">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="609ad-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="609ad-108">Remarks</span></span>

<span data-ttu-id="609ad-109">Esse método chama a função [**InitializeCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) para inicializar a seção crítica.</span><span class="sxs-lookup"><span data-stu-id="609ad-109">This method calls the [**InitializeCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) function to initialize the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="609ad-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="609ad-110">Requirements</span></span>



| <span data-ttu-id="609ad-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="609ad-111">Requirement</span></span> | <span data-ttu-id="609ad-112">Valor</span><span class="sxs-lookup"><span data-stu-id="609ad-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="609ad-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="609ad-113">Header</span></span><br/>  | <dl> <span data-ttu-id="609ad-114"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="609ad-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="609ad-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="609ad-115">Library</span></span><br/> | <dl> <span data-ttu-id="609ad-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="609ad-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="609ad-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="609ad-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="609ad-118">**Classe CCritSec**</span><span class="sxs-lookup"><span data-stu-id="609ad-118">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 


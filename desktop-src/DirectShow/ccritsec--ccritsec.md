---
description: Método destruidor.
ms.assetid: cade850c-391c-41dc-adfe-56de8b2bbfff
title: CCritSec. ~ CCritSec Destruitor (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.~CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21029e2d53fd03ded2be4faa98e8b3e27681600c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760772"
---
# <a name="ccritsecccritsec-destructor"></a><span data-ttu-id="c92ca-103">Destruidor CCritSec. ~ CCritSec</span><span class="sxs-lookup"><span data-stu-id="c92ca-103">CCritSec.~CCritSec destructor</span></span>

<span data-ttu-id="c92ca-104">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="c92ca-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c92ca-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c92ca-105">Syntax</span></span>


```C++
~CCritSec();
```



## <a name="remarks"></a><span data-ttu-id="c92ca-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="c92ca-106">Remarks</span></span>

<span data-ttu-id="c92ca-107">Esse método chama a função [**DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) para excluir a seção crítica.</span><span class="sxs-lookup"><span data-stu-id="c92ca-107">This method calls the [**DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) function to delete the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="c92ca-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c92ca-108">Requirements</span></span>



| <span data-ttu-id="c92ca-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="c92ca-109">Requirement</span></span> | <span data-ttu-id="c92ca-110">Valor</span><span class="sxs-lookup"><span data-stu-id="c92ca-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c92ca-111">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c92ca-111">Header</span></span><br/>  | <dl> <span data-ttu-id="c92ca-112"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c92ca-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c92ca-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c92ca-113">Library</span></span><br/> | <dl> <span data-ttu-id="c92ca-114"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c92ca-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c92ca-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="c92ca-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c92ca-116">**Classe CCritSec**</span><span class="sxs-lookup"><span data-stu-id="c92ca-116">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 


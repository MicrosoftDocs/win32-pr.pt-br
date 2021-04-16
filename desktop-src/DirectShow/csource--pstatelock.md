---
description: O método pStateLock recupera um ponteiro para o objeto de seção crítica do filtro.
ms.assetid: 10a2e74b-a5aa-4d68-958e-d86f4b78037e
title: Método CSource. pStateLock (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.pStateLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c0705584a513d64dfd1cd17075d95617234f7f8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757897"
---
# <a name="csourcepstatelock-method"></a><span data-ttu-id="f613d-103">Método CSource. pStateLock</span><span class="sxs-lookup"><span data-stu-id="f613d-103">CSource.pStateLock method</span></span>

<span data-ttu-id="f613d-104">O método **pStateLock** recupera um ponteiro para o objeto de seção crítica do filtro.</span><span class="sxs-lookup"><span data-stu-id="f613d-104">The **pStateLock** method retrieves a pointer to the filter's critical section object.</span></span>

> [!Note]  
> <span data-ttu-id="f613d-105">Embora nomeado como uma variável de membro, **pStateLock** é um método.</span><span class="sxs-lookup"><span data-stu-id="f613d-105">Although named like a member variable, **pStateLock** is a method.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f613d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f613d-106">Syntax</span></span>


```C++
CCritSec* pStateLock();
```



## <a name="parameters"></a><span data-ttu-id="f613d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f613d-107">Parameters</span></span>

<span data-ttu-id="f613d-108">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f613d-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f613d-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f613d-109">Return value</span></span>

<span data-ttu-id="f613d-110">Retorna um ponteiro para a variável de membro [**CSource:: m \_ cStateLock**](csource-m-cstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="f613d-110">Returns a pointer to the [**CSource::m\_cStateLock**](csource-m-cstatelock.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="f613d-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f613d-111">Requirements</span></span>



| <span data-ttu-id="f613d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f613d-112">Requirement</span></span> | <span data-ttu-id="f613d-113">Valor</span><span class="sxs-lookup"><span data-stu-id="f613d-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f613d-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f613d-114">Header</span></span><br/>  | <dl> <span data-ttu-id="f613d-115"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f613d-115"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f613d-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f613d-116">Library</span></span><br/> | <dl> <span data-ttu-id="f613d-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f613d-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f613d-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="f613d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f613d-119">**Classe CSource**</span><span class="sxs-lookup"><span data-stu-id="f613d-119">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 





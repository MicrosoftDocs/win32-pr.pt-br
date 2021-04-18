---
description: Método destruidor.
ms.assetid: 3714d030-f0bd-4826-a3c5-fc206bb88561
title: CBaseObject. ~ CBaseObject destruidor (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject.~CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 908f335105fa88f3ed547eed0e92ea50a6f85f26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752099"
---
# <a name="cbaseobjectcbaseobject-destructor"></a><span data-ttu-id="d328c-103">Destruidor CBaseObject. ~ CBaseObject</span><span class="sxs-lookup"><span data-stu-id="d328c-103">CBaseObject.~CBaseObject destructor</span></span>

<span data-ttu-id="d328c-104">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="d328c-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d328c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d328c-105">Syntax</span></span>


```C++
~CBaseObject();
```



## <a name="remarks"></a><span data-ttu-id="d328c-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="d328c-106">Remarks</span></span>

<span data-ttu-id="d328c-107">Esse método diminui a contagem de objetos ativos.</span><span class="sxs-lookup"><span data-stu-id="d328c-107">This method decrements the active-object count.</span></span> <span data-ttu-id="d328c-108">(Consulte [**CBaseObject:: ObjectsActive**](cbaseobject-objectsactive.md).)</span><span class="sxs-lookup"><span data-stu-id="d328c-108">(See [**CBaseObject::ObjectsActive**](cbaseobject-objectsactive.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="d328c-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d328c-109">Requirements</span></span>



| <span data-ttu-id="d328c-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="d328c-110">Requirement</span></span> | <span data-ttu-id="d328c-111">Valor</span><span class="sxs-lookup"><span data-stu-id="d328c-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d328c-112">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d328c-112">Header</span></span><br/>  | <dl> <span data-ttu-id="d328c-113"><dt>Combase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d328c-113"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d328c-114">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d328c-114">Library</span></span><br/> | <dl> <span data-ttu-id="d328c-115"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d328c-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d328c-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="d328c-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d328c-117">**Classe CBaseObject**</span><span class="sxs-lookup"><span data-stu-id="d328c-117">**CBaseObject Class**</span></span>](cbaseobject.md)
</dt> </dl>

 

 





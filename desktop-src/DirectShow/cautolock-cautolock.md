---
description: Método de construtor. O Construtor bloqueia o objeto de seção crítica especificado.
ms.assetid: 5a0d74f9-bb99-4922-9a92-2e7c1863421f
title: Construtor CAutoLock. CAutoLock (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock.CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fed29011d4fe581ed146f64800351a3f1053d957
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778653"
---
# <a name="cautolockcautolock-constructor"></a><span data-ttu-id="65ee4-104">Construtor CAutoLock. CAutoLock</span><span class="sxs-lookup"><span data-stu-id="65ee4-104">CAutoLock.CAutoLock constructor</span></span>

<span data-ttu-id="65ee4-105">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="65ee4-105">Constructor method.</span></span> <span data-ttu-id="65ee4-106">O Construtor bloqueia o objeto de seção crítica especificado.</span><span class="sxs-lookup"><span data-stu-id="65ee4-106">The constructor locks the specified critical section object.</span></span>

## <a name="syntax"></a><span data-ttu-id="65ee4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65ee4-107">Syntax</span></span>


```C++
CAutoLock(
   CCritSec *plock
);
```



## <a name="parameters"></a><span data-ttu-id="65ee4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65ee4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65ee4-109">*plock*</span><span class="sxs-lookup"><span data-stu-id="65ee4-109">*plock*</span></span> 
</dt> <dd>

<span data-ttu-id="65ee4-110">Ponteiro para um objeto [**CCritSec**](ccritsec.md) , que contém um objeto de seção crítica.</span><span class="sxs-lookup"><span data-stu-id="65ee4-110">Pointer to a [**CCritSec**](ccritsec.md) object, which contains a critical section object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="65ee4-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65ee4-111">Requirements</span></span>



| <span data-ttu-id="65ee4-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="65ee4-112">Requirement</span></span> | <span data-ttu-id="65ee4-113">Valor</span><span class="sxs-lookup"><span data-stu-id="65ee4-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65ee4-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="65ee4-114">Header</span></span><br/>  | <dl> <span data-ttu-id="65ee4-115"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65ee4-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="65ee4-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="65ee4-116">Library</span></span><br/> | <dl> <span data-ttu-id="65ee4-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="65ee4-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65ee4-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="65ee4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65ee4-119">**Classe CAutoLock**</span><span class="sxs-lookup"><span data-stu-id="65ee4-119">**CAutoLock Class**</span></span>](cautolock.md)
</dt> </dl>

 

 





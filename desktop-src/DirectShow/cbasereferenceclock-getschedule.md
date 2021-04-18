---
description: O método getschedule recupera um ponteiro para o objeto de agendamento do relógio.
ms.assetid: ae509f16-d85f-4365-8cf2-c6585cbbdc3d
title: Método CBaseReferenceClock. getschedule (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetSchedule
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a37cdb3e18f3ab71b144af071233aee5a6a3a93d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752509"
---
# <a name="cbasereferenceclockgetschedule-method"></a><span data-ttu-id="aba2a-103">Método CBaseReferenceClock. getschedule</span><span class="sxs-lookup"><span data-stu-id="aba2a-103">CBaseReferenceClock.GetSchedule method</span></span>

<span data-ttu-id="aba2a-104">O `GetSchedule` método recupera um ponteiro para o objeto de agendamento do relógio.</span><span class="sxs-lookup"><span data-stu-id="aba2a-104">The `GetSchedule` method retrieves a pointer to the clock's scheduling object.</span></span>

## <a name="syntax"></a><span data-ttu-id="aba2a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aba2a-105">Syntax</span></span>


```C++
CAMSchedule* GetSchedule();
```



## <a name="parameters"></a><span data-ttu-id="aba2a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aba2a-106">Parameters</span></span>

<span data-ttu-id="aba2a-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="aba2a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aba2a-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aba2a-108">Return value</span></span>

<span data-ttu-id="aba2a-109">Retorna a variável de membro [**CBaseReferenceClock:: m \_ pSchedule**](cbasereferenceclock-m-pschedule.md) .</span><span class="sxs-lookup"><span data-stu-id="aba2a-109">Returns the [**CBaseReferenceClock::m\_pSchedule**](cbasereferenceclock-m-pschedule.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="aba2a-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aba2a-110">Requirements</span></span>



| <span data-ttu-id="aba2a-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="aba2a-111">Requirement</span></span> | <span data-ttu-id="aba2a-112">Valor</span><span class="sxs-lookup"><span data-stu-id="aba2a-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aba2a-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aba2a-113">Header</span></span><br/>  | <dl> <span data-ttu-id="aba2a-114"><dt>Refclock. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aba2a-114"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="aba2a-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aba2a-115">Library</span></span><br/> | <dl> <span data-ttu-id="aba2a-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="aba2a-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aba2a-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="aba2a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aba2a-118">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="aba2a-118">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 





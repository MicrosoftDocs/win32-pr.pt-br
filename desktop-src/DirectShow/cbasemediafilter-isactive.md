---
description: O método IsActive determina se o objeto está ativo (em execução ou em pausa).
ms.assetid: 6531cf1f-e057-4094-9354-d5a32371c83c
title: Método CBaseMediaFilter. IsActive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.IsActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6438850b90309b47fbe1fb76b1fd4f7baea8f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756825"
---
# <a name="cbasemediafilterisactive-method"></a><span data-ttu-id="8f720-103">Método CBaseMediaFilter. IsActive</span><span class="sxs-lookup"><span data-stu-id="8f720-103">CBaseMediaFilter.IsActive method</span></span>

<span data-ttu-id="8f720-104">O `IsActive` método determina se o objeto está ativo (em execução ou em pausa).</span><span class="sxs-lookup"><span data-stu-id="8f720-104">The `IsActive` method determines whether the object is active (running or paused).</span></span>

## <a name="syntax"></a><span data-ttu-id="8f720-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f720-105">Syntax</span></span>


```C++
BOOL IsActive();
```



## <a name="parameters"></a><span data-ttu-id="8f720-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f720-106">Parameters</span></span>

<span data-ttu-id="8f720-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8f720-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8f720-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8f720-108">Return value</span></span>

<span data-ttu-id="8f720-109">Retornará **true** se o objeto estiver em pausa ou em execução, ou **false** se for interrompido.</span><span class="sxs-lookup"><span data-stu-id="8f720-109">Returns **TRUE** if the object is paused or running, or **FALSE** if it is stopped.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f720-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f720-110">Requirements</span></span>



| <span data-ttu-id="8f720-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f720-111">Requirement</span></span> | <span data-ttu-id="8f720-112">Valor</span><span class="sxs-lookup"><span data-stu-id="8f720-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f720-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8f720-113">Header</span></span><br/>  | <dl> <span data-ttu-id="8f720-114"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f720-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8f720-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8f720-115">Library</span></span><br/> | <dl> <span data-ttu-id="8f720-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="8f720-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f720-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f720-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f720-118">**Classe CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="8f720-118">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 





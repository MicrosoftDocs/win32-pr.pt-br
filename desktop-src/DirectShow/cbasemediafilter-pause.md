---
description: Pausa o objeto. Implementa o método IMediaFilter::P ause.
ms.assetid: 4f4cbe7e-3004-4731-864f-737c2f51afff
title: Método CBaseMediaFilter. PAUSE (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a75cbcf1d629b997584cff35ebd4095094fe8607
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753360"
---
# <a name="cbasemediafilterpause-method"></a><span data-ttu-id="1e45a-104">Método CBaseMediaFilter. Pause</span><span class="sxs-lookup"><span data-stu-id="1e45a-104">CBaseMediaFilter.Pause method</span></span>

<span data-ttu-id="1e45a-105">Pausa o objeto.</span><span class="sxs-lookup"><span data-stu-id="1e45a-105">Pauses the object.</span></span> <span data-ttu-id="1e45a-106">Implementa o método [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) .</span><span class="sxs-lookup"><span data-stu-id="1e45a-106">Implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e45a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e45a-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="1e45a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e45a-108">Parameters</span></span>

<span data-ttu-id="1e45a-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1e45a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1e45a-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1e45a-110">Return value</span></span>

<span data-ttu-id="1e45a-111">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1e45a-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e45a-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e45a-112">Remarks</span></span>

<span data-ttu-id="1e45a-113">Na classe base, esse método define a variável de membro de [**\_ estado CBaseMediaFilter:: m**](cbasemediafilter-m-state.md) para estado em \_ pausa, mas não faz mais nada.</span><span class="sxs-lookup"><span data-stu-id="1e45a-113">In the base class, this method sets the [**CBaseMediaFilter::m\_State**](cbasemediafilter-m-state.md) member variable to State\_Paused but does nothing else.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e45a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e45a-114">Requirements</span></span>



| <span data-ttu-id="1e45a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e45a-115">Requirement</span></span> | <span data-ttu-id="1e45a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="1e45a-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e45a-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1e45a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1e45a-118"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e45a-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1e45a-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1e45a-119">Library</span></span><br/> | <dl> <span data-ttu-id="1e45a-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1e45a-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e45a-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e45a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e45a-122">**Classe CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="1e45a-122">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 





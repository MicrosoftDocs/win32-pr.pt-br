---
description: 'O método Stop interrompe o objeto. Esse método implementa o método IMediaFilter:: Stop.'
ms.assetid: 9282d90a-932c-4ba0-84f1-1de2c125bfbd
title: Método CBaseMediaFilter. Stop (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22bb45234c8be832f8ea30ed70b50c8f4919b7e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751269"
---
# <a name="cbasemediafilterstop-method"></a><span data-ttu-id="d4b2c-104">Método CBaseMediaFilter. Stop</span><span class="sxs-lookup"><span data-stu-id="d4b2c-104">CBaseMediaFilter.Stop method</span></span>

<span data-ttu-id="d4b2c-105">O `Stop` método interrompe o objeto.</span><span class="sxs-lookup"><span data-stu-id="d4b2c-105">The `Stop` method stops the object.</span></span> <span data-ttu-id="d4b2c-106">Esse método implementa o método [**IMediaFilter:: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .</span><span class="sxs-lookup"><span data-stu-id="d4b2c-106">This method implements the [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4b2c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d4b2c-107">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="d4b2c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4b2c-108">Parameters</span></span>

<span data-ttu-id="d4b2c-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d4b2c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d4b2c-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d4b2c-110">Return value</span></span>

<span data-ttu-id="d4b2c-111">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d4b2c-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4b2c-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4b2c-112">Remarks</span></span>

<span data-ttu-id="d4b2c-113">Na classe base, esse método define a variável de membro de [**\_ estado CBaseMediaFilter:: m**](cbasemediafilter-m-state.md) para estado \_ parado, mas não faz mais nada.</span><span class="sxs-lookup"><span data-stu-id="d4b2c-113">In the base class, this method sets the [**CBaseMediaFilter::m\_State**](cbasemediafilter-m-state.md) member variable to State\_Stopped but does nothing else.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4b2c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4b2c-114">Requirements</span></span>



| <span data-ttu-id="d4b2c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4b2c-115">Requirement</span></span> | <span data-ttu-id="d4b2c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d4b2c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4b2c-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d4b2c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d4b2c-118"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4b2c-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d4b2c-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d4b2c-119">Library</span></span><br/> | <dl> <span data-ttu-id="d4b2c-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d4b2c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4b2c-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4b2c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4b2c-122">**Classe CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="d4b2c-122">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 





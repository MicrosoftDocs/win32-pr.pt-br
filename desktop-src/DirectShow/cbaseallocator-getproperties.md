---
description: 'O método GetProperties recupera o número de buffers que o alocador criará e as propriedades do buffer. Esse método implementa o método IMemAllocator:: GetProperties.'
ms.assetid: ccee4d69-52fc-4e3c-b6a4-787914708be4
title: Método CBaseAllocator. GetProperties (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abf143b11b6dd67fca6c87f9a31ce69f18951311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755796"
---
# <a name="cbaseallocatorgetproperties-method"></a><span data-ttu-id="ea559-104">Método CBaseAllocator. GetProperties</span><span class="sxs-lookup"><span data-stu-id="ea559-104">CBaseAllocator.GetProperties method</span></span>

<span data-ttu-id="ea559-105">O `GetProperties` método recupera o número de buffers que o alocador criará e as propriedades do buffer.</span><span class="sxs-lookup"><span data-stu-id="ea559-105">The `GetProperties` method retrieves the number of buffers that the allocator will create, and the buffer properties.</span></span> <span data-ttu-id="ea559-106">Esse método implementa o método [**IMemAllocator:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) .</span><span class="sxs-lookup"><span data-stu-id="ea559-106">This method implements the [**IMemAllocator::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea559-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea559-107">Syntax</span></span>


```C++
HRESULT GetProperties(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="ea559-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea559-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea559-109">*pProps*</span><span class="sxs-lookup"><span data-stu-id="ea559-109">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="ea559-110">Ponteiro para uma estrutura de [**\_ Propriedades de alocador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que recebe as propriedades de alocador.</span><span class="sxs-lookup"><span data-stu-id="ea559-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that receives the allocator properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea559-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ea559-111">Return value</span></span>

<span data-ttu-id="ea559-112">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ea559-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea559-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea559-113">Requirements</span></span>



| <span data-ttu-id="ea559-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea559-114">Requirement</span></span> | <span data-ttu-id="ea559-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ea559-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea559-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ea559-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ea559-117"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea559-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ea559-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ea559-118">Library</span></span><br/> | <dl> <span data-ttu-id="ea559-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ea559-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea559-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea559-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea559-121">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="ea559-121">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 





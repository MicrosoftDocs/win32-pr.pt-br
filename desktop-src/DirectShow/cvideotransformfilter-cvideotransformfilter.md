---
description: Construtor de CVideoTransformFilter. CVideoTransformFilter-método de construtor.
ms.assetid: 4dad635f-4637-4f40-9f02-a91b59d05278
title: Construtor CVideoTransformFilter. CVideoTransformFilter (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.CVideoTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 59609e09b252e56aded1669264bb98cdbe823e89
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084584"
---
# <a name="cvideotransformfiltercvideotransformfilter-constructor"></a><span data-ttu-id="03c24-103">Construtor CVideoTransformFilter. CVideoTransformFilter</span><span class="sxs-lookup"><span data-stu-id="03c24-103">CVideoTransformFilter.CVideoTransformFilter constructor</span></span>

<span data-ttu-id="03c24-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="03c24-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="03c24-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03c24-105">Syntax</span></span>


```C++
CVideoTransformFilter(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="03c24-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="03c24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03c24-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="03c24-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="03c24-108">Cadeia de caracteres que contém o nome de depuração do filtro.</span><span class="sxs-lookup"><span data-stu-id="03c24-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="03c24-109">Para obter mais informações, consulte [**CBaseObject:: CBaseObject**](cbaseobject-cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="03c24-109">For more information, see [**CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="03c24-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="03c24-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="03c24-111">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="03c24-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="03c24-112">Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="03c24-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="03c24-113">Caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="03c24-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="03c24-114">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="03c24-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="03c24-115">Identificador de classe do filtro.</span><span class="sxs-lookup"><span data-stu-id="03c24-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03c24-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03c24-116">Requirements</span></span>



| <span data-ttu-id="03c24-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="03c24-117">Requirement</span></span> | <span data-ttu-id="03c24-118">Valor</span><span class="sxs-lookup"><span data-stu-id="03c24-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03c24-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="03c24-119">Header</span></span><br/>  | <dl> <span data-ttu-id="03c24-120"><dt>Vtrans. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03c24-120"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="03c24-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="03c24-121">Library</span></span><br/> | <dl> <span data-ttu-id="03c24-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="03c24-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03c24-123">Consulte também</span><span class="sxs-lookup"><span data-stu-id="03c24-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03c24-124">**Classe CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="03c24-124">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 





---
description: Método de construtor.
ms.assetid: 94a92c1e-9768-4293-8290-a2b1938cd196
title: Construtor CSource. CSource (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.CSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 992775659d5f9838ef63b15c5395998f1faf6200
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785498"
---
# <a name="csourcecsource-constructor"></a><span data-ttu-id="efb5d-103">Construtor CSource. CSource</span><span class="sxs-lookup"><span data-stu-id="efb5d-103">CSource.CSource constructor</span></span>

<span data-ttu-id="efb5d-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="efb5d-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="efb5d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="efb5d-105">Syntax</span></span>


```C++
CSource(
   TCHAR     *pName,
   LPUNKNOWN lpunk,
   CLSID     clsid
);
```



## <a name="parameters"></a><span data-ttu-id="efb5d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="efb5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efb5d-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="efb5d-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="efb5d-108">Ponteiro para uma cadeia de caracteres que contém o nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="efb5d-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="efb5d-109">Para obter mais informações, consulte [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="efb5d-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="efb5d-110">*lpunk*</span><span class="sxs-lookup"><span data-stu-id="efb5d-110">*lpunk*</span></span> 
</dt> <dd>

<span data-ttu-id="efb5d-111">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="efb5d-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="efb5d-112">Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="efb5d-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="efb5d-113">Caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="efb5d-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="efb5d-114">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="efb5d-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="efb5d-115">Identificador de classe do filtro.</span><span class="sxs-lookup"><span data-stu-id="efb5d-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="efb5d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efb5d-116">Requirements</span></span>



| <span data-ttu-id="efb5d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="efb5d-117">Requirement</span></span> | <span data-ttu-id="efb5d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="efb5d-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efb5d-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="efb5d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="efb5d-120"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="efb5d-120"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="efb5d-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="efb5d-121">Library</span></span><br/> | <dl> <span data-ttu-id="efb5d-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="efb5d-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efb5d-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="efb5d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efb5d-124">**Classe CSource**</span><span class="sxs-lookup"><span data-stu-id="efb5d-124">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 





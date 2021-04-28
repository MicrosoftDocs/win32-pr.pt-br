---
description: Construtor de CTransInPlaceFilter. CTransInPlaceFilter-método de construtor.
ms.assetid: f0d30125-5d16-470c-a5fb-a7df96814dad
title: Construtor CTransInPlaceFilter. CTransInPlaceFilter (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CTransInPlaceFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6b14af4b0d1f33933db8ca2fd1835e9711edad9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084774"
---
# <a name="ctransinplacefilterctransinplacefilter-constructor"></a><span data-ttu-id="d5c8a-103">Construtor CTransInPlaceFilter. CTransInPlaceFilter</span><span class="sxs-lookup"><span data-stu-id="d5c8a-103">CTransInPlaceFilter.CTransInPlaceFilter constructor</span></span>

<span data-ttu-id="d5c8a-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="d5c8a-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5c8a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5c8a-105">Syntax</span></span>


```C++
CTransInPlaceFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   REFCLSID  clsid,
   HRESULT   *phr,
   bool      bModifiesData = TRUE
);
```



## <a name="parameters"></a><span data-ttu-id="d5c8a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5c8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5c8a-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="d5c8a-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="d5c8a-108">Cadeia de caracteres que contém o nome de depuração do filtro.</span><span class="sxs-lookup"><span data-stu-id="d5c8a-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="d5c8a-109">Para obter mais informações, consulte [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="d5c8a-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5c8a-110">*lpUnk*</span><span class="sxs-lookup"><span data-stu-id="d5c8a-110">*lpUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="d5c8a-111">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="d5c8a-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="d5c8a-112">Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="d5c8a-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="d5c8a-113">Caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d5c8a-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d5c8a-114">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="d5c8a-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="d5c8a-115">Identificador de classe do filtro.</span><span class="sxs-lookup"><span data-stu-id="d5c8a-115">Class identifier of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="d5c8a-116">*phr*</span><span class="sxs-lookup"><span data-stu-id="d5c8a-116">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="d5c8a-117">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="d5c8a-117">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="d5c8a-118">*bModifiesData*</span><span class="sxs-lookup"><span data-stu-id="d5c8a-118">*bModifiesData*</span></span> 
</dt> <dd>

<span data-ttu-id="d5c8a-119">Valor booliano que especifica se o filtro modifica os dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="d5c8a-119">Boolean value that specifies whether the filter modifies the input data.</span></span> <span data-ttu-id="d5c8a-120">Se **for true**, o filtro modificará os dados.</span><span class="sxs-lookup"><span data-stu-id="d5c8a-120">If **TRUE**, the filter modifies the data.</span></span> <span data-ttu-id="d5c8a-121">Caso contrário, o filtro passará o downstream de dados inalterado.</span><span class="sxs-lookup"><span data-stu-id="d5c8a-121">Otherwise, the filter passes the data downstream unchanged.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5c8a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5c8a-122">Requirements</span></span>



| <span data-ttu-id="d5c8a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5c8a-123">Requirement</span></span> | <span data-ttu-id="d5c8a-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d5c8a-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5c8a-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d5c8a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d5c8a-126"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5c8a-126"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d5c8a-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d5c8a-127">Library</span></span><br/> | <dl> <span data-ttu-id="d5c8a-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d5c8a-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5c8a-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d5c8a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5c8a-130">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="d5c8a-130">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 





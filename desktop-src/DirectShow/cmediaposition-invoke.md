---
description: O método Invoke fornece acesso a propriedades e métodos expostos pelo objeto.
ms.assetid: 3c03751d-239b-4cc5-bfab-8d1aed1074b8
title: Método CMediaPosition. Invoke (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3955848bf2a87e0983ddd7dc3bef48f157ae6648
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769229"
---
# <a name="cmediapositioninvoke-method"></a><span data-ttu-id="b2785-103">Método CMediaPosition. Invoke</span><span class="sxs-lookup"><span data-stu-id="b2785-103">CMediaPosition.Invoke method</span></span>

<span data-ttu-id="b2785-104">O `Invoke` método fornece acesso a propriedades e métodos expostos pelo objeto.</span><span class="sxs-lookup"><span data-stu-id="b2785-104">The `Invoke` method provides access to properties and methods exposed by the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2785-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2785-105">Syntax</span></span>


```C++
HRESULT Invoke(
   DISPID     dispidMember,
   REFIID     riid,
   LCID       lcid,
   WORD       wFlags,
   DISPPARAMS *pdispparams,
   VARIANT    *pvarResult,
   EXCEPINFO  *pexcepinfo,
   UINT       *puArgErr
);
```



## <a name="parameters"></a><span data-ttu-id="b2785-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2785-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2785-107">*dispidMember*</span><span class="sxs-lookup"><span data-stu-id="b2785-107">*dispidMember*</span></span> 
</dt> <dd>

<span data-ttu-id="b2785-108">Identificador do membro.</span><span class="sxs-lookup"><span data-stu-id="b2785-108">Identifier of the member.</span></span> <span data-ttu-id="b2785-109">Use [**CMediaPosition:: GetIDsOfNames**](cmediaposition-getidsofnames.md) para obter o identificador de expedição.</span><span class="sxs-lookup"><span data-stu-id="b2785-109">Use [**CMediaPosition::GetIDsOfNames**](cmediaposition-getidsofnames.md) to obtain the dispatch identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b2785-110">*riid*</span><span class="sxs-lookup"><span data-stu-id="b2785-110">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="b2785-111">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="b2785-111">Reserved for future use.</span></span> <span data-ttu-id="b2785-112">Deve ser um IID \_ nulo.</span><span class="sxs-lookup"><span data-stu-id="b2785-112">Must be IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="b2785-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="b2785-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="b2785-114">Contexto de localidade no qual interpretar argumentos.</span><span class="sxs-lookup"><span data-stu-id="b2785-114">Locale context in which to interpret arguments.</span></span>

</dd> <dt>

<span data-ttu-id="b2785-115">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="b2785-115">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="b2785-116">Sinalizadores que descrevem o contexto da chamada.</span><span class="sxs-lookup"><span data-stu-id="b2785-116">Flags describing the context of the call.</span></span>

</dd> <dt>

<span data-ttu-id="b2785-117">*pdispparams*</span><span class="sxs-lookup"><span data-stu-id="b2785-117">*pdispparams*</span></span> 
</dt> <dd>

<span data-ttu-id="b2785-118">Ponteiro para uma estrutura **DIPPARAMS** que contém os argumentos.</span><span class="sxs-lookup"><span data-stu-id="b2785-118">Pointer to a **DIPPARAMS** structure that contains the arguments.</span></span>

</dd> <dt>

<span data-ttu-id="b2785-119">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="b2785-119">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="b2785-120">Ponteiro para uma **variante** que recebe o resultado, ou **NULL** se o chamador não espera nenhum resultado.</span><span class="sxs-lookup"><span data-stu-id="b2785-120">Pointer to a **VARIANT** that receives the result, or **NULL** if the caller expects no result.</span></span>

</dd> <dt>

<span data-ttu-id="b2785-121">*pexcepinfo*</span><span class="sxs-lookup"><span data-stu-id="b2785-121">*pexcepinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="b2785-122">Ponteiro para uma estrutura que recebe informações de exceção.</span><span class="sxs-lookup"><span data-stu-id="b2785-122">Pointer to a structure that receives exception information.</span></span>

</dd> <dt>

<span data-ttu-id="b2785-123">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="b2785-123">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="b2785-124">Aponta para uma variável que recebe o índice do primeiro argumento que causa um erro.</span><span class="sxs-lookup"><span data-stu-id="b2785-124">Pointer to a variable that receives the index of the first argument that causes an error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2785-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b2785-125">Return value</span></span>

<span data-ttu-id="b2785-126">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b2785-126">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b2785-127">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="b2785-127">Possible values include the following.</span></span>



| <span data-ttu-id="b2785-128">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b2785-128">Return code</span></span>                                                                                              | <span data-ttu-id="b2785-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="b2785-129">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="b2785-130"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b2785-130"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="b2785-131">Êxito.</span><span class="sxs-lookup"><span data-stu-id="b2785-131">Success.</span></span><br/>                              |
| <dl> <span data-ttu-id="b2785-132"><dt>**DISP \_ E \_ UNKNOWNINTERFACE**</dt></span><span class="sxs-lookup"><span data-stu-id="b2785-132"><dt>**DISP\_E\_UNKNOWNINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="b2785-133">O parâmetro *riid* não é nulo de IID \_</span><span class="sxs-lookup"><span data-stu-id="b2785-133">The *riid* parameter is not IID\_NULL</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b2785-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2785-134">Requirements</span></span>



| <span data-ttu-id="b2785-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2785-135">Requirement</span></span> | <span data-ttu-id="b2785-136">Valor</span><span class="sxs-lookup"><span data-stu-id="b2785-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2785-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b2785-137">Header</span></span><br/>  | <dl> <span data-ttu-id="b2785-138"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2785-138"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b2785-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b2785-139">Library</span></span><br/> | <dl> <span data-ttu-id="b2785-140"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b2785-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2785-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2785-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2785-142">**Classe CMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="b2785-142">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 





---
description: A função CreatePosPassThru cria um objeto CPosPassThru ou um objeto CRendererPosPassThru.
ms.assetid: d6fccfb4-b256-40aa-b927-84c7a886f631
title: Função CreatePosPassThru (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePosPassThru
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08735a0bac2cc5aa8f5bb61461f10097435ad9c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789698"
---
# <a name="createpospassthru-function"></a><span data-ttu-id="b2ffb-103">Função CreatePosPassThru</span><span class="sxs-lookup"><span data-stu-id="b2ffb-103">CreatePosPassThru function</span></span>

<span data-ttu-id="b2ffb-104">A `CreatePosPassThru` função cria um objeto [**CPosPassThru**](cpospassthru.md) ou um objeto [**CRendererPosPassThru**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="b2ffb-104">The `CreatePosPassThru` function creates a [**CPosPassThru**](cpospassthru.md) object or [**CRendererPosPassThru**](crendererpospassthru.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2ffb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2ffb-105">Syntax</span></span>


```C++
STDAPI CreatePosPassThru(
   LPUNKNOWN pAgg,
   BOOL      bRenderer,
   IPin      *pPin,
   IUnknown  **ppPassThru
);
```



## <a name="parameters"></a><span data-ttu-id="b2ffb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2ffb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2ffb-107">*pAgg*</span><span class="sxs-lookup"><span data-stu-id="b2ffb-107">*pAgg*</span></span> 
</dt> <dd>

<span data-ttu-id="b2ffb-108">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="b2ffb-108">Pointer to the owner of this object.</span></span> <span data-ttu-id="b2ffb-109">Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="b2ffb-109">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="b2ffb-110">Caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b2ffb-110">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b2ffb-111">*bRenderer*</span><span class="sxs-lookup"><span data-stu-id="b2ffb-111">*bRenderer*</span></span> 
</dt> <dd>

<span data-ttu-id="b2ffb-112">Valor booliano que especifica se o filtro é um renderizador.</span><span class="sxs-lookup"><span data-stu-id="b2ffb-112">Boolean value that specifies whether the filter is a renderer.</span></span> <span data-ttu-id="b2ffb-113">Use o valor **true** se o filtro for um renderizador ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="b2ffb-113">Use the value **TRUE** if the filter is a renderer, or **FALSE** otherwise.</span></span> <span data-ttu-id="b2ffb-114">Se o valor for **true**, esse método criará uma instância da classe [**CRendererPosPassThru**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="b2ffb-114">If the value is **TRUE**, this method creates an instance of the [**CRendererPosPassThru**](crendererpospassthru.md) class.</span></span> <span data-ttu-id="b2ffb-115">Se o valor for **false**, o método criará uma instância da classe **CPosPassThru** .</span><span class="sxs-lookup"><span data-stu-id="b2ffb-115">If the value is **FALSE**, the method creates an instance of the **CPosPassThru** class.</span></span>

</dd> <dt>

<span data-ttu-id="b2ffb-116">*pPin*</span><span class="sxs-lookup"><span data-stu-id="b2ffb-116">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="b2ffb-117">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) no pino de entrada do filtro.</span><span class="sxs-lookup"><span data-stu-id="b2ffb-117">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface on the filter's input pin.</span></span>

</dd> <dt>

<span data-ttu-id="b2ffb-118">*ppPassThru*</span><span class="sxs-lookup"><span data-stu-id="b2ffb-118">*ppPassThru*</span></span> 
</dt> <dd>

<span data-ttu-id="b2ffb-119">Endereço de uma variável que recebe um ponteiro para a interface **IUnknown** do objeto.</span><span class="sxs-lookup"><span data-stu-id="b2ffb-119">Address of a variable that receives a pointer to the object's **IUnknown** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2ffb-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b2ffb-120">Return value</span></span>

<span data-ttu-id="b2ffb-121">Retornará S \_ OK se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b2ffb-121">Returns S\_OK if successful.</span></span> <span data-ttu-id="b2ffb-122">Caso contrário, retorna um valor **HRESULT** que indica a causa do erro.</span><span class="sxs-lookup"><span data-stu-id="b2ffb-122">Otherwise, returns an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2ffb-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2ffb-123">Remarks</span></span>

<span data-ttu-id="b2ffb-124">Esse método usa a interface [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="b2ffb-124">This method uses the [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) interface to create the object.</span></span> <span data-ttu-id="b2ffb-125">O objeto é carregado dinamicamente do Quartz.dll.</span><span class="sxs-lookup"><span data-stu-id="b2ffb-125">The object is loaded dynamically from Quartz.dll.</span></span>

<span data-ttu-id="b2ffb-126">Se a função for realizada com sucesso, a interface **IUnknown** retornada terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="b2ffb-126">If the function succeeds, the returned **IUnknown** interface has an outstanding reference count.</span></span> <span data-ttu-id="b2ffb-127">O chamador deve liberar a interface.</span><span class="sxs-lookup"><span data-stu-id="b2ffb-127">The caller must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2ffb-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2ffb-128">Requirements</span></span>



| <span data-ttu-id="b2ffb-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2ffb-129">Requirement</span></span> | <span data-ttu-id="b2ffb-130">Valor</span><span class="sxs-lookup"><span data-stu-id="b2ffb-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2ffb-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b2ffb-131">Header</span></span><br/>  | <dl> <span data-ttu-id="b2ffb-132"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2ffb-132"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b2ffb-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b2ffb-133">Library</span></span><br/> | <dl> <span data-ttu-id="b2ffb-134"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b2ffb-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2ffb-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2ffb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2ffb-136">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="b2ffb-136">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 





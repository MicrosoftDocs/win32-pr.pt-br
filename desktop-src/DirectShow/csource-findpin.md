---
description: 'O método FindPin recupera o PIN com o identificador especificado. Esse método implementa o método IBaseFilter:: FindPin.'
ms.assetid: ad593dbf-ca56-4409-ac6e-1b88908c8cee
title: Método CSource. FindPin (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fac8df1e53e4a129b42d1284a19392bc7b58aa2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749241"
---
# <a name="csourcefindpin-method"></a><span data-ttu-id="0fcbd-104">Método CSource. FindPin</span><span class="sxs-lookup"><span data-stu-id="0fcbd-104">CSource.FindPin method</span></span>

<span data-ttu-id="0fcbd-105">O `FindPin` método recupera o PIN com o identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="0fcbd-105">The `FindPin` method retrieves the pin with the specified identifier.</span></span> <span data-ttu-id="0fcbd-106">Esse método implementa o método [**IBaseFilter:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) .</span><span class="sxs-lookup"><span data-stu-id="0fcbd-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fcbd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0fcbd-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="0fcbd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0fcbd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fcbd-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="0fcbd-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="0fcbd-110">Ponteiro para uma cadeia de caracteres terminada em nulo que identifica o PIN.</span><span class="sxs-lookup"><span data-stu-id="0fcbd-110">Pointer to a null-terminated string that identifies the pin.</span></span>

</dd> <dt>

<span data-ttu-id="0fcbd-111">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="0fcbd-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="0fcbd-112">Recebe um ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do PIN.</span><span class="sxs-lookup"><span data-stu-id="0fcbd-112">Receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span> <span data-ttu-id="0fcbd-113">Se o método falhar, \* *ppPin* será definido como **nulo**</span><span class="sxs-lookup"><span data-stu-id="0fcbd-113">If the method fails, \**ppPin* is set to **NULL**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fcbd-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0fcbd-114">Return value</span></span>

<span data-ttu-id="0fcbd-115">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0fcbd-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="0fcbd-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0fcbd-116">Return code</span></span>                                                                                       | <span data-ttu-id="0fcbd-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="0fcbd-117">Description</span></span>                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="0fcbd-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0fcbd-118"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="0fcbd-119">Êxito.</span><span class="sxs-lookup"><span data-stu-id="0fcbd-119">Success.</span></span><br/>                                   |
| <dl> <span data-ttu-id="0fcbd-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="0fcbd-120"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="0fcbd-121">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="0fcbd-121">**NULL** pointer argument.</span></span><br/>                 |
| <dl> <span data-ttu-id="0fcbd-122"><dt>**VFW \_ E \_ não \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="0fcbd-122"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="0fcbd-123">Não foi possível encontrar um PIN com este identificador.</span><span class="sxs-lookup"><span data-stu-id="0fcbd-123">Could not find a pin with this identifier.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0fcbd-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="0fcbd-124">Remarks</span></span>

<span data-ttu-id="0fcbd-125">O primeiro PIN é sempre denominado "1"; o segundo PIN é denominado "2"; e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="0fcbd-125">The first pin is always named "1"; the second pin is named "2"; and so forth.</span></span> <span data-ttu-id="0fcbd-126">Para obter mais informações, consulte [**CSourceStream:: QueryId**](csourcestream-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="0fcbd-126">For more information, see [**CSourceStream::QueryId**](csourcestream-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0fcbd-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fcbd-127">Requirements</span></span>



| <span data-ttu-id="0fcbd-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fcbd-128">Requirement</span></span> | <span data-ttu-id="0fcbd-129">Valor</span><span class="sxs-lookup"><span data-stu-id="0fcbd-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fcbd-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0fcbd-130">Header</span></span><br/>  | <dl> <span data-ttu-id="0fcbd-131"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0fcbd-131"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0fcbd-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0fcbd-132">Library</span></span><br/> | <dl> <span data-ttu-id="0fcbd-133"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0fcbd-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fcbd-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="0fcbd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fcbd-135">**Classe CSource**</span><span class="sxs-lookup"><span data-stu-id="0fcbd-135">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 





---
description: 'O método FindPin Obtém o PIN com o identificador especificado. Esse método implementa o método IBaseFilter:: FindPin.'
ms.assetid: 56ee3e0d-9e3f-4d25-846b-50119b55a122
title: Método CTransformFilter. FindPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1631651932d5adbc49fb59d44291dccea55fd41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747809"
---
# <a name="ctransformfilterfindpin-method"></a><span data-ttu-id="b258e-104">Método CTransformFilter. FindPin</span><span class="sxs-lookup"><span data-stu-id="b258e-104">CTransformFilter.FindPin method</span></span>

<span data-ttu-id="b258e-105">O método **FindPin** Obtém o PIN com o identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="b258e-105">The **FindPin** method gets the pin with the specified identifier.</span></span> <span data-ttu-id="b258e-106">Esse método implementa o método [**IBaseFilter:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) .</span><span class="sxs-lookup"><span data-stu-id="b258e-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b258e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b258e-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="b258e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b258e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b258e-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="b258e-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="b258e-110">Cadeia de caracteres largos que contém o identificador do PIN.</span><span class="sxs-lookup"><span data-stu-id="b258e-110">Wide-character string that contains the pin identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b258e-111">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="b258e-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="b258e-112">Recebe um ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do PIN.</span><span class="sxs-lookup"><span data-stu-id="b258e-112">Receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span> <span data-ttu-id="b258e-113">Se o método falhar, `*ppPin` será definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b258e-113">If the method fails, `*ppPin` is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b258e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b258e-114">Return value</span></span>

<span data-ttu-id="b258e-115">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b258e-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="b258e-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b258e-116">Return code</span></span>                                                                                       | <span data-ttu-id="b258e-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="b258e-117">Description</span></span>                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="b258e-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b258e-118"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="b258e-119">Êxito.</span><span class="sxs-lookup"><span data-stu-id="b258e-119">Success.</span></span><br/>                                   |
| <dl> <span data-ttu-id="b258e-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b258e-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>     | <span data-ttu-id="b258e-121">Memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="b258e-121">Insufficient memory.</span></span><br/>                       |
| <dl> <span data-ttu-id="b258e-122"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="b258e-122"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="b258e-123">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="b258e-123">**NULL** pointer argument.</span></span><br/>                 |
| <dl> <span data-ttu-id="b258e-124"><dt>**VFW \_ E \_ não \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="b258e-124"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="b258e-125">Não foi possível encontrar um PIN com este identificador.</span><span class="sxs-lookup"><span data-stu-id="b258e-125">Could not find a pin with this identifier.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b258e-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="b258e-126">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b258e-127">A implementação desse método não chama [**IPin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) para corresponder ao identificador do PIN.</span><span class="sxs-lookup"><span data-stu-id="b258e-127">The implementation of this method does not call [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) to match the pin identifier.</span></span> <span data-ttu-id="b258e-128">Em vez disso, o método pressupõe que o pino de entrada é denominado "in", e o pino de saída é chamado de "out".</span><span class="sxs-lookup"><span data-stu-id="b258e-128">Instead, the method assumes that the input pin is named "In", and the output pin is named "Out".</span></span> <span data-ttu-id="b258e-129">Se você usar um conjunto diferente de identificadores de PIN, substitua esse método.</span><span class="sxs-lookup"><span data-stu-id="b258e-129">If you use a different set of pin identifiers, override this method.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b258e-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b258e-130">Requirements</span></span>



| <span data-ttu-id="b258e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b258e-131">Requirement</span></span> | <span data-ttu-id="b258e-132">Valor</span><span class="sxs-lookup"><span data-stu-id="b258e-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b258e-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b258e-133">Header</span></span><br/>  | <dl> <span data-ttu-id="b258e-134"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b258e-134"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b258e-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b258e-135">Library</span></span><br/> | <dl> <span data-ttu-id="b258e-136"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b258e-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b258e-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="b258e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b258e-138">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="b258e-138">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 





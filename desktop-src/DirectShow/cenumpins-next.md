---
description: 'O método Next recupera um número especificado de Pins na sequência de enumeração. Esse método implementa o método IEnumPins:: Next.'
ms.assetid: c38fbd32-7d83-43ec-a105-4a7cb515b471
title: Método CEnumPins. Next (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 612dcd638939b34803b7296babf7445a07cdad22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753170"
---
# <a name="cenumpinsnext-method"></a><span data-ttu-id="579bb-104">Método CEnumPins. Next</span><span class="sxs-lookup"><span data-stu-id="579bb-104">CEnumPins.Next method</span></span>

<span data-ttu-id="579bb-105">O método Next recupera um número especificado de Pins na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="579bb-105">The Next method retrieves a specified number of pins in the enumeration sequence.</span></span> <span data-ttu-id="579bb-106">Esse método implementa o método [**IEnumPins:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) .</span><span class="sxs-lookup"><span data-stu-id="579bb-106">This method implements the [**IEnumPins::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="579bb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="579bb-107">Syntax</span></span>


```C++
HRESULT Next(
   ULONG cPins,
   IPin  **ppPins,
   ULONG *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="579bb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="579bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="579bb-109">*cPins*</span><span class="sxs-lookup"><span data-stu-id="579bb-109">*cPins*</span></span> 
</dt> <dd>

<span data-ttu-id="579bb-110">Número de Pins a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="579bb-110">Number of pins to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="579bb-111">*ppPins*</span><span class="sxs-lookup"><span data-stu-id="579bb-111">*ppPins*</span></span> 
</dt> <dd>

<span data-ttu-id="579bb-112">Matriz de tamanho *cPins* que é preenchida com ponteiros [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="579bb-112">Array of size *cPins* that is filled with [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) pointers.</span></span>

</dd> <dt>

<span data-ttu-id="579bb-113">*pcFetched*</span><span class="sxs-lookup"><span data-stu-id="579bb-113">*pcFetched*</span></span> 
</dt> <dd>

<span data-ttu-id="579bb-114">Ponteiro para uma variável que recebe o número de Pins recuperados.</span><span class="sxs-lookup"><span data-stu-id="579bb-114">Pointer to a variable that receives the number of pins retrieved.</span></span> <span data-ttu-id="579bb-115">Pode ser **NULL** se *cPins* for 1.</span><span class="sxs-lookup"><span data-stu-id="579bb-115">Can be **NULL** if *cPins* is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="579bb-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="579bb-116">Return value</span></span>

<span data-ttu-id="579bb-117">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="579bb-117">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="579bb-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="579bb-118">Return code</span></span>                                                                                                | <span data-ttu-id="579bb-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="579bb-119">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="579bb-120"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="579bb-120"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="579bb-121">Não foi possível recuperar quantos Pins forem solicitados.</span><span class="sxs-lookup"><span data-stu-id="579bb-121">Did not retrieve as many pins as requested.</span></span><br/>                                 |
| <dl> <span data-ttu-id="579bb-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="579bb-122"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="579bb-123">Êxito.</span><span class="sxs-lookup"><span data-stu-id="579bb-123">Success.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="579bb-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="579bb-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="579bb-125">Argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="579bb-125">Invalid argument.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="579bb-126"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="579bb-126"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="579bb-127">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="579bb-127">**NULL** pointer argument.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="579bb-128"><dt>**VFW \_ E \_ enum \_ fora \_ de \_ sincronia**</dt></span><span class="sxs-lookup"><span data-stu-id="579bb-128"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="579bb-129">O estado do filtro foi alterado e agora está inconsistente com o enumerador.</span><span class="sxs-lookup"><span data-stu-id="579bb-129">The filter's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="579bb-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="579bb-130">Remarks</span></span>

<span data-ttu-id="579bb-131">Esse método recupera ponteiros para o número especificado de Pins, começando na posição atual na enumeração e os coloca na matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="579bb-131">This method retrieves pointers to the specified number of pins, starting at the current position in the enumeration, and places them in the specified array.</span></span>

<span data-ttu-id="579bb-132">Esse método chama o método [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) do filtro para recuperar os Pins.</span><span class="sxs-lookup"><span data-stu-id="579bb-132">This method calls the filter's [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method to retrieve the pins.</span></span>

<span data-ttu-id="579bb-133">Se o método tiver sucesso, os ponteiros **IPin** terão contagens de referência pendentes.</span><span class="sxs-lookup"><span data-stu-id="579bb-133">If the method succeeds, the **IPin** pointers all have outstanding reference counts.</span></span> <span data-ttu-id="579bb-134">Lembre-se de liberá-los quando terminar.</span><span class="sxs-lookup"><span data-stu-id="579bb-134">Be sure to release them when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="579bb-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="579bb-135">Requirements</span></span>



| <span data-ttu-id="579bb-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="579bb-136">Requirement</span></span> | <span data-ttu-id="579bb-137">Valor</span><span class="sxs-lookup"><span data-stu-id="579bb-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="579bb-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="579bb-138">Header</span></span><br/>  | <dl> <span data-ttu-id="579bb-139"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="579bb-139"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="579bb-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="579bb-140">Library</span></span><br/> | <dl> <span data-ttu-id="579bb-141"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="579bb-141"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="579bb-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="579bb-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="579bb-143">**Classe CEnumPins**</span><span class="sxs-lookup"><span data-stu-id="579bb-143">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 





---
description: 'O método QueryInternalConnections recupera os PINs que estão conectados internamente a esse PIN (dentro do filtro). Esse método implementa o método IPin:: QueryInternalConnections.'
ms.assetid: 08344fc5-38b2-4dbe-8ef9-30d2fcd64187
title: Método CBasePin. QueryInternalConnections (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryInternalConnections
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99a636295fc87347a1735ab028b6de342e887d55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752902"
---
# <a name="cbasepinqueryinternalconnections-method"></a><span data-ttu-id="03a81-104">Método CBasePin. QueryInternalConnections</span><span class="sxs-lookup"><span data-stu-id="03a81-104">CBasePin.QueryInternalConnections method</span></span>

<span data-ttu-id="03a81-105">O `QueryInternalConnections` método recupera os PINs que estão conectados internamente a esse PIN (dentro do filtro).</span><span class="sxs-lookup"><span data-stu-id="03a81-105">The `QueryInternalConnections` method retrieves the pins that are connected internally to this pin (within the filter).</span></span> <span data-ttu-id="03a81-106">Esse método implementa o método [**IPin:: QueryInternalConnections**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) .</span><span class="sxs-lookup"><span data-stu-id="03a81-106">This method implements the [**IPin::QueryInternalConnections**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="03a81-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03a81-107">Syntax</span></span>


```C++
HRESULT QueryInternalConnections(
   IPin  *apPin,
   ULONG *nPin
);
```



## <a name="parameters"></a><span data-ttu-id="03a81-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="03a81-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03a81-109">*apPin*</span><span class="sxs-lookup"><span data-stu-id="03a81-109">*apPin*</span></span> 
</dt> <dd>

<span data-ttu-id="03a81-110">Endereço de uma matriz de ponteiros [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="03a81-110">Address of an array of [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) pointers.</span></span>

</dd> <dt>

<span data-ttu-id="03a81-111">*nPin*</span><span class="sxs-lookup"><span data-stu-id="03a81-111">*nPin*</span></span> 
</dt> <dd>

<span data-ttu-id="03a81-112">Em entrada, especifica o tamanho da matriz.</span><span class="sxs-lookup"><span data-stu-id="03a81-112">On input, specifies the size of the array.</span></span> <span data-ttu-id="03a81-113">Quando o método retorna, o valor é definido como o número de ponteiros retornados na matriz.</span><span class="sxs-lookup"><span data-stu-id="03a81-113">When the method returns, the value is set to the number of pointers returned in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03a81-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="03a81-114">Return value</span></span>

<span data-ttu-id="03a81-115">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="03a81-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="03a81-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="03a81-116">Return code</span></span>                                                                               | <span data-ttu-id="03a81-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="03a81-117">Description</span></span>                         |
|-------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="03a81-118"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="03a81-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="03a81-119">Tamanho de matriz insuficiente.</span><span class="sxs-lookup"><span data-stu-id="03a81-119">Insufficient array size.</span></span><br/> |
| <dl> <span data-ttu-id="03a81-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="03a81-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="03a81-121">Êxito.</span><span class="sxs-lookup"><span data-stu-id="03a81-121">Success.</span></span><br/>                 |
| <dl> <span data-ttu-id="03a81-122"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="03a81-122"><dt>**E\_FAIL**</dt></span></span> </dl>    | <span data-ttu-id="03a81-123">Falha.</span><span class="sxs-lookup"><span data-stu-id="03a81-123">Failure.</span></span><br/>                 |
| <dl> <span data-ttu-id="03a81-124"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="03a81-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="03a81-125">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="03a81-125">Not implemented.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="03a81-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="03a81-126">Remarks</span></span>

<span data-ttu-id="03a81-127">Em alguns filtros, os Pins de entrada correspondem a Pins de saída específicos.</span><span class="sxs-lookup"><span data-stu-id="03a81-127">On some filters, input pins correspond to particular output pins.</span></span> <span data-ttu-id="03a81-128">Para cada PIN, esse método preenche uma matriz com ponteiros para os Pins correspondentes.</span><span class="sxs-lookup"><span data-stu-id="03a81-128">For each pin, this method fills an array with pointers to the corresponding pins.</span></span> <span data-ttu-id="03a81-129">Se cada PIN de entrada fornecer dados para cada pino de saída, retornará E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="03a81-129">If every input pin provides data for every output pin, return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="03a81-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03a81-130">Requirements</span></span>



| <span data-ttu-id="03a81-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="03a81-131">Requirement</span></span> | <span data-ttu-id="03a81-132">Valor</span><span class="sxs-lookup"><span data-stu-id="03a81-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03a81-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="03a81-133">Header</span></span><br/>  | <dl> <span data-ttu-id="03a81-134"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03a81-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="03a81-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="03a81-135">Library</span></span><br/> | <dl> <span data-ttu-id="03a81-136"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="03a81-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03a81-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="03a81-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03a81-138">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="03a81-138">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





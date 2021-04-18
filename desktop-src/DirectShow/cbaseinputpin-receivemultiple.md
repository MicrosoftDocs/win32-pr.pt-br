---
description: 'O método ReceiveMultiple recebe uma matriz de amostras. Esse método implementa o método IMemInputPin:: ReceiveMultiple.'
ms.assetid: 21e757c7-f623-4ccb-8e37-512ee4dd7aa7
title: Método CBaseInputPin. ReceiveMultiple (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5725b7d8b70c8f7c61eb44231812997a903ba41a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811763"
---
# <a name="cbaseinputpinreceivemultiple-method"></a><span data-ttu-id="9c8a5-104">Método CBaseInputPin. ReceiveMultiple</span><span class="sxs-lookup"><span data-stu-id="9c8a5-104">CBaseInputPin.ReceiveMultiple method</span></span>

<span data-ttu-id="9c8a5-105">O `ReceiveMultiple` método recebe uma matriz de amostras.</span><span class="sxs-lookup"><span data-stu-id="9c8a5-105">The `ReceiveMultiple` method receives an array of samples.</span></span> <span data-ttu-id="9c8a5-106">Esse método implementa o método [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) .</span><span class="sxs-lookup"><span data-stu-id="9c8a5-106">This method implements the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c8a5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9c8a5-107">Syntax</span></span>


```C++
HRESULT ReceiveMultiple(
   IMediaSample **pSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a><span data-ttu-id="9c8a5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9c8a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c8a5-109">*pSamples*</span><span class="sxs-lookup"><span data-stu-id="9c8a5-109">*pSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="9c8a5-110">Endereço de uma matriz de ponteiros [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) , de tamanho *nSamples*.</span><span class="sxs-lookup"><span data-stu-id="9c8a5-110">Address of an array of [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pointers, of size *nSamples*.</span></span>

</dd> <dt>

<span data-ttu-id="9c8a5-111">*nSamples*</span><span class="sxs-lookup"><span data-stu-id="9c8a5-111">*nSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="9c8a5-112">Número de amostras a serem processadas.</span><span class="sxs-lookup"><span data-stu-id="9c8a5-112">Number of samples to process.</span></span>

</dd> <dt>

<span data-ttu-id="9c8a5-113">*nSamplesProcessed*</span><span class="sxs-lookup"><span data-stu-id="9c8a5-113">*nSamplesProcessed*</span></span> 
</dt> <dd>

<span data-ttu-id="9c8a5-114">Ponteiro para uma variável que recebe o número de amostras que foram processadas.</span><span class="sxs-lookup"><span data-stu-id="9c8a5-114">Pointer to a variable that receives the number of samples that were processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c8a5-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9c8a5-115">Return value</span></span>

<span data-ttu-id="9c8a5-116">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9c8a5-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="9c8a5-117">Os valores possíveis incluem os listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9c8a5-117">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="9c8a5-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9c8a5-118">Return code</span></span>                                                                                             | <span data-ttu-id="9c8a5-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="9c8a5-119">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="9c8a5-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9c8a5-120"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="9c8a5-121">Êxito.</span><span class="sxs-lookup"><span data-stu-id="9c8a5-121">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="9c8a5-122"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="9c8a5-122"><dt>**S\_FALSE**</dt></span></span> </dl>                 | <span data-ttu-id="9c8a5-123">O PIN está sendo liberado no momento; o exemplo foi rejeitado.</span><span class="sxs-lookup"><span data-stu-id="9c8a5-123">Pin is currently flushing; sample was rejected.</span></span><br/> |
| <dl> <span data-ttu-id="9c8a5-124"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="9c8a5-124"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="9c8a5-125">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="9c8a5-125">**NULL** pointer argument.</span></span><br/>                      |
| <dl> <span data-ttu-id="9c8a5-126"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="9c8a5-126"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="9c8a5-127">Tipo de mídia inválido.</span><span class="sxs-lookup"><span data-stu-id="9c8a5-127">Invalid media type.</span></span><br/>                             |
| <dl> <span data-ttu-id="9c8a5-128"><dt>**VFW \_ E \_ erro de tempo de execução \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9c8a5-128"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl>   | <span data-ttu-id="9c8a5-129">Ocorreu um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="9c8a5-129">A run-time error occurred.</span></span><br/>                      |
| <dl> <span data-ttu-id="9c8a5-130"><dt>**VFW \_ E \_ estado incorreto \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9c8a5-130"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>     | <span data-ttu-id="9c8a5-131">O PIN foi interrompido.</span><span class="sxs-lookup"><span data-stu-id="9c8a5-131">The pin is stopped.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="9c8a5-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c8a5-132">Remarks</span></span>

<span data-ttu-id="9c8a5-133">Esse método se comporta como o método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) , mas recebe uma matriz de amostras.</span><span class="sxs-lookup"><span data-stu-id="9c8a5-133">This method behaves like the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method, but receives an array of samples.</span></span> <span data-ttu-id="9c8a5-134">Na classe base, o método percorre a matriz e chama **Receive** com cada exemplo.</span><span class="sxs-lookup"><span data-stu-id="9c8a5-134">In the base class, the method loops through the array and calls **Receive** with each sample.</span></span> <span data-ttu-id="9c8a5-135">Substitua essa função se o filtro puder processar lotes de amostras com mais eficiência do que processá-los um de cada vez.</span><span class="sxs-lookup"><span data-stu-id="9c8a5-135">Override this function if your filter can process batches of samples more efficiently than processing them one at a time.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c8a5-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c8a5-136">Requirements</span></span>



| <span data-ttu-id="9c8a5-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c8a5-137">Requirement</span></span> | <span data-ttu-id="9c8a5-138">Valor</span><span class="sxs-lookup"><span data-stu-id="9c8a5-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c8a5-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9c8a5-139">Header</span></span><br/>  | <dl> <span data-ttu-id="9c8a5-140"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9c8a5-140"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9c8a5-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9c8a5-141">Library</span></span><br/> | <dl> <span data-ttu-id="9c8a5-142"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="9c8a5-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c8a5-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c8a5-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c8a5-144">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="9c8a5-144">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 





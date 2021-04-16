---
description: O método QueryId recupera um identificador para o PIN.
ms.assetid: 6050292e-6203-4a79-87bf-47394624cb32
title: Método CSourceStream. QueryId (origem. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 267748fe4ce1eeec4650544a2f72069df897a366
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758529"
---
# <a name="csourcestreamqueryid-method"></a><span data-ttu-id="424f1-103">Método CSourceStream. QueryId</span><span class="sxs-lookup"><span data-stu-id="424f1-103">CSourceStream.QueryId method</span></span>

<span data-ttu-id="424f1-104">O `QueryId` método recupera um identificador para o PIN.</span><span class="sxs-lookup"><span data-stu-id="424f1-104">The `QueryId` method retrieves an identifier for the pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="424f1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="424f1-105">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="424f1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="424f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="424f1-107">*Id*</span><span class="sxs-lookup"><span data-stu-id="424f1-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="424f1-108">Ponteiro para uma variável que recebe uma cadeia de caracteres que contém o identificador do PIN.</span><span class="sxs-lookup"><span data-stu-id="424f1-108">Pointer to a variable that receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="424f1-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="424f1-109">Return value</span></span>

<span data-ttu-id="424f1-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="424f1-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="424f1-111">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="424f1-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="424f1-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="424f1-112">Return code</span></span>                                                                                       | <span data-ttu-id="424f1-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="424f1-113">Description</span></span>                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="424f1-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="424f1-114"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="424f1-115">Êxito.</span><span class="sxs-lookup"><span data-stu-id="424f1-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="424f1-116"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="424f1-116"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>     | <span data-ttu-id="424f1-117">Memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="424f1-117">Insufficient memory.</span></span><br/>             |
| <dl> <span data-ttu-id="424f1-118"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="424f1-118"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="424f1-119">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="424f1-119">**NULL** pointer argument.</span></span><br/>       |
| <dl> <span data-ttu-id="424f1-120"><dt>**VFW \_ E \_ não \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="424f1-120"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="424f1-121">O PIN não foi encontrado no filtro.</span><span class="sxs-lookup"><span data-stu-id="424f1-121">Pin was not found on the filter.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="424f1-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="424f1-122">Remarks</span></span>

<span data-ttu-id="424f1-123">Esse método implementa o método [**IPin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .</span><span class="sxs-lookup"><span data-stu-id="424f1-123">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span> <span data-ttu-id="424f1-124">Para construir uma cadeia de caracteres de identificador, o PIN chama o método [**CSource:: FindPinNumber**](csource-findpinnumber.md) como o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="424f1-124">To construct an identifier string, the pin calls the [**CSource::FindPinNumber**](csource-findpinnumber.md) method with itself as the parameter.</span></span> <span data-ttu-id="424f1-125">O método **FindPinNumber** retorna o número do PIN, indexado de zero.</span><span class="sxs-lookup"><span data-stu-id="424f1-125">The **FindPinNumber** method returns the pin number, indexed from zero.</span></span> <span data-ttu-id="424f1-126">`QueryId` incrementa o valor de retorno em um e converte o resultado em uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="424f1-126">`QueryId` increments the return value by one and converts the result to a string.</span></span> <span data-ttu-id="424f1-127">Por exemplo, o primeiro PIN se torna "1"; o segundo PIN se torna "2"; e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="424f1-127">For example, the first pin becomes "1"; the second pin becomes "2"; and so forth.</span></span>

<span data-ttu-id="424f1-128">Se esse método retornar VFW \_ e \_ não \_ for encontrado, ele indicará que a matriz de Pins do filtro é inválida, supostamente causada por um bug no filtro.</span><span class="sxs-lookup"><span data-stu-id="424f1-128">If this method returns VFW\_E\_NOT\_FOUND, it indicates that the filter's array of pins is invalid, presumably caused by a bug in the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="424f1-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="424f1-129">Requirements</span></span>



| <span data-ttu-id="424f1-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="424f1-130">Requirement</span></span> | <span data-ttu-id="424f1-131">Valor</span><span class="sxs-lookup"><span data-stu-id="424f1-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="424f1-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="424f1-132">Header</span></span><br/>  | <dl> <span data-ttu-id="424f1-133"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="424f1-133"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="424f1-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="424f1-134">Library</span></span><br/> | <dl> <span data-ttu-id="424f1-135"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="424f1-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="424f1-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="424f1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="424f1-137">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="424f1-137">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 





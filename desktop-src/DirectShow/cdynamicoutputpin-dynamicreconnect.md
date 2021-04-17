---
description: O método DynamicReconnect executa uma reconexão dinâmica com um novo tipo de mídia. A reconexão pode ocorrer enquanto o grafo de filtro está em execução.
ms.assetid: 1fe9f1cc-1f5d-407e-8c80-fea6cd1cb16f
title: Método CDynamicOutputPin. DynamicReconnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DynamicReconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd595748380a35f74e591283ed3d03273c683e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748812"
---
# <a name="cdynamicoutputpindynamicreconnect-method"></a><span data-ttu-id="02bb5-104">Método CDynamicOutputPin. DynamicReconnect</span><span class="sxs-lookup"><span data-stu-id="02bb5-104">CDynamicOutputPin.DynamicReconnect method</span></span>

<span data-ttu-id="02bb5-105">O `DynamicReconnect` método executa uma reconexão dinâmica com um novo tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="02bb5-105">The `DynamicReconnect` method performs a dynamic reconnection with a new media type.</span></span> <span data-ttu-id="02bb5-106">A reconexão pode ocorrer enquanto o grafo de filtro está em execução.</span><span class="sxs-lookup"><span data-stu-id="02bb5-106">The reconnection can occur while the filter graph is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="02bb5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02bb5-107">Syntax</span></span>


```C++
HRESULT DynamicReconnect(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="02bb5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02bb5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02bb5-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="02bb5-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="02bb5-110">Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="02bb5-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02bb5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="02bb5-111">Return value</span></span>

<span data-ttu-id="02bb5-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="02bb5-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="02bb5-113">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="02bb5-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="02bb5-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="02bb5-114">Return code</span></span>                                                                            | <span data-ttu-id="02bb5-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="02bb5-115">Description</span></span>                                                                                                                                         |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="02bb5-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="02bb5-116"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="02bb5-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="02bb5-117">Success.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="02bb5-118"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="02bb5-118"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="02bb5-119">Falha.</span><span class="sxs-lookup"><span data-stu-id="02bb5-119">Failure.</span></span> <span data-ttu-id="02bb5-120">Possivelmente o filtro proprietário não chamou o método [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) .</span><span class="sxs-lookup"><span data-stu-id="02bb5-120">Possibly the owning filter did not call the [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="02bb5-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="02bb5-121">Remarks</span></span>

<span data-ttu-id="02bb5-122">Esse método deve ser chamado do mesmo thread que entrega dados ao PIN.</span><span class="sxs-lookup"><span data-stu-id="02bb5-122">This method must be called from the same thread that delivers data to the pin.</span></span> <span data-ttu-id="02bb5-123">Depois que esse método é chamado, os exemplos com o tipo de mídia antigo não podem ser entregues.</span><span class="sxs-lookup"><span data-stu-id="02bb5-123">Once this method is called, samples with the old media type cannot be delivered.</span></span> <span data-ttu-id="02bb5-124">O chamador deve garantir que nenhuma amostra antiga esteja pendente.</span><span class="sxs-lookup"><span data-stu-id="02bb5-124">The caller must ensure that no old samples are pending.</span></span>

<span data-ttu-id="02bb5-125">Chame [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) antes de chamar este método.</span><span class="sxs-lookup"><span data-stu-id="02bb5-125">Call [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="02bb5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02bb5-126">Requirements</span></span>



| <span data-ttu-id="02bb5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="02bb5-127">Requirement</span></span> | <span data-ttu-id="02bb5-128">Valor</span><span class="sxs-lookup"><span data-stu-id="02bb5-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02bb5-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="02bb5-129">Header</span></span><br/>  | <dl> <span data-ttu-id="02bb5-130"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="02bb5-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="02bb5-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="02bb5-131">Library</span></span><br/> | <dl> <span data-ttu-id="02bb5-132"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="02bb5-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02bb5-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="02bb5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02bb5-134">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="02bb5-134">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 





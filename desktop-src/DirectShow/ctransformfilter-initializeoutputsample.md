---
description: O método InitializeOutputSample recupera um novo exemplo de saída e inicializa-o.
ms.assetid: a4f8f514-cf1a-4f8f-ac17-17378705c2ea
title: CTransformFilter.Inimétodo tializeOutputSample (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.InitializeOutputSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: efe7e62936c6feb1984a339a67783cdbc1e4f124
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748191"
---
# <a name="ctransformfilterinitializeoutputsample-method"></a><span data-ttu-id="48a86-103">CTransformFilter.Inimétodo tializeOutputSample</span><span class="sxs-lookup"><span data-stu-id="48a86-103">CTransformFilter.InitializeOutputSample method</span></span>

<span data-ttu-id="48a86-104">O `InitializeOutputSample` método recupera um novo exemplo de saída e inicializa-o.</span><span class="sxs-lookup"><span data-stu-id="48a86-104">The `InitializeOutputSample` method retrieves a new output sample and initializes it.</span></span>

## <a name="syntax"></a><span data-ttu-id="48a86-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="48a86-105">Syntax</span></span>


```C++
HRESULT InitializeOutputSample(
   IMediaSample *pSample,
   IMediaSample **ppOutSample
);
```



## <a name="parameters"></a><span data-ttu-id="48a86-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48a86-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48a86-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="48a86-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="48a86-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo de entrada.</span><span class="sxs-lookup"><span data-stu-id="48a86-108">Pointer to the input sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="48a86-109">*ppOutSample*</span><span class="sxs-lookup"><span data-stu-id="48a86-109">*ppOutSample*</span></span> 
</dt> <dd>

<span data-ttu-id="48a86-110">Recebe um ponteiro para a interface **IMediaSample** da amostra de saída.</span><span class="sxs-lookup"><span data-stu-id="48a86-110">Receives a pointer to the output sample's **IMediaSample** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48a86-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="48a86-111">Return value</span></span>

<span data-ttu-id="48a86-112">Retorna S \_ OK ou outro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="48a86-112">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="48a86-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="48a86-113">Remarks</span></span>

<span data-ttu-id="48a86-114">Esse método é chamado pelo método [**CTransformFilter:: Receive**](ctransformfilter-receive.md) para preparar o exemplo de saída.</span><span class="sxs-lookup"><span data-stu-id="48a86-114">This method is called by the [**CTransformFilter::Receive**](ctransformfilter-receive.md) method to prepare the output sample.</span></span> <span data-ttu-id="48a86-115">Em geral, você não precisa chamar esse método em sua classe derivada, a menos que substitua o método **Receive** .</span><span class="sxs-lookup"><span data-stu-id="48a86-115">Generally you do not have to call this method in your derived class, unless you override the **Receive** method.</span></span>

<span data-ttu-id="48a86-116">Esse método recupera uma nova amostra do alocador do pino de saída.</span><span class="sxs-lookup"><span data-stu-id="48a86-116">This method retrieves a new sample from the output pin's allocator.</span></span> <span data-ttu-id="48a86-117">Em seguida, ele copia as propriedades de exemplo do exemplo de entrada para o exemplo de saída.</span><span class="sxs-lookup"><span data-stu-id="48a86-117">Then it copies the sample properties from the input sample to the output sample.</span></span> <span data-ttu-id="48a86-118">As propriedades de exemplo são definidas na estrutura de [**\_ \_ Propriedades am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .</span><span class="sxs-lookup"><span data-stu-id="48a86-118">The sample properties are defined in the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="48a86-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48a86-119">Requirements</span></span>



| <span data-ttu-id="48a86-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="48a86-120">Requirement</span></span> | <span data-ttu-id="48a86-121">Valor</span><span class="sxs-lookup"><span data-stu-id="48a86-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48a86-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="48a86-122">Header</span></span><br/>  | <dl> <span data-ttu-id="48a86-123"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="48a86-123"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="48a86-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="48a86-124">Library</span></span><br/> | <dl> <span data-ttu-id="48a86-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="48a86-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48a86-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="48a86-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48a86-127">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="48a86-127">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 





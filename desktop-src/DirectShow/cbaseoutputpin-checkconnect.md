---
description: O método CheckConnect determina se uma conexão de PIN é adequada.
ms.assetid: 50ab59ad-8ff7-4d7b-add3-b59203d93307
title: Método CBaseOutputPin. CheckConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3274e47e9a77d86f350c17aaca04ec0cdb95ef3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751708"
---
# <a name="cbaseoutputpincheckconnect-method"></a><span data-ttu-id="eb4d5-103">Método CBaseOutputPin. CheckConnect</span><span class="sxs-lookup"><span data-stu-id="eb4d5-103">CBaseOutputPin.CheckConnect method</span></span>

<span data-ttu-id="eb4d5-104">O `CheckConnect` método determina se uma conexão de PIN é adequada.</span><span class="sxs-lookup"><span data-stu-id="eb4d5-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb4d5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb4d5-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="eb4d5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb4d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb4d5-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="eb4d5-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="eb4d5-108">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="eb4d5-108">Pointer to the input pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb4d5-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eb4d5-109">Return value</span></span>

<span data-ttu-id="eb4d5-110">Retorna um dos valores de **HRESULT** a seguir.</span><span class="sxs-lookup"><span data-stu-id="eb4d5-110">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="eb4d5-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="eb4d5-111">Return code</span></span>                                                                                               | <span data-ttu-id="eb4d5-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="eb4d5-112">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="eb4d5-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="eb4d5-113"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="eb4d5-114">Êxito.</span><span class="sxs-lookup"><span data-stu-id="eb4d5-114">Success.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="eb4d5-115"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="eb4d5-115"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>             | <span data-ttu-id="eb4d5-116">O PIN de entrada não dá suporte a [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin).</span><span class="sxs-lookup"><span data-stu-id="eb4d5-116">Input pin does not support [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin).</span></span><br/> |
| <dl> <span data-ttu-id="eb4d5-117"><dt>**VFW \_ E \_ direção inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eb4d5-117"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="eb4d5-118">As direções do PIN não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="eb4d5-118">Pin directions are not compatible.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="eb4d5-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb4d5-119">Remarks</span></span>

<span data-ttu-id="eb4d5-120">Esse método chama o método [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) de classe base e, em seguida, consulta o pino de entrada para sua interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="eb4d5-120">This method calls the base-class [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method, and then queries the input pin for its [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb4d5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb4d5-121">Requirements</span></span>



| <span data-ttu-id="eb4d5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb4d5-122">Requirement</span></span> | <span data-ttu-id="eb4d5-123">Valor</span><span class="sxs-lookup"><span data-stu-id="eb4d5-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb4d5-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eb4d5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="eb4d5-125"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb4d5-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="eb4d5-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eb4d5-126">Library</span></span><br/> | <dl> <span data-ttu-id="eb4d5-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="eb4d5-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb4d5-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb4d5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb4d5-129">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="eb4d5-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 





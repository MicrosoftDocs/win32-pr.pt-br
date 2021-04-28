---
description: Método CBaseOutputPin. CheckConnect – o método CheckConnect determina se uma conexão de PIN é adequada.
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
ms.openlocfilehash: 7ea5ad32de18046f3d23145d82e971391c3e304c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096184"
---
# <a name="cbaseoutputpincheckconnect-method"></a><span data-ttu-id="2f93c-103">Método CBaseOutputPin. CheckConnect</span><span class="sxs-lookup"><span data-stu-id="2f93c-103">CBaseOutputPin.CheckConnect method</span></span>

<span data-ttu-id="2f93c-104">O `CheckConnect` método determina se uma conexão de PIN é adequada.</span><span class="sxs-lookup"><span data-stu-id="2f93c-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f93c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f93c-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="2f93c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f93c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f93c-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="2f93c-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="2f93c-108">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="2f93c-108">Pointer to the input pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f93c-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2f93c-109">Return value</span></span>

<span data-ttu-id="2f93c-110">Retorna um dos valores de **HRESULT** a seguir.</span><span class="sxs-lookup"><span data-stu-id="2f93c-110">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="2f93c-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2f93c-111">Return code</span></span>                                                                                               | <span data-ttu-id="2f93c-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="2f93c-112">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2f93c-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2f93c-113"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="2f93c-114">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="2f93c-114">Success.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="2f93c-115"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="2f93c-115"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>             | <span data-ttu-id="2f93c-116">O PIN de entrada não dá suporte a [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin).</span><span class="sxs-lookup"><span data-stu-id="2f93c-116">Input pin does not support [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin).</span></span><br/> |
| <dl> <span data-ttu-id="2f93c-117"><dt>**VFW \_ E \_ direção inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2f93c-117"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="2f93c-118">As direções do PIN não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="2f93c-118">Pin directions are not compatible.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="2f93c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f93c-119">Remarks</span></span>

<span data-ttu-id="2f93c-120">Esse método chama o método [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) de classe base e, em seguida, consulta o pino de entrada para sua interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="2f93c-120">This method calls the base-class [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method, and then queries the input pin for its [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f93c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f93c-121">Requirements</span></span>



| <span data-ttu-id="2f93c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f93c-122">Requirement</span></span> | <span data-ttu-id="2f93c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="2f93c-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f93c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2f93c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2f93c-125"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f93c-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2f93c-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2f93c-126">Library</span></span><br/> | <dl> <span data-ttu-id="2f93c-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="2f93c-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f93c-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2f93c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f93c-129">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="2f93c-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 





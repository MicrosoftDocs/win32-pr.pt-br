---
description: O método CheckConnect determina se uma conexão de PIN é adequada.
ms.assetid: 3dae5c6d-720e-4445-b601-3bdfe32f4c21
title: Método CTransformOutputPin. CheckConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9a20eb8d3e20679cb8805d3a1cd8e167ef0bfd5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757637"
---
# <a name="ctransformoutputpincheckconnect-method"></a><span data-ttu-id="b8bb4-103">Método CTransformOutputPin. CheckConnect</span><span class="sxs-lookup"><span data-stu-id="b8bb4-103">CTransformOutputPin.CheckConnect method</span></span>

<span data-ttu-id="b8bb4-104">O `CheckConnect` método determina se uma conexão de PIN é adequada.</span><span class="sxs-lookup"><span data-stu-id="b8bb4-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8bb4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8bb4-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="b8bb4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8bb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8bb4-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="b8bb4-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="b8bb4-108">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de saída.</span><span class="sxs-lookup"><span data-stu-id="b8bb4-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8bb4-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b8bb4-109">Return value</span></span>

<span data-ttu-id="b8bb4-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b8bb4-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b8bb4-111">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="b8bb4-111">Possible values include the following.</span></span>



| <span data-ttu-id="b8bb4-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b8bb4-112">Return code</span></span>                                                                                  | <span data-ttu-id="b8bb4-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="b8bb4-113">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="b8bb4-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b8bb4-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="b8bb4-115">Êxito.</span><span class="sxs-lookup"><span data-stu-id="b8bb4-115">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="b8bb4-116"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="b8bb4-116"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="b8bb4-117">O pino de entrada do filtro não está conectado.</span><span class="sxs-lookup"><span data-stu-id="b8bb4-117">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b8bb4-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8bb4-118">Remarks</span></span>

<span data-ttu-id="b8bb4-119">Esse método substitui o método [**CBaseOutputPin:: CheckConnect**](cbaseoutputpin-checkconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="b8bb4-119">This method overrides the [**CBaseOutputPin::CheckConnect**](cbaseoutputpin-checkconnect.md) method.</span></span> <span data-ttu-id="b8bb4-120">Ele chama o método [**CTransformFilter:: CheckConnect**](ctransformfilter-checkconnect.md) do filtro, que retorna s \_ OK na classe base.</span><span class="sxs-lookup"><span data-stu-id="b8bb4-120">It calls the filter's [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="b8bb4-121">A classe derivada pode substituir o método **CTransformFilter:: CheckConnect** para executar verificações adicionais.</span><span class="sxs-lookup"><span data-stu-id="b8bb4-121">The derived class can override the **CTransformFilter::CheckConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8bb4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8bb4-122">Requirements</span></span>



| <span data-ttu-id="b8bb4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8bb4-123">Requirement</span></span> | <span data-ttu-id="b8bb4-124">Valor</span><span class="sxs-lookup"><span data-stu-id="b8bb4-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8bb4-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b8bb4-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b8bb4-126"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8bb4-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b8bb4-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b8bb4-127">Library</span></span><br/> | <dl> <span data-ttu-id="b8bb4-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b8bb4-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





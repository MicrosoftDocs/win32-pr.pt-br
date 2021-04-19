---
description: O método CompleteConnect conclui uma conexão com outro PIN.
ms.assetid: 568cee55-b9ea-4fc2-ac9d-0080b7de9790
title: Método CTransformInputPin. CompleteConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 455517968481b9333fbeba590aca644b34b2f5be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768612"
---
# <a name="ctransforminputpincompleteconnect-method"></a><span data-ttu-id="b95a9-103">Método CTransformInputPin. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="b95a9-103">CTransformInputPin.CompleteConnect method</span></span>

<span data-ttu-id="b95a9-104">O `CompleteConnect` método conclui uma conexão com outro PIN.</span><span class="sxs-lookup"><span data-stu-id="b95a9-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="b95a9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b95a9-105">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="b95a9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b95a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b95a9-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="b95a9-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="b95a9-108">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do outro PIN.</span><span class="sxs-lookup"><span data-stu-id="b95a9-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b95a9-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b95a9-109">Return value</span></span>

<span data-ttu-id="b95a9-110">Retorna S \_ OK ou outro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b95a9-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b95a9-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b95a9-111">Remarks</span></span>

<span data-ttu-id="b95a9-112">Esse método substitui o método [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="b95a9-112">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span> <span data-ttu-id="b95a9-113">Ele chama o método [**CTransformFilter:: CompleteConnect**](ctransformfilter-completeconnect.md) do filtro, que retorna s \_ OK na classe base.</span><span class="sxs-lookup"><span data-stu-id="b95a9-113">It calls the filter's [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="b95a9-114">A classe derivada pode substituir o método **CTransformFilter:: CompleteConnect** para executar verificações adicionais.</span><span class="sxs-lookup"><span data-stu-id="b95a9-114">The derived class can override the **CTransformFilter::CompleteConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="b95a9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b95a9-115">Requirements</span></span>



| <span data-ttu-id="b95a9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b95a9-116">Requirement</span></span> | <span data-ttu-id="b95a9-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b95a9-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b95a9-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b95a9-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b95a9-119"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b95a9-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b95a9-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b95a9-120">Library</span></span><br/> | <dl> <span data-ttu-id="b95a9-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b95a9-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





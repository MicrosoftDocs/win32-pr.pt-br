---
description: Método CTransformInputPin. CompleteConnect – o método CompleteConnect conclui uma conexão com outro PIN.
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
ms.openlocfilehash: 20f378479209b2614116ba25f51950923358f1b2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085004"
---
# <a name="ctransforminputpincompleteconnect-method"></a><span data-ttu-id="e45c6-103">Método CTransformInputPin. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="e45c6-103">CTransformInputPin.CompleteConnect method</span></span>

<span data-ttu-id="e45c6-104">O `CompleteConnect` método conclui uma conexão com outro PIN.</span><span class="sxs-lookup"><span data-stu-id="e45c6-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="e45c6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e45c6-105">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="e45c6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e45c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e45c6-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="e45c6-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="e45c6-108">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do outro PIN.</span><span class="sxs-lookup"><span data-stu-id="e45c6-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e45c6-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e45c6-109">Return value</span></span>

<span data-ttu-id="e45c6-110">Retorna S \_ OK ou outro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e45c6-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e45c6-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e45c6-111">Remarks</span></span>

<span data-ttu-id="e45c6-112">Esse método substitui o método [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="e45c6-112">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span> <span data-ttu-id="e45c6-113">Ele chama o método [**CTransformFilter:: CompleteConnect**](ctransformfilter-completeconnect.md) do filtro, que retorna s \_ OK na classe base.</span><span class="sxs-lookup"><span data-stu-id="e45c6-113">It calls the filter's [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="e45c6-114">A classe derivada pode substituir o método **CTransformFilter:: CompleteConnect** para executar verificações adicionais.</span><span class="sxs-lookup"><span data-stu-id="e45c6-114">The derived class can override the **CTransformFilter::CompleteConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="e45c6-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e45c6-115">Requirements</span></span>



| <span data-ttu-id="e45c6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e45c6-116">Requirement</span></span> | <span data-ttu-id="e45c6-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e45c6-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e45c6-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e45c6-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e45c6-119"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e45c6-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e45c6-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e45c6-120">Library</span></span><br/> | <dl> <span data-ttu-id="e45c6-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e45c6-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





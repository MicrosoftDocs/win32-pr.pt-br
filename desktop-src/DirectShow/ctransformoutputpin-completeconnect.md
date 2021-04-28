---
description: Método CTransformOutputPin. CompleteConnect – o método CompleteConnect conclui uma conexão com outro PIN.
ms.assetid: 14bc48bc-ddfb-4491-8d5b-9e5ac601ba04
title: Método CTransformOutputPin. CompleteConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ab3d7e56473094b31c0d97d0e15c083ff61a21d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094914"
---
# <a name="ctransformoutputpincompleteconnect-method"></a><span data-ttu-id="e4b5a-103">Método CTransformOutputPin. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="e4b5a-103">CTransformOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="e4b5a-104">O `CompleteConnect` método conclui uma conexão com outro PIN.</span><span class="sxs-lookup"><span data-stu-id="e4b5a-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4b5a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4b5a-105">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="e4b5a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4b5a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4b5a-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="e4b5a-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="e4b5a-108">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do outro PIN.</span><span class="sxs-lookup"><span data-stu-id="e4b5a-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4b5a-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e4b5a-109">Return value</span></span>

<span data-ttu-id="e4b5a-110">Retorna S \_ OK ou outro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e4b5a-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4b5a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4b5a-111">Remarks</span></span>

<span data-ttu-id="e4b5a-112">Esse método substitui o método [**CBaseOutputPin:: CompleteConnect**](cbaseoutputpin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="e4b5a-112">This method overrides the [**CBaseOutputPin::CompleteConnect**](cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="e4b5a-113">Ele chama o método [**CTransformFilter:: CompleteConnect**](ctransformfilter-completeconnect.md) do filtro, que retorna s \_ OK na classe base.</span><span class="sxs-lookup"><span data-stu-id="e4b5a-113">It calls the filter's [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="e4b5a-114">A classe derivada pode substituir o método **CTransformFilter:: CompleteConnect** para executar verificações adicionais.</span><span class="sxs-lookup"><span data-stu-id="e4b5a-114">The derived class can override the **CTransformFilter::CompleteConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4b5a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4b5a-115">Requirements</span></span>



| <span data-ttu-id="e4b5a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4b5a-116">Requirement</span></span> | <span data-ttu-id="e4b5a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e4b5a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b5a-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e4b5a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e4b5a-119"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4b5a-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e4b5a-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e4b5a-120">Library</span></span><br/> | <dl> <span data-ttu-id="e4b5a-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e4b5a-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





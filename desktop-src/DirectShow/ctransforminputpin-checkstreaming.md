---
description: O método CheckStreaming determina se o PIN pode aceitar amostras.
ms.assetid: fa063966-4c72-466e-933c-def6a6818621
title: Método CTransformInputPin. CheckStreaming (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e5c49a00054547193e3f492f0731f77af8331a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748190"
---
# <a name="ctransforminputpincheckstreaming-method"></a><span data-ttu-id="fb794-103">Método CTransformInputPin. CheckStreaming</span><span class="sxs-lookup"><span data-stu-id="fb794-103">CTransformInputPin.CheckStreaming method</span></span>

<span data-ttu-id="fb794-104">O `CheckStreaming` método determina se o PIN pode aceitar amostras.</span><span class="sxs-lookup"><span data-stu-id="fb794-104">The `CheckStreaming` method determines whether the pin can accept samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb794-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb794-105">Syntax</span></span>


```C++
HRESULT CheckStreaming();
```



## <a name="parameters"></a><span data-ttu-id="fb794-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb794-106">Parameters</span></span>

<span data-ttu-id="fb794-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fb794-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fb794-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fb794-108">Return value</span></span>

<span data-ttu-id="fb794-109">Retorna um dos valores **HRESULT** listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="fb794-109">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="fb794-110">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fb794-110">Return code</span></span>                                                                                           | <span data-ttu-id="fb794-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb794-111">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="fb794-112"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fb794-112"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="fb794-113">Êxito.</span><span class="sxs-lookup"><span data-stu-id="fb794-113">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="fb794-114"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="fb794-114"><dt>**S\_FALSE**</dt></span></span> </dl>               | <span data-ttu-id="fb794-115">O PIN está sendo liberado no momento.</span><span class="sxs-lookup"><span data-stu-id="fb794-115">Pin is currently flushing.</span></span><br/>       |
| <dl> <span data-ttu-id="fb794-116"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="fb794-116"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="fb794-117">O pino de saída não está conectado.</span><span class="sxs-lookup"><span data-stu-id="fb794-117">The output pin is not connected.</span></span><br/> |
| <dl> <span data-ttu-id="fb794-118"><dt>**VFW \_ E \_ erro de tempo de execução \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fb794-118"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="fb794-119">Ocorreu um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="fb794-119">A run-time error occurred.</span></span><br/>       |
| <dl> <span data-ttu-id="fb794-120"><dt>**VFW \_ E \_ estado incorreto \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fb794-120"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="fb794-121">O PIN foi interrompido.</span><span class="sxs-lookup"><span data-stu-id="fb794-121">The pin is stopped.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="fb794-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb794-122">Remarks</span></span>

<span data-ttu-id="fb794-123">Esse método substitui o método [**CBaseInputPin:: CheckStreaming**](cbaseinputpin-checkstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="fb794-123">This method overrides the [**CBaseInputPin::CheckStreaming**](cbaseinputpin-checkstreaming.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb794-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb794-124">Requirements</span></span>



| <span data-ttu-id="fb794-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb794-125">Requirement</span></span> | <span data-ttu-id="fb794-126">Valor</span><span class="sxs-lookup"><span data-stu-id="fb794-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb794-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb794-127">Header</span></span><br/>  | <dl> <span data-ttu-id="fb794-128"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fb794-128"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fb794-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fb794-129">Library</span></span><br/> | <dl> <span data-ttu-id="fb794-130"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="fb794-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





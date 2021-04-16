---
description: 'O método ativo notifica o PIN de que o filtro está ativo agora. Esse método substitui o método CBasePin:: active. Se o PIN estiver conectado, esse método iniciará o thread de streaming.'
ms.assetid: ea32b602-2583-4de6-96ec-6ea875c49d14
title: Método CSourceStream. Active (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a161c82621f29b916e03fbc2e59ec762871940b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768796"
---
# <a name="csourcestreamactive-method"></a><span data-ttu-id="2b8a1-105">Método CSourceStream. active</span><span class="sxs-lookup"><span data-stu-id="2b8a1-105">CSourceStream.Active method</span></span>

<span data-ttu-id="2b8a1-106">O `Active` método notifica o PIN de que o filtro está ativo agora.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-106">The `Active` method notifies the pin that the filter is now active.</span></span> <span data-ttu-id="2b8a1-107">Esse método substitui o método [**CBasePin:: active**](cbasepin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="2b8a1-107">This method overrides the [**CBasePin::Active**](cbasepin-active.md) method.</span></span> <span data-ttu-id="2b8a1-108">Se o PIN estiver conectado, esse método iniciará o thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-108">If the pin is connected, this method starts the streaming thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b8a1-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b8a1-109">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="2b8a1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b8a1-110">Parameters</span></span>

<span data-ttu-id="2b8a1-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2b8a1-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2b8a1-112">Return value</span></span>

<span data-ttu-id="2b8a1-113">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2b8a1-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2b8a1-114">Os valores possíveis incluem os listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-114">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="2b8a1-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2b8a1-115">Return code</span></span>                                                                             | <span data-ttu-id="2b8a1-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b8a1-116">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="2b8a1-117"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="2b8a1-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="2b8a1-118">O PIN já está ativo.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-118">The pin is already active.</span></span><br/>  |
| <dl> <span data-ttu-id="2b8a1-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2b8a1-119"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="2b8a1-120">Êxito.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-120">Success.</span></span><br/>                    |
| <dl> <span data-ttu-id="2b8a1-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="2b8a1-121"><dt>**E\_FAIL**</dt></span></span> </dl>  | <span data-ttu-id="2b8a1-122">Não foi possível iniciar o thread.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-122">Could not start the thread.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2b8a1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b8a1-123">Requirements</span></span>



| <span data-ttu-id="2b8a1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b8a1-124">Requirement</span></span> | <span data-ttu-id="2b8a1-125">Valor</span><span class="sxs-lookup"><span data-stu-id="2b8a1-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b8a1-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2b8a1-126">Header</span></span><br/>  | <dl> <span data-ttu-id="2b8a1-127"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b8a1-127"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="2b8a1-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2b8a1-128">Library</span></span><br/> | <dl> <span data-ttu-id="2b8a1-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="2b8a1-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b8a1-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b8a1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b8a1-131">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="2b8a1-131">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 





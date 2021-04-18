---
description: O método UnblockOutputPin desbloqueia o PIN. Quando o PIN é desbloqueado, ele pode entregar amostras, alterar seu formato de saída e se conectar novamente.
ms.assetid: ea6e6312-8c7f-44db-ac7f-165dc45dec23
title: Método CDynamicOutputPin. UnblockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.UnblockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60bcde3ccad01e19f3802e2cd19f0f6b873380ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778625"
---
# <a name="cdynamicoutputpinunblockoutputpin-method"></a><span data-ttu-id="e39e4-104">Método CDynamicOutputPin. UnblockOutputPin</span><span class="sxs-lookup"><span data-stu-id="e39e4-104">CDynamicOutputPin.UnblockOutputPin method</span></span>

<span data-ttu-id="e39e4-105">O `UnblockOutputPin` método desbloqueia o PIN.</span><span class="sxs-lookup"><span data-stu-id="e39e4-105">The `UnblockOutputPin` method unblocks the pin.</span></span> <span data-ttu-id="e39e4-106">Quando o PIN é desbloqueado, ele pode entregar amostras, alterar seu formato de saída e se conectar novamente.</span><span class="sxs-lookup"><span data-stu-id="e39e4-106">When the pin is unblocked, it can deliver samples, change its output format, and reconnect itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="e39e4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e39e4-107">Syntax</span></span>


```C++
HRESULT UnblockOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="e39e4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e39e4-108">Parameters</span></span>

<span data-ttu-id="e39e4-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e39e4-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e39e4-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e39e4-110">Return value</span></span>

<span data-ttu-id="e39e4-111">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e39e4-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="e39e4-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e39e4-112">Return code</span></span>                                                                             | <span data-ttu-id="e39e4-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="e39e4-113">Description</span></span>                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="e39e4-114"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="e39e4-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="e39e4-115">O PIN já estava desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="e39e4-115">Pin was already unblocked.</span></span><br/> |
| <dl> <span data-ttu-id="e39e4-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e39e4-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="e39e4-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="e39e4-117">Success.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="e39e4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e39e4-118">Requirements</span></span>



| <span data-ttu-id="e39e4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e39e4-119">Requirement</span></span> | <span data-ttu-id="e39e4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e39e4-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e39e4-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e39e4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e39e4-122"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e39e4-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e39e4-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e39e4-123">Library</span></span><br/> | <dl> <span data-ttu-id="e39e4-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e39e4-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e39e4-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e39e4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e39e4-126">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="e39e4-126">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 





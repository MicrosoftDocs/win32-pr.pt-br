---
description: O método GetResult recupera a lista de argumentos resultantes, se houver.
ms.assetid: a2a8b17c-3dcf-4f59-89c3-f42070d2a8eb
title: Método CDeferredCommand. GetResult (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetResult
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e8c1638dc33be6457dd682f37e2ddd49e73a111a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811744"
---
# <a name="cdeferredcommandgetresult-method"></a><span data-ttu-id="377fe-103">Método CDeferredCommand. GetResult</span><span class="sxs-lookup"><span data-stu-id="377fe-103">CDeferredCommand.GetResult method</span></span>

<span data-ttu-id="377fe-104">O `GetResult` método recupera a lista de argumentos resultantes, se houver.</span><span class="sxs-lookup"><span data-stu-id="377fe-104">The `GetResult` method retrieves the resulting argument list, if one exists.</span></span>

## <a name="syntax"></a><span data-ttu-id="377fe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="377fe-105">Syntax</span></span>


```C++
VARIANT* GetResult();
```



## <a name="parameters"></a><span data-ttu-id="377fe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="377fe-106">Parameters</span></span>

<span data-ttu-id="377fe-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="377fe-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="377fe-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="377fe-108">Return value</span></span>

<span data-ttu-id="377fe-109">Retorna um ponteiro para uma **variante** que contém a lista de argumentos do método, se existir.</span><span class="sxs-lookup"><span data-stu-id="377fe-109">Returns a pointer to a **VARIANT** containing the method's argument list, if it exists.</span></span>

## <a name="requirements"></a><span data-ttu-id="377fe-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="377fe-110">Requirements</span></span>



| <span data-ttu-id="377fe-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="377fe-111">Requirement</span></span> | <span data-ttu-id="377fe-112">Valor</span><span class="sxs-lookup"><span data-stu-id="377fe-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="377fe-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="377fe-113">Header</span></span><br/>  | <dl> <span data-ttu-id="377fe-114"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="377fe-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="377fe-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="377fe-115">Library</span></span><br/> | <dl> <span data-ttu-id="377fe-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="377fe-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="377fe-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="377fe-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="377fe-118">**Classe CDeferredCommand**</span><span class="sxs-lookup"><span data-stu-id="377fe-118">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 





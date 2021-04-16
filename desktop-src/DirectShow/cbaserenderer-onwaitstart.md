---
description: O método OnWaitStart é chamado quando o filtro começa a aguardar o tempo de apresentação de um exemplo.
ms.assetid: 598cd676-3afe-4ec9-ae38-83971412e6a7
title: Método CBaseRenderer. OnWaitStart (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c2f88f11e370c6d1962ae6076f4c8f5eecc31407
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757432"
---
# <a name="cbaserendereronwaitstart-method"></a><span data-ttu-id="7d449-103">Método CBaseRenderer. OnWaitStart</span><span class="sxs-lookup"><span data-stu-id="7d449-103">CBaseRenderer.OnWaitStart method</span></span>

<span data-ttu-id="7d449-104">O `OnWaitStart` método é chamado quando o filtro começa a aguardar o tempo de apresentação de um exemplo.</span><span class="sxs-lookup"><span data-stu-id="7d449-104">The `OnWaitStart` method is called when the filter starts waiting for a sample's presentation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d449-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7d449-105">Syntax</span></span>


```C++
virtual void OnWaitStart();
```



## <a name="parameters"></a><span data-ttu-id="7d449-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7d449-106">Parameters</span></span>

<span data-ttu-id="7d449-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7d449-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7d449-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7d449-108">Return value</span></span>

<span data-ttu-id="7d449-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7d449-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d449-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d449-110">Remarks</span></span>

<span data-ttu-id="7d449-111">O método [**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md) chama esse método quando ele começa a aguardar o tempo de apresentação de um exemplo.</span><span class="sxs-lookup"><span data-stu-id="7d449-111">The [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md) method calls this method when it begins waiting for a sample's presentation time.</span></span> <span data-ttu-id="7d449-112">Esse método não faz nada na classe base, mas a classe derivada pode substituí-la.</span><span class="sxs-lookup"><span data-stu-id="7d449-112">This method does not do anything in the base class, but the derived class can override it.</span></span>

<span data-ttu-id="7d449-113">Se você estiver implementando o controle de qualidade, poderá substituir esse método junto com o método [**CBaseRenderer:: OnWaitEnd**](cbaserenderer-onwaitend.md) .</span><span class="sxs-lookup"><span data-stu-id="7d449-113">If you are implementing quality control, you might override this method along with the [**CBaseRenderer::OnWaitEnd**](cbaserenderer-onwaitend.md) method.</span></span> <span data-ttu-id="7d449-114">Você pode usar esses métodos para acompanhar o desempenho do filtro.</span><span class="sxs-lookup"><span data-stu-id="7d449-114">You can use these methods to track the filter's performance.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d449-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d449-115">Requirements</span></span>



| <span data-ttu-id="7d449-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d449-116">Requirement</span></span> | <span data-ttu-id="7d449-117">Valor</span><span class="sxs-lookup"><span data-stu-id="7d449-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d449-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7d449-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7d449-119"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7d449-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7d449-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7d449-120">Library</span></span><br/> | <dl> <span data-ttu-id="7d449-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7d449-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d449-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d449-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d449-123">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="7d449-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 





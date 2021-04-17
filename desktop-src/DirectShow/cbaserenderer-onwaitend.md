---
description: O método OnWaitEnd é chamado quando o filtro é concluído aguardando o tempo de apresentação de um exemplo.
ms.assetid: 47ff8f79-da69-4dcf-8cbb-02c1b56e382e
title: Método CBaseRenderer. OnWaitEnd (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5a290ad5d39fc83a4213d1c8a32119b4caa9858
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758861"
---
# <a name="cbaserendereronwaitend-method"></a><span data-ttu-id="6c75a-103">Método CBaseRenderer. OnWaitEnd</span><span class="sxs-lookup"><span data-stu-id="6c75a-103">CBaseRenderer.OnWaitEnd method</span></span>

<span data-ttu-id="6c75a-104">O `OnWaitEnd` método é chamado quando o filtro é concluído aguardando o tempo de apresentação de um exemplo.</span><span class="sxs-lookup"><span data-stu-id="6c75a-104">The `OnWaitEnd` method is called when the filter is done waiting for a sample's presentation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c75a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c75a-105">Syntax</span></span>


```C++
virtual void OnWaitEnd();
```



## <a name="parameters"></a><span data-ttu-id="6c75a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c75a-106">Parameters</span></span>

<span data-ttu-id="6c75a-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6c75a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6c75a-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6c75a-108">Return value</span></span>

<span data-ttu-id="6c75a-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6c75a-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c75a-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c75a-110">Remarks</span></span>

<span data-ttu-id="6c75a-111">O método [**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md) chama esse método quando ele termina de aguardar o tempo de apresentação de um exemplo.</span><span class="sxs-lookup"><span data-stu-id="6c75a-111">The [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md) method calls this method when it has finished waiting for a sample's presentation time.</span></span> <span data-ttu-id="6c75a-112">Esse método não faz nada na classe base, mas a classe derivada pode substituí-la.</span><span class="sxs-lookup"><span data-stu-id="6c75a-112">This method does not do anything in the base class, but the derived class can override it.</span></span>

<span data-ttu-id="6c75a-113">Se você estiver implementando o controle de qualidade, poderá substituir esse método junto com o método [**CBaseRenderer:: OnWaitStart**](cbaserenderer-onwaitstart.md) .</span><span class="sxs-lookup"><span data-stu-id="6c75a-113">If you are implementing quality control, you might override this method along with the [**CBaseRenderer::OnWaitStart**](cbaserenderer-onwaitstart.md) method.</span></span> <span data-ttu-id="6c75a-114">Você pode usar esses métodos para acompanhar o desempenho do filtro.</span><span class="sxs-lookup"><span data-stu-id="6c75a-114">You can use these methods to track the filter's performance.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c75a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c75a-115">Requirements</span></span>



| <span data-ttu-id="6c75a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c75a-116">Requirement</span></span> | <span data-ttu-id="6c75a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="6c75a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c75a-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6c75a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6c75a-119"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c75a-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6c75a-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6c75a-120">Library</span></span><br/> | <dl> <span data-ttu-id="6c75a-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6c75a-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c75a-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c75a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c75a-123">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="6c75a-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 





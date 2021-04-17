---
description: O método SetAbortSignal define um sinalizador que indica se deve parar a renderização e rejeitar mais exemplos.
ms.assetid: 2dbf3b4d-e285-4d17-a77c-01a16c09d148
title: Método CBaseRenderer. SetAbortSignal (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetAbortSignal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70527d5e43ccab4df7b2110a33df8d813bd16d28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754546"
---
# <a name="cbaserenderersetabortsignal-method"></a><span data-ttu-id="c679f-103">Método CBaseRenderer. SetAbortSignal</span><span class="sxs-lookup"><span data-stu-id="c679f-103">CBaseRenderer.SetAbortSignal method</span></span>

<span data-ttu-id="c679f-104">O `SetAbortSignal` método define um sinalizador que indica se deve parar a renderização e rejeitar exemplos adicionais.</span><span class="sxs-lookup"><span data-stu-id="c679f-104">The `SetAbortSignal` method sets a flag which indicates whether to stop rendering and reject further samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="c679f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c679f-105">Syntax</span></span>


```C++
void SetAbortSignal(
   BOOL bAbort
);
```



## <a name="parameters"></a><span data-ttu-id="c679f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c679f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c679f-107">*bAbort*</span><span class="sxs-lookup"><span data-stu-id="c679f-107">*bAbort*</span></span> 
</dt> <dd>

<span data-ttu-id="c679f-108">Valor booliano que indica se a renderização deve ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="c679f-108">Boolean value indicating whether to stop rendering.</span></span> <span data-ttu-id="c679f-109">Se **for true**, o filtro não renderizará mais nenhum exemplo.</span><span class="sxs-lookup"><span data-stu-id="c679f-109">If **TRUE**, the filter will not render any more samples.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c679f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c679f-110">Return value</span></span>

<span data-ttu-id="c679f-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c679f-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c679f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c679f-112">Remarks</span></span>

<span data-ttu-id="c679f-113">Esse método define o sinalizador [**CBaseRenderer:: m \_ bAbort**](cbaserenderer-m-babort.md) .</span><span class="sxs-lookup"><span data-stu-id="c679f-113">This method sets the [**CBaseRenderer::m\_bAbort**](cbaserenderer-m-babort.md) flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="c679f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c679f-114">Requirements</span></span>



| <span data-ttu-id="c679f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c679f-115">Requirement</span></span> | <span data-ttu-id="c679f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c679f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c679f-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c679f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c679f-118"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c679f-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c679f-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c679f-119">Library</span></span><br/> | <dl> <span data-ttu-id="c679f-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c679f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c679f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="c679f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c679f-122">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="c679f-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 





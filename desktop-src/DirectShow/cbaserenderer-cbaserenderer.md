---
description: Construtor de CBaseRenderer. CBaseRenderer-método de construtor.
ms.assetid: df5efbb3-6bce-4e30-b1b1-d69bf64fa87d
title: Construtor CBaseRenderer. CBaseRenderer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CBaseRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 68ebc6255456f0fcbb4bf732a91dce981d0f78ce
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119904"
---
# <a name="cbaserenderercbaserenderer-constructor"></a><span data-ttu-id="e4987-103">Construtor CBaseRenderer. CBaseRenderer</span><span class="sxs-lookup"><span data-stu-id="e4987-103">CBaseRenderer.CBaseRenderer constructor</span></span>

<span data-ttu-id="e4987-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="e4987-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4987-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4987-105">Syntax</span></span>


```C++
CBaseRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   UINT      TimerResolution = 1
);
```



## <a name="parameters"></a><span data-ttu-id="e4987-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4987-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4987-107">*RenderClass*</span><span class="sxs-lookup"><span data-stu-id="e4987-107">*RenderClass*</span></span> 
</dt> <dd>

<span data-ttu-id="e4987-108">Identificador de classe do renderizador.</span><span class="sxs-lookup"><span data-stu-id="e4987-108">Class identifier of the renderer.</span></span>

</dd> <dt>

<span data-ttu-id="e4987-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="e4987-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="e4987-110">Ponteiro para uma cadeia de caracteres que contém o nome do filtro, para fins de depuração.</span><span class="sxs-lookup"><span data-stu-id="e4987-110">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="e4987-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="e4987-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="e4987-112">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="e4987-112">Pointer to the owner of this object.</span></span> <span data-ttu-id="e4987-113">Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="e4987-113">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="e4987-114">Caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e4987-114">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e4987-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="e4987-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="e4987-116">Recebe um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e4987-116">Receives an **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="e4987-117">*TimerResolution*</span><span class="sxs-lookup"><span data-stu-id="e4987-117">*TimerResolution*</span></span> 
</dt> <dd>

<span data-ttu-id="e4987-118">Resolução do temporizador.</span><span class="sxs-lookup"><span data-stu-id="e4987-118">Timer resolution.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e4987-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4987-119">Requirements</span></span>



| <span data-ttu-id="e4987-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4987-120">Requirement</span></span> | <span data-ttu-id="e4987-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e4987-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4987-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e4987-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e4987-123"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4987-123"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e4987-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e4987-124">Library</span></span><br/> | <dl> <span data-ttu-id="e4987-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e4987-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4987-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e4987-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4987-127">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="e4987-127">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 





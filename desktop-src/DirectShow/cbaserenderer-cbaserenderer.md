---
description: Método de construtor.
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
ms.openlocfilehash: b41f8d7f9681a64f58413aea2fd8717320278f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749630"
---
# <a name="cbaserenderercbaserenderer-constructor"></a><span data-ttu-id="732c7-103">Construtor CBaseRenderer. CBaseRenderer</span><span class="sxs-lookup"><span data-stu-id="732c7-103">CBaseRenderer.CBaseRenderer constructor</span></span>

<span data-ttu-id="732c7-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="732c7-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="732c7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="732c7-105">Syntax</span></span>


```C++
CBaseRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   UINT      TimerResolution = 1
);
```



## <a name="parameters"></a><span data-ttu-id="732c7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="732c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="732c7-107">*RenderClass*</span><span class="sxs-lookup"><span data-stu-id="732c7-107">*RenderClass*</span></span> 
</dt> <dd>

<span data-ttu-id="732c7-108">Identificador de classe do renderizador.</span><span class="sxs-lookup"><span data-stu-id="732c7-108">Class identifier of the renderer.</span></span>

</dd> <dt>

<span data-ttu-id="732c7-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="732c7-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="732c7-110">Ponteiro para uma cadeia de caracteres que contém o nome do filtro, para fins de depuração.</span><span class="sxs-lookup"><span data-stu-id="732c7-110">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="732c7-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="732c7-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="732c7-112">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="732c7-112">Pointer to the owner of this object.</span></span> <span data-ttu-id="732c7-113">Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="732c7-113">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="732c7-114">Caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="732c7-114">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="732c7-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="732c7-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="732c7-116">Recebe um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="732c7-116">Receives an **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="732c7-117">*TimerResolution*</span><span class="sxs-lookup"><span data-stu-id="732c7-117">*TimerResolution*</span></span> 
</dt> <dd>

<span data-ttu-id="732c7-118">Resolução do temporizador.</span><span class="sxs-lookup"><span data-stu-id="732c7-118">Timer resolution.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="732c7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="732c7-119">Requirements</span></span>



| <span data-ttu-id="732c7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="732c7-120">Requirement</span></span> | <span data-ttu-id="732c7-121">Valor</span><span class="sxs-lookup"><span data-stu-id="732c7-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="732c7-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="732c7-122">Header</span></span><br/>  | <dl> <span data-ttu-id="732c7-123"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="732c7-123"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="732c7-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="732c7-124">Library</span></span><br/> | <dl> <span data-ttu-id="732c7-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="732c7-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="732c7-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="732c7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="732c7-127">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="732c7-127">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 





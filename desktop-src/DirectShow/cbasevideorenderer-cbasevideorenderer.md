---
description: Método de construtor.
ms.assetid: 9b69632b-7932-4a9b-bd68-69b06dd8a5ec
title: Construtor CBaseVideoRenderer. CBaseVideoRenderer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.CBaseVideoRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27ed49be63d9c2c05e12a2ac92ae33f64705460b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778512"
---
# <a name="cbasevideorenderercbasevideorenderer-constructor"></a><span data-ttu-id="537f5-103">Construtor CBaseVideoRenderer. CBaseVideoRenderer</span><span class="sxs-lookup"><span data-stu-id="537f5-103">CBaseVideoRenderer.CBaseVideoRenderer constructor</span></span>

<span data-ttu-id="537f5-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="537f5-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="537f5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="537f5-105">Syntax</span></span>


```C++
CBaseVideoRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="537f5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="537f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="537f5-107">*RenderClass*</span><span class="sxs-lookup"><span data-stu-id="537f5-107">*RenderClass*</span></span> 
</dt> <dd>

<span data-ttu-id="537f5-108">Identificador de classe para este renderizador.</span><span class="sxs-lookup"><span data-stu-id="537f5-108">Class identifier for this renderer.</span></span>

</dd> <dt>

<span data-ttu-id="537f5-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="537f5-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="537f5-110">Ponteiro para uma descrição usada para fins de depuração.</span><span class="sxs-lookup"><span data-stu-id="537f5-110">Pointer to a description used for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="537f5-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="537f5-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="537f5-112">Ponteiro para o objeto do proprietário agregado.</span><span class="sxs-lookup"><span data-stu-id="537f5-112">Pointer to the aggregated owner object.</span></span>

</dd> <dt>

<span data-ttu-id="537f5-113">*phr*</span><span class="sxs-lookup"><span data-stu-id="537f5-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="537f5-114">Ponteiro para um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="537f5-114">Pointer to an **HRESULT** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="537f5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="537f5-115">Requirements</span></span>



| <span data-ttu-id="537f5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="537f5-116">Requirement</span></span> | <span data-ttu-id="537f5-117">Valor</span><span class="sxs-lookup"><span data-stu-id="537f5-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="537f5-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="537f5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="537f5-119"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="537f5-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="537f5-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="537f5-120">Library</span></span><br/> | <dl> <span data-ttu-id="537f5-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="537f5-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="537f5-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="537f5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="537f5-123">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="537f5-123">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 





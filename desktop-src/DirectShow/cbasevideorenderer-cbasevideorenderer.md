---
description: Construtor de CBaseVideoRenderer. CBaseVideoRenderer-método de construtor.
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
ms.openlocfilehash: c0ae558238b94402150e5cb15373d202065e485e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095834"
---
# <a name="cbasevideorenderercbasevideorenderer-constructor"></a><span data-ttu-id="f2c0d-103">Construtor CBaseVideoRenderer. CBaseVideoRenderer</span><span class="sxs-lookup"><span data-stu-id="f2c0d-103">CBaseVideoRenderer.CBaseVideoRenderer constructor</span></span>

<span data-ttu-id="f2c0d-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="f2c0d-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2c0d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2c0d-105">Syntax</span></span>


```C++
CBaseVideoRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="f2c0d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2c0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2c0d-107">*RenderClass*</span><span class="sxs-lookup"><span data-stu-id="f2c0d-107">*RenderClass*</span></span> 
</dt> <dd>

<span data-ttu-id="f2c0d-108">Identificador de classe para este renderizador.</span><span class="sxs-lookup"><span data-stu-id="f2c0d-108">Class identifier for this renderer.</span></span>

</dd> <dt>

<span data-ttu-id="f2c0d-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="f2c0d-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="f2c0d-110">Ponteiro para uma descrição usada para fins de depuração.</span><span class="sxs-lookup"><span data-stu-id="f2c0d-110">Pointer to a description used for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="f2c0d-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="f2c0d-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="f2c0d-112">Ponteiro para o objeto do proprietário agregado.</span><span class="sxs-lookup"><span data-stu-id="f2c0d-112">Pointer to the aggregated owner object.</span></span>

</dd> <dt>

<span data-ttu-id="f2c0d-113">*phr*</span><span class="sxs-lookup"><span data-stu-id="f2c0d-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="f2c0d-114">Ponteiro para um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f2c0d-114">Pointer to an **HRESULT** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f2c0d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2c0d-115">Requirements</span></span>



| <span data-ttu-id="f2c0d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2c0d-116">Requirement</span></span> | <span data-ttu-id="f2c0d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f2c0d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c0d-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f2c0d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f2c0d-119"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2c0d-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f2c0d-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f2c0d-120">Library</span></span><br/> | <dl> <span data-ttu-id="f2c0d-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f2c0d-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2c0d-122">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f2c0d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2c0d-123">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="f2c0d-123">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 





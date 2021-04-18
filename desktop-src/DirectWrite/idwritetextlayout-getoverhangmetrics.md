---
title: Método IDWriteTextLayout GetOverhangMetrics
description: Retorna os sobretravamentos (em DIPs) do layout e todos os objetos contidos nele, incluindo os glifos de texto e objetos embutidos.
ms.assetid: 4b23f6c5-cacc-41e2-8934-6f95208b999a
keywords:
- Gravação direta do método GetOverhangMetrics
- Método GetOverhangMetrics Direct Write, interface IDWriteTextLayout
- IDWriteTextLayout interface de gravação direta, método GetOverhangMetrics
topic_type:
- apiref
api_name:
- IDWriteTextLayout.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d8a015998f0a673a310319f93d8f4892dd4b1c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766922"
---
# <a name="idwritetextlayoutgetoverhangmetrics-method"></a><span data-ttu-id="2bb50-106">Método IDWriteTextLayout:: GetOverhangMetrics</span><span class="sxs-lookup"><span data-stu-id="2bb50-106">IDWriteTextLayout::GetOverhangMetrics method</span></span>

<span data-ttu-id="2bb50-107">Retorna os sobretravamentos (em DIPs) do layout e todos os objetos contidos nele, incluindo os glifos de texto e objetos embutidos.</span><span class="sxs-lookup"><span data-stu-id="2bb50-107">Returns the overhangs (in DIPs) of the layout and all objects contained in it, including text glyphs and inline objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bb50-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2bb50-108">Syntax</span></span>


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="2bb50-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2bb50-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bb50-110">*sobretravamentos* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2bb50-110">*overhangs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2bb50-111">Tipo: **[ **DWRITE \_ de \_ métricas de folga**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="2bb50-111">Type: **[**DWRITE\_OVERHANG\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span></span>

<span data-ttu-id="2bb50-112">Sobrelançações de extensões visíveis (em DIPs) fora do layout.</span><span class="sxs-lookup"><span data-stu-id="2bb50-112">Overshoots of visible extents (in DIPs) outside the layout.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bb50-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2bb50-113">Return value</span></span>

<span data-ttu-id="2bb50-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2bb50-114">Type: **HRESULT**</span></span>

<span data-ttu-id="2bb50-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2bb50-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2bb50-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2bb50-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bb50-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2bb50-117">Remarks</span></span>

<span data-ttu-id="2bb50-118">Sublinhados e tachados não contribuem para a determinação da caixa preta, pois eles são, na verdade, desenhados pelo renderizador, que tem permissão para desenhá-los em qualquer variedade de estilos.</span><span class="sxs-lookup"><span data-stu-id="2bb50-118">Underlines and strikethroughs do not contribute to the black box determination, since these are actually drawn by the renderer, which is allowed to draw them in any variety of styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bb50-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bb50-119">Requirements</span></span>



| <span data-ttu-id="2bb50-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bb50-120">Requirement</span></span> | <span data-ttu-id="2bb50-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2bb50-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2bb50-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2bb50-122">Library</span></span><br/> | <dl> <span data-ttu-id="2bb50-123"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2bb50-123"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="2bb50-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2bb50-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="2bb50-125"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bb50-125"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bb50-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="2bb50-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bb50-127">**IDWriteTextLayout**</span><span class="sxs-lookup"><span data-stu-id="2bb50-127">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[<span data-ttu-id="2bb50-128">**IDWriteTextLayout**</span><span class="sxs-lookup"><span data-stu-id="2bb50-128">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 


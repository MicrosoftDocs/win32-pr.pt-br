---
title: Método IDWriteFontFace GetGdiCompatibleMetrics
description: Obtém as unidades de design e as métricas comuns para a face da fonte. Essas métricas são aplicáveis a todos os glifos em um fontface e são usadas por aplicativos para cálculos de layout.
ms.assetid: 9e132ec0-64cb-4681-b079-02a0047badd5
keywords:
- Gravação direta do método GetGdiCompatibleMetrics
- Método GetGdiCompatibleMetrics Direct Write, interface IDWriteFontFace
- IDWriteFontFace interface de gravação direta, método GetGdiCompatibleMetrics
topic_type:
- apiref
api_name:
- IDWriteFontFace.GetGdiCompatibleMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81b1c00c872352c984c87ee84f7eaed5baffafd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759425"
---
# <a name="idwritefontfacegetgdicompatiblemetrics-method"></a><span data-ttu-id="f1ad1-107">Método IDWriteFontFace:: GetGdiCompatibleMetrics</span><span class="sxs-lookup"><span data-stu-id="f1ad1-107">IDWriteFontFace::GetGdiCompatibleMetrics method</span></span>

<span data-ttu-id="f1ad1-108">Obtém as unidades de design e as métricas comuns para a face da fonte.</span><span class="sxs-lookup"><span data-stu-id="f1ad1-108">Obtains design units and common metrics for the font face.</span></span> <span data-ttu-id="f1ad1-109">Essas métricas são aplicáveis a todos os glifos em um fontface e são usadas por aplicativos para cálculos de layout.</span><span class="sxs-lookup"><span data-stu-id="f1ad1-109">These metrics are applicable to all the glyphs within a fontface and are used by applications for layout calculations.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1ad1-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1ad1-110">Syntax</span></span>


```C++
virtual HRESULT GetGdiCompatibleMetrics(
                       FLOAT               emSize,
                       FLOAT               pixelsPerDip,
  [in, optional] const DWRITE_MATRIX       *transform,
  [out]                DWRITE_FONT_METRICS *fontFaceMetrics
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="f1ad1-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1ad1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1ad1-112">*emSize*</span><span class="sxs-lookup"><span data-stu-id="f1ad1-112">*emSize*</span></span> 
</dt> <dd>

<span data-ttu-id="f1ad1-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f1ad1-113">Type: **FLOAT**</span></span>

<span data-ttu-id="f1ad1-114">O tamanho lógico da fonte em unidades DIP.</span><span class="sxs-lookup"><span data-stu-id="f1ad1-114">The logical size of the font in DIP units.</span></span>

</dd> <dt>

<span data-ttu-id="f1ad1-115">*pixelsPerDip*</span><span class="sxs-lookup"><span data-stu-id="f1ad1-115">*pixelsPerDip*</span></span> 
</dt> <dd>

<span data-ttu-id="f1ad1-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f1ad1-116">Type: **FLOAT**</span></span>

<span data-ttu-id="f1ad1-117">O número de pixels físicos por DIP.</span><span class="sxs-lookup"><span data-stu-id="f1ad1-117">The number of physical pixels per DIP.</span></span>

</dd> <dt>

<span data-ttu-id="f1ad1-118">*transformar* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f1ad1-118">*transform* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f1ad1-119">Tipo: **\* [**\_ matriz DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) const**</span><span class="sxs-lookup"><span data-stu-id="f1ad1-119">Type: **const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\***</span></span>

<span data-ttu-id="f1ad1-120">Uma transformação opcional aplicada aos glifos e às suas posições.</span><span class="sxs-lookup"><span data-stu-id="f1ad1-120">An optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="f1ad1-121">Essa transformação é aplicada após o dimensionamento especificado pelo tamanho da fonte e *pixelsPerDip*.</span><span class="sxs-lookup"><span data-stu-id="f1ad1-121">This transform is applied after the scaling specified by the font size and *pixelsPerDip*.</span></span>

</dd> <dt>

<span data-ttu-id="f1ad1-122">*fontFaceMetrics* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f1ad1-122">*fontFaceMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1ad1-123">Tipo: **[ **\_ \_ métricas de fonte DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="f1ad1-123">Type: **[**DWRITE\_FONT\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)\***</span></span>

<span data-ttu-id="f1ad1-124">Um ponteiro para uma estrutura S de [**\_ \_ métrica de fonte DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)para preencher.</span><span class="sxs-lookup"><span data-stu-id="f1ad1-124">A pointer to a [**DWRITE\_FONT\_METRIC**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)S structure to fill in.</span></span> <span data-ttu-id="f1ad1-125">As métricas retornadas por essa função estão em unidades de design de fonte.</span><span class="sxs-lookup"><span data-stu-id="f1ad1-125">The metrics returned by this function are in font design units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1ad1-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f1ad1-126">Return value</span></span>

<span data-ttu-id="f1ad1-127">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f1ad1-127">Type: **HRESULT**</span></span>

<span data-ttu-id="f1ad1-128">Código de erro HRESULT padrão.</span><span class="sxs-lookup"><span data-stu-id="f1ad1-128">Standard HRESULT error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1ad1-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1ad1-129">Requirements</span></span>



| <span data-ttu-id="f1ad1-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1ad1-130">Requirement</span></span> | <span data-ttu-id="f1ad1-131">Valor</span><span class="sxs-lookup"><span data-stu-id="f1ad1-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1ad1-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f1ad1-132">Library</span></span><br/> | <dl> <span data-ttu-id="f1ad1-133"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1ad1-133"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="f1ad1-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f1ad1-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="f1ad1-135"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1ad1-135"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1ad1-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1ad1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1ad1-137">**IDWriteFontFace**</span><span class="sxs-lookup"><span data-stu-id="f1ad1-137">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[<span data-ttu-id="f1ad1-138">**IDWriteFontFace**</span><span class="sxs-lookup"><span data-stu-id="f1ad1-138">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 


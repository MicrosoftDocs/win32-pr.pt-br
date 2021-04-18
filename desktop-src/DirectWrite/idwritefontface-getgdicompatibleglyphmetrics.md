---
title: Método IDWriteFontFace GetGdiCompatibleGlyphMetrics
description: Obtém métricas de glifo em unidades de design de fonte com os valores de retorno compatíveis com o que o GDI produziria.
ms.assetid: 7bda3916-6db3-4f56-b18c-288506c0b646
keywords:
- Gravação direta do método GetGdiCompatibleGlyphMetrics
- Método GetGdiCompatibleGlyphMetrics Direct Write, interface IDWriteFontFace
- IDWriteFontFace interface de gravação direta, método GetGdiCompatibleGlyphMetrics
topic_type:
- apiref
api_name:
- IDWriteFontFace.GetGdiCompatibleGlyphMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a949edbdad2f25d748e5af64ebe408c79c7372b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811890"
---
# <a name="idwritefontfacegetgdicompatibleglyphmetrics-method"></a><span data-ttu-id="15071-106">Método IDWriteFontFace:: GetGdiCompatibleGlyphMetrics</span><span class="sxs-lookup"><span data-stu-id="15071-106">IDWriteFontFace::GetGdiCompatibleGlyphMetrics method</span></span>

<span data-ttu-id="15071-107">Obtém métricas de glifo em unidades de design de fonte com os valores de retorno compatíveis com o que o GDI produziria.</span><span class="sxs-lookup"><span data-stu-id="15071-107">Obtains glyph metrics in font design units with the return values compatible with what GDI would produce.</span></span>

## <a name="syntax"></a><span data-ttu-id="15071-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15071-108">Syntax</span></span>


```C++
virtual HRESULT GetGdiCompatibleGlyphMetrics(
                       FLOAT                emSize,
                       FLOAT                pixelsPerDip,
  [in, optional] const DWRITE_MATRIX        *transform,
                       BOOL                 useGdiNatural,
  [in]           const UINT16               *glyphIndices,
                       UINT32               glyphCount,
  [out]                DWRITE_GLYPH_METRICS *glyphMetrics,
                       BOOL                 isSideways = FALSE
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="15071-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15071-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15071-110">*emSize*</span><span class="sxs-lookup"><span data-stu-id="15071-110">*emSize*</span></span> 
</dt> <dd>

<span data-ttu-id="15071-111">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="15071-111">Type: **FLOAT**</span></span>

<span data-ttu-id="15071-112">O tamanho ogical da fonte em unidades DIP.</span><span class="sxs-lookup"><span data-stu-id="15071-112">The ogical size of the font in DIP units.</span></span>

</dd> <dt>

<span data-ttu-id="15071-113">*pixelsPerDip*</span><span class="sxs-lookup"><span data-stu-id="15071-113">*pixelsPerDip*</span></span> 
</dt> <dd>

<span data-ttu-id="15071-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="15071-114">Type: **FLOAT**</span></span>

<span data-ttu-id="15071-115">O número de pixels físicos por DIP.</span><span class="sxs-lookup"><span data-stu-id="15071-115">The number of physical pixels per DIP.</span></span>

</dd> <dt>

<span data-ttu-id="15071-116">*transformar* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="15071-116">*transform* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="15071-117">Tipo: **\* [**\_ matriz DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) const**</span><span class="sxs-lookup"><span data-stu-id="15071-117">Type: **const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\***</span></span>

<span data-ttu-id="15071-118">Uma transformação opcional aplicada aos glifos e às suas posições.</span><span class="sxs-lookup"><span data-stu-id="15071-118">An optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="15071-119">Essa transformação é aplicada após o dimensionamento especificado pelo tamanho da fonte e *pixelsPerDip*.</span><span class="sxs-lookup"><span data-stu-id="15071-119">This transform is applied after the scaling specified by the font size and *pixelsPerDip*.</span></span>

</dd> <dt>

<span data-ttu-id="15071-120">*useGdiNatural*</span><span class="sxs-lookup"><span data-stu-id="15071-120">*useGdiNatural*</span></span> 
</dt> <dd>

<span data-ttu-id="15071-121">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="15071-121">Type: **BOOL**</span></span>

<span data-ttu-id="15071-122">Quando definido como **false**, as métricas são as mesmas que as métricas de texto com alias GDI.</span><span class="sxs-lookup"><span data-stu-id="15071-122">When set to **FALSE**, the metrics are the same as the metrics of GDI aliased text.</span></span> <span data-ttu-id="15071-123">Quando definido como **true**, as métricas são as mesmas que as métricas de texto medido por GDI usando uma fonte criada com a **\_ \_ qualidade natural de ClearType**.</span><span class="sxs-lookup"><span data-stu-id="15071-123">When set to **TRUE**, the metrics are the same as the metrics of text measured by GDI using a font created with **CLEARTYPE\_NATURAL\_QUALITY**.</span></span>

</dd> <dt>

<span data-ttu-id="15071-124">*glyphIndices* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="15071-124">*glyphIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15071-125">Tipo: **const UINT16 \***</span><span class="sxs-lookup"><span data-stu-id="15071-125">Type: **const UINT16\***</span></span>

<span data-ttu-id="15071-126">Uma matriz de índices de glifo para os quais computar as métricas.</span><span class="sxs-lookup"><span data-stu-id="15071-126">An array of glyph indices for which to compute the metrics.</span></span>

</dd> <dt>

<span data-ttu-id="15071-127">*glyphCount*</span><span class="sxs-lookup"><span data-stu-id="15071-127">*glyphCount*</span></span> 
</dt> <dd>

<span data-ttu-id="15071-128">Tipo: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="15071-128">Type: **UINT32**</span></span>

<span data-ttu-id="15071-129">O número de elementos na matriz *glyphIndices* .</span><span class="sxs-lookup"><span data-stu-id="15071-129">The number of elements in the *glyphIndices* array.</span></span>

</dd> <dt>

<span data-ttu-id="15071-130">*glyphMetrics* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="15071-130">*glyphMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15071-131">Tipo: **[ **\_ \_ métricas de glifo DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="15071-131">Type: **[**DWRITE\_GLYPH\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics)\***</span></span>

<span data-ttu-id="15071-132">Uma matriz de estruturas de [**\_ \_ métricas de glifo DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) preenchidas por essa função.</span><span class="sxs-lookup"><span data-stu-id="15071-132">An array of [**DWRITE\_GLYPH\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) structures filled by this function.</span></span> <span data-ttu-id="15071-133">As métricas estão em unidades de design de fontes.</span><span class="sxs-lookup"><span data-stu-id="15071-133">The metrics are in font design units.</span></span>

</dd> <dt>

<span data-ttu-id="15071-134">*islaterals*</span><span class="sxs-lookup"><span data-stu-id="15071-134">*isSideways*</span></span> 
</dt> <dd>

<span data-ttu-id="15071-135">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="15071-135">Type: **BOOL**</span></span>

<span data-ttu-id="15071-136">Um valor BOOL que indica se a fonte está sendo usada em uma execução lateral.</span><span class="sxs-lookup"><span data-stu-id="15071-136">A BOOL value that indicates whether the font is being used in a sideways run.</span></span> <span data-ttu-id="15071-137">Isso pode afetar as métricas de glifo se a fonte tiver uma simulação oblíqua porque a simulação de oblíquo lateral difere da simulação oblíqua não lateral.</span><span class="sxs-lookup"><span data-stu-id="15071-137">This can affect the glyph metrics if the font has oblique simulation because sideways oblique simulation differs from non-sideways oblique simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15071-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15071-138">Return value</span></span>

<span data-ttu-id="15071-139">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="15071-139">Type: **HRESULT**</span></span>

<span data-ttu-id="15071-140">Código de erro **HRESULT** padrão.</span><span class="sxs-lookup"><span data-stu-id="15071-140">Standard **HRESULT** error code.</span></span> <span data-ttu-id="15071-141">Se qualquer um dos índices de glifos de entrada estiver fora do intervalo de índice de glifo válido para o tipo de fonte atual, **E \_ INVALIDARG** será retornado.</span><span class="sxs-lookup"><span data-stu-id="15071-141">If any of the input glyph indices are outside of the valid glyph index range for the current font face, **E\_INVALIDARG** will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="15071-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15071-142">Requirements</span></span>



| <span data-ttu-id="15071-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="15071-143">Requirement</span></span> | <span data-ttu-id="15071-144">Valor</span><span class="sxs-lookup"><span data-stu-id="15071-144">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="15071-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="15071-145">Library</span></span><br/> | <dl> <span data-ttu-id="15071-146"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15071-146"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="15071-147">DLL</span><span class="sxs-lookup"><span data-stu-id="15071-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="15071-148"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15071-148"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15071-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="15071-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15071-150">**IDWriteFontFace**</span><span class="sxs-lookup"><span data-stu-id="15071-150">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[<span data-ttu-id="15071-151">**IDWriteFontFace**</span><span class="sxs-lookup"><span data-stu-id="15071-151">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 


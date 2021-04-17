---
title: Método IDWriteTextAnalyzer GetGdiCompatibleGlyphPlacements
description: Coloque a saída de glifos do método getglifos de acordo com a fonte e as regras de renderização do sistema de escrita.
ms.assetid: 49312b03-9ee9-44ef-b3eb-a35631a6e693
keywords:
- Gravação direta do método GetGdiCompatibleGlyphPlacements
- Método GetGdiCompatibleGlyphPlacements Direct Write, interface IDWriteTextAnalyzer
- IDWriteTextAnalyzer interface de gravação direta, método GetGdiCompatibleGlyphPlacements
topic_type:
- apiref
api_name:
- IDWriteTextAnalyzer.GetGdiCompatibleGlyphPlacements
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f548e5fd20ce8814dc59657ff7bb422387c959fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769358"
---
# <a name="idwritetextanalyzergetgdicompatibleglyphplacements-method"></a><span data-ttu-id="e3cc1-106">Método IDWriteTextAnalyzer:: GetGdiCompatibleGlyphPlacements</span><span class="sxs-lookup"><span data-stu-id="e3cc1-106">IDWriteTextAnalyzer::GetGdiCompatibleGlyphPlacements method</span></span>

<span data-ttu-id="e3cc1-107">Coloque a saída de glifos do método [**Getglifos**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs) de acordo com a fonte e as regras de renderização do sistema de escrita.</span><span class="sxs-lookup"><span data-stu-id="e3cc1-107">Place glyphs output from the [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs) method according to the font and the writing system's rendering rules.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3cc1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3cc1-108">Syntax</span></span>


```C++
virtual HRESULT GetGdiCompatibleGlyphPlacements(
  [in]           const WCHAR                           *textString,
  [in]           const UINT16                          *clusterMap,
  [in]                 DWRITE_SHAPING_TEXT_PROPERTIES  *textProps,
                       UINT32                          textLength,
  [in]           const UINT16                          *glyphIndices,
  [in]           const DWRITE_SHAPING_GLYPH_PROPERTIES *glyphProps,
                       UINT32                          glyphCount,
  [in]                 IDWriteFontFace                 *fontFace,
                       FLOAT                           fontEmSize,
                       FLOAT                           pixelsPerDip,
  [in, optional] const DWRITE_MATRIX                   *transform,
                       BOOL                            useGdiNatural,
                       BOOL                             isSideways,
                       BOOL                             isRightToLeft,
  [in]           const DWRITE_SCRIPT_ANALYSIS          * scriptAnalysis,
  [in, optional] const WCHAR                           * localeName,
  [in, optional] const DWRITE_TYPOGRAPHIC_FEATURES     ** features,
  [in, optional] const UINT32                          * featureRangeLengths,
                       UINT32                           featureRanges,
  [out]                FLOAT                           * glyphAdvances,
  [out]                DWRITE_GLYPH_OFFSET             * glyphOffsets
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="e3cc1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3cc1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3cc1-110">*textString* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e3cc1-110">*textString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3cc1-111">Tipo: **const WCHAR \***</span><span class="sxs-lookup"><span data-stu-id="e3cc1-111">Type: **const WCHAR\***</span></span>

<span data-ttu-id="e3cc1-112">Uma matriz de caracteres que contém a cadeia original da qual os glifos vieram.</span><span class="sxs-lookup"><span data-stu-id="e3cc1-112">An array of characters containing the original string from which the glyphs came.</span></span>

</dd> <dt>

<span data-ttu-id="e3cc1-113">*clusterMap* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e3cc1-113">*clusterMap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3cc1-114">Tipo: **const UINT16 \***</span><span class="sxs-lookup"><span data-stu-id="e3cc1-114">Type: **const UINT16\***</span></span>

<span data-ttu-id="e3cc1-115">Um ponteiro para o mapeamento de intervalos de caracteres para intervalos de glifos.</span><span class="sxs-lookup"><span data-stu-id="e3cc1-115">A pointer to the mapping from character ranges to glyph ranges.</span></span> <span data-ttu-id="e3cc1-116">Isso é retornado por [**Getglifos**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span><span class="sxs-lookup"><span data-stu-id="e3cc1-116">This is returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="e3cc1-117">*Textprops* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e3cc1-117">*textProps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3cc1-118">Tipo: **[ **DWRITE \_ SHAPING \_ Text \_ Properties**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties)\***</span><span class="sxs-lookup"><span data-stu-id="e3cc1-118">Type: **[**DWRITE\_SHAPING\_TEXT\_PROPERTIES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties)\***</span></span>

<span data-ttu-id="e3cc1-119">Um ponteiro para uma matriz de estruturas que contém propriedades de formatação para cada caractere.</span><span class="sxs-lookup"><span data-stu-id="e3cc1-119">A pointer to an array of structures that contains shaping properties for each character.</span></span> <span data-ttu-id="e3cc1-120">Essa estrutura é retornada por [**Getglifos**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span><span class="sxs-lookup"><span data-stu-id="e3cc1-120">This structure is returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="e3cc1-121">*textLength*</span><span class="sxs-lookup"><span data-stu-id="e3cc1-121">*textLength*</span></span> 
</dt> <dd>

<span data-ttu-id="e3cc1-122">Tipo: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="e3cc1-122">Type: **UINT32**</span></span>

<span data-ttu-id="e3cc1-123">O comprimento do texto de *textString*.</span><span class="sxs-lookup"><span data-stu-id="e3cc1-123">The text length of *textString*.</span></span>

</dd> <dt>

<span data-ttu-id="e3cc1-124">*glyphIndices* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e3cc1-124">*glyphIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3cc1-125">Tipo: **const UINT16 \***</span><span class="sxs-lookup"><span data-stu-id="e3cc1-125">Type: **const UINT16\***</span></span>

<span data-ttu-id="e3cc1-126">Uma matriz de índices de glifos retornada por [**Getglifos**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span><span class="sxs-lookup"><span data-stu-id="e3cc1-126">An array of glyph indices returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="e3cc1-127">*glyphProps* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e3cc1-127">*glyphProps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3cc1-128">Tipo: **\* [**Propriedades de \_ \_ glifo \_ const DWRITE SHAPING**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties)**</span><span class="sxs-lookup"><span data-stu-id="e3cc1-128">Type: **const [**DWRITE\_SHAPING\_GLYPH\_PROPERTIES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties)\***</span></span>

<span data-ttu-id="e3cc1-129">Um ponteiro para uma matriz de estruturas que contém propriedades de formatação para cada glifo retornado por [**Getglifos**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span><span class="sxs-lookup"><span data-stu-id="e3cc1-129">A pointer to an array of structures that contain shaping properties for each glyph returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="e3cc1-130">*glyphCount*</span><span class="sxs-lookup"><span data-stu-id="e3cc1-130">*glyphCount*</span></span> 
</dt> <dd>

<span data-ttu-id="e3cc1-131">Tipo: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="e3cc1-131">Type: **UINT32**</span></span>

<span data-ttu-id="e3cc1-132">O número de glifos retornados de [**Getglifos**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span><span class="sxs-lookup"><span data-stu-id="e3cc1-132">The number of glyphs returned from [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="e3cc1-133">*fontface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e3cc1-133">*fontFace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3cc1-134">Tipo: **[ **IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)\***</span><span class="sxs-lookup"><span data-stu-id="e3cc1-134">Type: **[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)\***</span></span>

<span data-ttu-id="e3cc1-135">Um ponteiro para a face de fonte que é a origem dos glifos de saída.</span><span class="sxs-lookup"><span data-stu-id="e3cc1-135">A pointer to the font face that is the source for the output glyphs.</span></span>

</dd> <dt>

<span data-ttu-id="e3cc1-136">*fontEmSize*</span><span class="sxs-lookup"><span data-stu-id="e3cc1-136">*fontEmSize*</span></span> 
</dt> <dd>

<span data-ttu-id="e3cc1-137">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e3cc1-137">Type: **FLOAT**</span></span>

<span data-ttu-id="e3cc1-138">O tamanho da fonte lógica em DIPs.</span><span class="sxs-lookup"><span data-stu-id="e3cc1-138">The logical font size in DIPs.</span></span>

</dd> <dt>

<span data-ttu-id="e3cc1-139">*pixelsPerDip*</span><span class="sxs-lookup"><span data-stu-id="e3cc1-139">*pixelsPerDip*</span></span> 
</dt> <dd>

<span data-ttu-id="e3cc1-140">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e3cc1-140">Type: **FLOAT**</span></span>

<span data-ttu-id="e3cc1-141">O número de pixels físicos por DIP.</span><span class="sxs-lookup"><span data-stu-id="e3cc1-141">The number of physical pixels per DIP.</span></span>

</dd> <dt>

<span data-ttu-id="e3cc1-142">*transformar* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e3cc1-142">*transform* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e3cc1-143">Tipo: **\* [**\_ matriz DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) const**</span><span class="sxs-lookup"><span data-stu-id="e3cc1-143">Type: **const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\***</span></span>

<span data-ttu-id="e3cc1-144">Uma transformação opcional aplicada aos glifos e às suas posições.</span><span class="sxs-lookup"><span data-stu-id="e3cc1-144">An optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="e3cc1-145">Essa transformação é aplicada após o dimensionamento especificado pelo tamanho da fonte e *pixelsPerDip*.</span><span class="sxs-lookup"><span data-stu-id="e3cc1-145">This transform is applied after the scaling specified by the font size and *pixelsPerDip*.</span></span>

</dd> <dt>

<span data-ttu-id="e3cc1-146">*useGdiNatural*</span><span class="sxs-lookup"><span data-stu-id="e3cc1-146">*useGdiNatural*</span></span> 
</dt> <dd>

<span data-ttu-id="e3cc1-147">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="e3cc1-147">Type: **BOOL**</span></span>

<span data-ttu-id="e3cc1-148">Quando definido como **false**, as métricas são as mesmas que as métricas de texto com alias GDI.</span><span class="sxs-lookup"><span data-stu-id="e3cc1-148">When set to **FALSE**, the metrics are the same as the metrics of GDI aliased text.</span></span> <span data-ttu-id="e3cc1-149">Quando definido como **true**, as métricas são as mesmas que as métricas de texto medido por GDI usando uma fonte criada com a **\_ \_ qualidade natural de ClearType**.</span><span class="sxs-lookup"><span data-stu-id="e3cc1-149">When set to **TRUE**, the metrics are the same as the metrics of text measured by GDI using a font created with **CLEARTYPE\_NATURAL\_QUALITY**.</span></span>

</dd> <dt>

 <span data-ttu-id="e3cc1-150">*islaterals*</span><span class="sxs-lookup"><span data-stu-id="e3cc1-150">*isSideways*</span></span> 
</dt> <dd>

<span data-ttu-id="e3cc1-151">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="e3cc1-151">Type: **BOOL**</span></span>

<span data-ttu-id="e3cc1-152">Um sinalizador booliano definido como **true** se o texto se destina a ser desenhado verticalmente.</span><span class="sxs-lookup"><span data-stu-id="e3cc1-152">A Boolean flag set to **TRUE** if the text is intended to be drawn vertically.</span></span>

</dd> <dt>

 <span data-ttu-id="e3cc1-153">*IsRightToLeft*</span><span class="sxs-lookup"><span data-stu-id="e3cc1-153">*isRightToLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="e3cc1-154">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="e3cc1-154">Type: **BOOL**</span></span>

<span data-ttu-id="e3cc1-155">Um sinalizador booliano definido como **true** para texto da direita para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="e3cc1-155">A Boolean flag set to **TRUE** for right-to-left text.</span></span>

</dd> <dt>

 <span data-ttu-id="e3cc1-156">*scriptAnalysis* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e3cc1-156">*scriptAnalysis* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3cc1-157">Type: **const [**DWRITE \_ script \_ Analysis**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) \***</span><span class="sxs-lookup"><span data-stu-id="e3cc1-157">Type: **const [**DWRITE\_SCRIPT\_ANALYSIS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis)\***</span></span>

<span data-ttu-id="e3cc1-158">Um ponteiro para um resultado de análise de script de uma chamada [**AnalyzeScript**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript) .</span><span class="sxs-lookup"><span data-stu-id="e3cc1-158">A pointer to a Script analysis result from an [**AnalyzeScript**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript) call.</span></span>

</dd> <dt>

 <span data-ttu-id="e3cc1-159">*localename* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e3cc1-159">*localeName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e3cc1-160">Tipo: **const WCHAR \***</span><span class="sxs-lookup"><span data-stu-id="e3cc1-160">Type: **const WCHAR\***</span></span>

<span data-ttu-id="e3cc1-161">Uma matriz de caracteres que contém a localidade a ser usada ao selecionar glifos.</span><span class="sxs-lookup"><span data-stu-id="e3cc1-161">An array of characters containing the locale to use when selecting glyphs.</span></span> <span data-ttu-id="e3cc1-162">Por exemplo, o mesmo caractere pode ser mapeado para glifos diferentes para ja-JP versus zh-CHS.</span><span class="sxs-lookup"><span data-stu-id="e3cc1-162">For example, the same character may map to different glyphs for ja-jp versus zh-chs.</span></span> <span data-ttu-id="e3cc1-163">Se isso for **nulo**, o mapeamento padrão baseado no script será usado.</span><span class="sxs-lookup"><span data-stu-id="e3cc1-163">If this is **NULL**, then the default mapping based on the script is used.</span></span>

</dd> <dt>

 <span data-ttu-id="e3cc1-164">*recursos* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e3cc1-164">*features* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e3cc1-165">Tipo: **\* \* const [**DWRITE \_ de \_ recursos tipográficos**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features)**</span><span class="sxs-lookup"><span data-stu-id="e3cc1-165">Type: **const [**DWRITE\_TYPOGRAPHIC\_FEATURES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features)\*\***</span></span>

<span data-ttu-id="e3cc1-166">Uma matriz de ponteiros para os conjuntos de recursos tipográficos a serem usados em cada intervalo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e3cc1-166">An array of pointers to the sets of typographic features to use in each feature range.</span></span>

</dd> <dt>

 <span data-ttu-id="e3cc1-167">*featureRangeLengths* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e3cc1-167">*featureRangeLengths* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e3cc1-168">Tipo: **const UINT32 \***</span><span class="sxs-lookup"><span data-stu-id="e3cc1-168">Type: **const UINT32\***</span></span>

<span data-ttu-id="e3cc1-169">O comprimento de cada intervalo de recursos, em caracteres.</span><span class="sxs-lookup"><span data-stu-id="e3cc1-169">The length of each feature range, in characters.</span></span> <span data-ttu-id="e3cc1-170">A soma de todos os comprimentos deve ser igual a *TextLength*.</span><span class="sxs-lookup"><span data-stu-id="e3cc1-170">The sum of all lengths should be equal to *textLength*.</span></span>

</dd> <dt>

 <span data-ttu-id="e3cc1-171">*featureRanges*</span><span class="sxs-lookup"><span data-stu-id="e3cc1-171">*featureRanges*</span></span> 
</dt> <dd>

<span data-ttu-id="e3cc1-172">Tipo: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="e3cc1-172">Type: **UINT32**</span></span>

<span data-ttu-id="e3cc1-173">O número de intervalos de recursos.</span><span class="sxs-lookup"><span data-stu-id="e3cc1-173">The number of feature ranges.</span></span>

</dd> <dt>

 <span data-ttu-id="e3cc1-174">*glyphAdvances* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e3cc1-174">*glyphAdvances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3cc1-175">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="e3cc1-175">Type: **FLOAT\***</span></span>

<span data-ttu-id="e3cc1-176">Quando esse método retorna, contém a largura antecipada de cada glifo.</span><span class="sxs-lookup"><span data-stu-id="e3cc1-176">When this method returns, contains the advance width of each glyph.</span></span>

</dd> <dt>

 <span data-ttu-id="e3cc1-177">*glyphOffsets* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e3cc1-177">*glyphOffsets* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3cc1-178">Tipo: **[ **\_ \_ deslocamento de glifo DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset)\***</span><span class="sxs-lookup"><span data-stu-id="e3cc1-178">Type: **[**DWRITE\_GLYPH\_OFFSET**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset)\***</span></span>

<span data-ttu-id="e3cc1-179">Quando esse método retorna, contém o deslocamento da origem de cada glifo.</span><span class="sxs-lookup"><span data-stu-id="e3cc1-179">When this method returns, contains the offset of the origin of each glyph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3cc1-180">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e3cc1-180">Return value</span></span>

<span data-ttu-id="e3cc1-181">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e3cc1-181">Type: **HRESULT**</span></span>

<span data-ttu-id="e3cc1-182">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e3cc1-182">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e3cc1-183">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e3cc1-183">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3cc1-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3cc1-184">Requirements</span></span>



| <span data-ttu-id="e3cc1-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3cc1-185">Requirement</span></span> | <span data-ttu-id="e3cc1-186">Valor</span><span class="sxs-lookup"><span data-stu-id="e3cc1-186">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3cc1-187">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e3cc1-187">Library</span></span><br/> | <dl> <span data-ttu-id="e3cc1-188"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3cc1-188"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="e3cc1-189">DLL</span><span class="sxs-lookup"><span data-stu-id="e3cc1-189">DLL</span></span><br/>     | <dl> <span data-ttu-id="e3cc1-190"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3cc1-190"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3cc1-191">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3cc1-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3cc1-192">**IDWriteTextAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="e3cc1-192">**IDWriteTextAnalyzer**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer)
</dt> </dl>

 


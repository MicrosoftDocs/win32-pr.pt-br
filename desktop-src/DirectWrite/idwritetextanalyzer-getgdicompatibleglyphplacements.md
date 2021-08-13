---
title: Método GetGdiCompatibleGlyphPlacements de IDWriteTextAnalyzer
description: Coloque a saída de glifos do método GetGlyphs de acordo com a fonte e as regras de renderização do sistema de escrita.
ms.assetid: 49312b03-9ee9-44ef-b3eb-a35631a6e693
keywords:
- Método GetGdiCompatibleGlyphPlacements Direct Write
- Método GetGdiCompatibleGlyphPlacements Direct Write , interface IDWriteTextAnalyzer
- Método IDWriteTextAnalyzer interface Direct Write , GetGdiCompatibleGlyphPlacements
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
ms.openlocfilehash: 8d05fcf5595500f34730a720e4a4c2e80d68922929d8055b754a26a1dc92f63c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650006"
---
# <a name="idwritetextanalyzergetgdicompatibleglyphplacements-method"></a>Método IDWriteTextAnalyzer::GetGdiCompatibleGlyphPlacements

Coloque a saída de glifos do [**método GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs) de acordo com a fonte e as regras de renderização do sistema de escrita.

## <a name="syntax"></a>Sintaxe


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



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*textString* \[ Em\]
</dt> <dd>

Tipo: **const \* WCHAR**

Uma matriz de caracteres que contém a cadeia de caracteres original da qual os glifos foram lançados.

</dd> <dt>

*clusterMap* \[ Em\]
</dt> <dd>

Tipo: **const UINT16 \***

Um ponteiro para o mapeamento de intervalos de caracteres para intervalos de glifo. Isso é retornado por [**GetGlyphs.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)

</dd> <dt>

*textProps* \[ Em\]
</dt> <dd>

Tipo: **[ **DWRITE \_ FORMATANDO PROPRIEDADES \_ DE \_ TEXTO**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties)\***

Um ponteiro para uma matriz de estruturas que contém propriedades de formatação para cada caractere. Essa estrutura é retornada [**por GetGlyphs.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)

</dd> <dt>

*Textlength* 
</dt> <dd>

Tipo: **UINT32**

O comprimento do texto *de textString.*

</dd> <dt>

*glifoIndices* \[ Em\]
</dt> <dd>

Tipo: **const UINT16 \***

Uma matriz de índices de glifo retornados por [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*glifoProps* \[ Em\]
</dt> <dd>

Tipo: **const [**DWRITE \_ SHAPING \_ \_ LYPH PROPERTIES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties) \***

Um ponteiro para uma matriz de estruturas que contêm propriedades de formatação para cada glifo retornado por [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*glifoCount* 
</dt> <dd>

Tipo: **UINT32**

O número de glifos retornados de [**GetGlyphs.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)

</dd> <dt>

*fontFace* \[ Em\]
</dt> <dd>

Tipo: **[ **IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)\***

Um ponteiro para o rosto da fonte que é a origem dos glifos de saída.

</dd> <dt>

*fontEmSize* 
</dt> <dd>

Tipo: **FLOAT**

O tamanho da fonte lógica em DIPs.

</dd> <dt>

*pixelsPerDip* 
</dt> <dd>

Tipo: **FLOAT**

O número de pixels físicos por DIP.

</dd> <dt>

*transformação* \[ in, opcional\]
</dt> <dd>

Tipo: **const [**DWRITE \_ MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***

Uma transformação opcional aplicada aos glifos e suas posições. Essa transformação é aplicada após o dimensionamento especificado pelo tamanho da fonte e *pixelsPerDip.*

</dd> <dt>

*useGdiNatural* 
</dt> <dd>

Tipo: **BOOL**

Quando definidas como **FALSE,** as métricas são as mesmas que as métricas do texto com alias GDI. Quando definidas como **TRUE,** as métricas são as mesmas que as métricas de texto medida pela GDI usando uma fonte criada com **CLEARTYPE \_ NATURAL \_ QUALITY**.

</dd> <dt>

 *isSideways* 
</dt> <dd>

Tipo: **BOOL**

Um sinalizador booliana definido como **TRUE** se o texto for destinado a ser desenhado verticalmente.

</dd> <dt>

 *Isrighttoleft* 
</dt> <dd>

Tipo: **BOOL**

Um sinalizador booliana definido como **TRUE** para texto da direita para a esquerda.

</dd> <dt>

 *scriptAnalysis* \[ Em\]
</dt> <dd>

Tipo: **const [**DWRITE \_ SCRIPT \_ ANALYSIS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) \***

Um ponteiro para um resultado de análise de script de [**uma chamada AnalyzeScript.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript)

</dd> <dt>

 *localeName* \[ in, opcional\]
</dt> <dd>

Tipo: **const \* WCHAR**

Uma matriz de caracteres que contém a localidade a ser usada ao selecionar glifos. Por exemplo, o mesmo caractere pode mapear para glifos diferentes para ja-jp versus zh-chs. Se for **NULL,** o mapeamento padrão com base no script será usado.

</dd> <dt>

 *recursos* \[ in, opcional\]
</dt> <dd>

Tipo: **const [**DWRITE \_ TYPOGRAPHIC \_ FEATURES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features) \* \***

Uma matriz de ponteiros para os conjuntos de recursos tipográficos a usar em cada intervalo de recursos.

</dd> <dt>

 *featureRangeLengths* \[ in, opcional\]
</dt> <dd>

Tipo: **const UINT32 \***

O comprimento de cada intervalo de recursos, em caracteres. A soma de todos os comprimentos deve ser igual a *textLength.*

</dd> <dt>

 *featureRanges* 
</dt> <dd>

Tipo: **UINT32**

O número de intervalos de recursos.

</dd> <dt>

 *glifoAdvances* \[ out\]
</dt> <dd>

Tipo: **\* FLOAT**

Quando este método retorna, contém a largura antecipada de cada glifo.

</dd> <dt>

 *glifoOffsets* \[ out\]
</dt> <dd>

Tipo: **[ **DESLOCAMENTO DE \_ GLIFO \_ DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset)\***

Quando este método retorna, contém o deslocamento da origem de cada glifo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteTextAnalyzer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer)
</dt> </dl>

 


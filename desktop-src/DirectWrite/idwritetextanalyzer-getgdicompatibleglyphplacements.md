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
# <a name="idwritetextanalyzergetgdicompatibleglyphplacements-method"></a>Método IDWriteTextAnalyzer:: GetGdiCompatibleGlyphPlacements

Coloque a saída de glifos do método [**Getglifos**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs) de acordo com a fonte e as regras de renderização do sistema de escrita.

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

*textString* \[ no\]
</dt> <dd>

Tipo: **const WCHAR \***

Uma matriz de caracteres que contém a cadeia original da qual os glifos vieram.

</dd> <dt>

*clusterMap* \[ no\]
</dt> <dd>

Tipo: **const UINT16 \***

Um ponteiro para o mapeamento de intervalos de caracteres para intervalos de glifos. Isso é retornado por [**Getglifos**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*Textprops* \[ no\]
</dt> <dd>

Tipo: **[ **DWRITE \_ SHAPING \_ Text \_ Properties**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties)\***

Um ponteiro para uma matriz de estruturas que contém propriedades de formatação para cada caractere. Essa estrutura é retornada por [**Getglifos**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*textLength* 
</dt> <dd>

Tipo: **UINT32**

O comprimento do texto de *textString*.

</dd> <dt>

*glyphIndices* \[ no\]
</dt> <dd>

Tipo: **const UINT16 \***

Uma matriz de índices de glifos retornada por [**Getglifos**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*glyphProps* \[ no\]
</dt> <dd>

Tipo: **\* [**Propriedades de \_ \_ glifo \_ const DWRITE SHAPING**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties)**

Um ponteiro para uma matriz de estruturas que contém propriedades de formatação para cada glifo retornado por [**Getglifos**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*glyphCount* 
</dt> <dd>

Tipo: **UINT32**

O número de glifos retornados de [**Getglifos**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*fontface* \[ no\]
</dt> <dd>

Tipo: **[ **IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)\***

Um ponteiro para a face de fonte que é a origem dos glifos de saída.

</dd> <dt>

*fontEmSize* 
</dt> <dd>

Tipo: **float**

O tamanho da fonte lógica em DIPs.

</dd> <dt>

*pixelsPerDip* 
</dt> <dd>

Tipo: **float**

O número de pixels físicos por DIP.

</dd> <dt>

*transformar* \[ em, opcional\]
</dt> <dd>

Tipo: **\* [**\_ matriz DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) const**

Uma transformação opcional aplicada aos glifos e às suas posições. Essa transformação é aplicada após o dimensionamento especificado pelo tamanho da fonte e *pixelsPerDip*.

</dd> <dt>

*useGdiNatural* 
</dt> <dd>

Tipo: **bool**

Quando definido como **false**, as métricas são as mesmas que as métricas de texto com alias GDI. Quando definido como **true**, as métricas são as mesmas que as métricas de texto medido por GDI usando uma fonte criada com a **\_ \_ qualidade natural de ClearType**.

</dd> <dt>

 *islaterals* 
</dt> <dd>

Tipo: **bool**

Um sinalizador booliano definido como **true** se o texto se destina a ser desenhado verticalmente.

</dd> <dt>

 *IsRightToLeft* 
</dt> <dd>

Tipo: **bool**

Um sinalizador booliano definido como **true** para texto da direita para a esquerda.

</dd> <dt>

 *scriptAnalysis* \[ no\]
</dt> <dd>

Type: **const [**DWRITE \_ script \_ Analysis**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) \***

Um ponteiro para um resultado de análise de script de uma chamada [**AnalyzeScript**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript) .

</dd> <dt>

 *localename* \[ em, opcional\]
</dt> <dd>

Tipo: **const WCHAR \***

Uma matriz de caracteres que contém a localidade a ser usada ao selecionar glifos. Por exemplo, o mesmo caractere pode ser mapeado para glifos diferentes para ja-JP versus zh-CHS. Se isso for **nulo**, o mapeamento padrão baseado no script será usado.

</dd> <dt>

 *recursos* \[ do em, opcional\]
</dt> <dd>

Tipo: **\* \* const [**DWRITE \_ de \_ recursos tipográficos**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features)**

Uma matriz de ponteiros para os conjuntos de recursos tipográficos a serem usados em cada intervalo de recursos.

</dd> <dt>

 *featureRangeLengths* \[ em, opcional\]
</dt> <dd>

Tipo: **const UINT32 \***

O comprimento de cada intervalo de recursos, em caracteres. A soma de todos os comprimentos deve ser igual a *TextLength*.

</dd> <dt>

 *featureRanges* 
</dt> <dd>

Tipo: **UINT32**

O número de intervalos de recursos.

</dd> <dt>

 *glyphAdvances* \[ fora\]
</dt> <dd>

Tipo: **float \***

Quando esse método retorna, contém a largura antecipada de cada glifo.

</dd> <dt>

 *glyphOffsets* \[ fora\]
</dt> <dd>

Tipo: **[ **\_ \_ deslocamento de glifo DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset)\***

Quando esse método retorna, contém o deslocamento da origem de cada glifo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteTextAnalyzer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer)
</dt> </dl>

 


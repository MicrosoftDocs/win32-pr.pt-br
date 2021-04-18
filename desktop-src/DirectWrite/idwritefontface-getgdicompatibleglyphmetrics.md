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
# <a name="idwritefontfacegetgdicompatibleglyphmetrics-method"></a>Método IDWriteFontFace:: GetGdiCompatibleGlyphMetrics

Obtém métricas de glifo em unidades de design de fonte com os valores de retorno compatíveis com o que o GDI produziria.

## <a name="syntax"></a>Sintaxe


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



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*emSize* 
</dt> <dd>

Tipo: **float**

O tamanho ogical da fonte em unidades DIP.

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

*glyphIndices* \[ no\]
</dt> <dd>

Tipo: **const UINT16 \***

Uma matriz de índices de glifo para os quais computar as métricas.

</dd> <dt>

*glyphCount* 
</dt> <dd>

Tipo: **UINT32**

O número de elementos na matriz *glyphIndices* .

</dd> <dt>

*glyphMetrics* \[ fora\]
</dt> <dd>

Tipo: **[ **\_ \_ métricas de glifo DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics)\***

Uma matriz de estruturas de [**\_ \_ métricas de glifo DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) preenchidas por essa função. As métricas estão em unidades de design de fontes.

</dd> <dt>

*islaterals* 
</dt> <dd>

Tipo: **bool**

Um valor BOOL que indica se a fonte está sendo usada em uma execução lateral. Isso pode afetar as métricas de glifo se a fonte tiver uma simulação oblíqua porque a simulação de oblíquo lateral difere da simulação oblíqua não lateral.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Código de erro **HRESULT** padrão. Se qualquer um dos índices de glifos de entrada estiver fora do intervalo de índice de glifo válido para o tipo de fonte atual, **E \_ INVALIDARG** será retornado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 


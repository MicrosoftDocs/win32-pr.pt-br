---
title: Método GetGdiCompatibleGlyphMetrics de IDWriteFontFace
description: Obtém métricas de glifo em unidades de design de fonte com os valores de retorno compatíveis com o que a GDI produziria.
ms.assetid: 7bda3916-6db3-4f56-b18c-288506c0b646
keywords:
- Método GetGdiCompatibleGlyphMetrics Direct Write
- Método GetGdiCompatibleGlyphMetrics Direct Write , interface IDWriteFontFace
- Método Direct Write , GetGdiCompatibleGlyphMetrics da interface IDWriteFontFace
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
ms.openlocfilehash: bd36fc09ff8161ba8fb72d3b55b9351b0a7d2a6bd3f3f11a71c15a8d9422f6c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816496"
---
# <a name="idwritefontfacegetgdicompatibleglyphmetrics-method"></a>Método IDWriteFontFace::GetGdiCompatibleGlyphMetrics

Obtém métricas de glifo em unidades de design de fonte com os valores de retorno compatíveis com o que a GDI produziria.

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

Tipo: **FLOAT**

O tamanho ogical da fonte em unidades DIP.

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

*glifoIndices* \[ Em\]
</dt> <dd>

Tipo: **const UINT16 \***

Uma matriz de índices de glifo para os quais calcular as métricas.

</dd> <dt>

*glifoCount* 
</dt> <dd>

Tipo: **UINT32**

O número de elementos na *matriz glifoIndices.*

</dd> <dt>

*glifoMetrics* \[ out\]
</dt> <dd>

Tipo: **[ **DWRITE \_ \_ MÉTRICAS DE GLIFO**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics)\***

Uma matriz de [**estruturas \_ \_ MÉTRICAS de GLIFO DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) preenchidas por essa função. As métricas estão em unidades de design de fonte.

</dd> <dt>

*isSideways* 
</dt> <dd>

Tipo: **BOOL**

Um valor BOOL que indica se a fonte está sendo usada em uma operação lateral. Isso poderá afetar as métricas de glifo se a fonte tiver simulação oblíqua porque a simulação oblíqua lateral é diferente da simulação oblíqua não lateral.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Código **de erro HRESULT** padrão. Se qualquer um dos índices de glifo de entrada estiver fora do intervalo de índice de glifo válido para a face da fonte atual, **E \_ INVALIDARG** será retornado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 


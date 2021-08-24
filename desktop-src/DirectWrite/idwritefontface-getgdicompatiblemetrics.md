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
ms.openlocfilehash: fce5080edc44501290672bf0db0ebac69ef4856ec0b7163821cf60ac63d384ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290706"
---
# <a name="idwritefontfacegetgdicompatiblemetrics-method"></a>Método IDWriteFontFace:: GetGdiCompatibleMetrics

Obtém as unidades de design e as métricas comuns para a face da fonte. Essas métricas são aplicáveis a todos os glifos em um fontface e são usadas por aplicativos para cálculos de layout.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT GetGdiCompatibleMetrics(
                       FLOAT               emSize,
                       FLOAT               pixelsPerDip,
  [in, optional] const DWRITE_MATRIX       *transform,
  [out]                DWRITE_FONT_METRICS *fontFaceMetrics
) = 0;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*emSize* 
</dt> <dd>

Tipo: **float**

O tamanho lógico da fonte em unidades DIP.

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

*fontFaceMetrics* \[ fora\]
</dt> <dd>

Tipo: **[ **\_ \_ métricas de fonte DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)\***

Um ponteiro para uma estrutura S de [**\_ \_ métrica de fonte DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)para preencher. As métricas retornadas por essa função estão em unidades de design de fonte.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Código de erro HRESULT padrão.

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

 


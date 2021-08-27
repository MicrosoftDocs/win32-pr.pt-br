---
title: Método CreateGlyphRunAnalysis de IDWriteFactory2
description: Cria um objeto de análise de run de glifo, que encapsula as informações usadas para renderizar uma run de glifo.
ms.assetid: 13cecfbf-8bb6-88a2-c8b2-3243f6cb92fd
keywords:
- Gravação direta do método CreateGlyphRunAnalysis
- Método CreateGlyphRunAnalysis Direct Write, interface IDWriteFactory2
- IDWriteFactory2 interface Direct Write , método CreateGlyphRunAnalysis
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateGlyphRunAnalysis
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4ea5c2dc4cb97b1b9ba02e786efc20a4e2a44990b9a1d28b862aeab254079a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048826"
---
# <a name="idwritefactory2createglyphrunanalysis-method"></a>Método IDWriteFactory2::CreateGlyphRunAnalysis

Cria um objeto de análise de run de glifo, que encapsula as informações usadas para renderizar uma run de glifo.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT CreateGlyphRunAnalysis(
  [in]           const DWRITE_GLYPH_RUN           *glyphRun,
  [in, optional] const DWRITE_MATRIX              *transform,
                       DWRITE_RENDERING_MODE      renderingMode,
                       DWRITE_MEASURING_MODE      measuringMode,
                       DWRITE_GRID_FIT_MODE       gridFitMode,
                       DWRITE_TEXT_ANTIALIAS_MODE antialiasMode,
                       FLOAT                      baselineOriginX,
                       FLOAT                      baselineOriginY,
  [out]                IDWriteGlyphRunAnalysis    **glyphRunAnalysis
) = 0;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*glifoRun* \[ Em\]
</dt> <dd>

Tipo: **const [**DWRITE \_ GLYPH \_ RUN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) \***

Estrutura que especifica as propriedades da run de glifo.

</dd> <dt>

*transformação* \[ in, opcional\]
</dt> <dd>

Tipo: **const [**DWRITE \_ MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***

Transformação opcional aplicada aos glifos e suas posições. Essa transformação é aplicada após o dimensionamento especificado pelo emSize e pixelsPerDip.

</dd> <dt>

*renderingMode* 
</dt> <dd>

Tipo: **MODO DE RENDERIZAÇÃO DWRITE \_ \_**

Especifica o modo de renderização, que deve ser um dos modos de renderização de raster (ou seja, não padrão e não contorno).

</dd> <dt>

*measuringMode* 
</dt> <dd>

Tipo: **[ **DWRITE \_ MEASURING \_ MODE**](/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode)**

Especifica o método para medir glifos.

</dd> <dt>

*gridFitMode* 
</dt> <dd>

Tipo: **[ **MODO DE AJUSTE DE \_ GRADE \_ \_ DWRITE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**

Como ajustar contornos de glifo em grade. Isso deve ser não padrão.

</dd> <dt>

*antialiasMode* 
</dt> <dd>

Tipo: **[ **MODO \_ \_ ANTIALIAS DE TEXTO \_ DWRITE**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode)**

Especifica o modo antialias.

</dd> <dt>

*baselineOriginX* 
</dt> <dd>

Tipo: **FLOAT**

Posição horizontal da origem da linha de base, em DIPs.

</dd> <dt>

*baselineOriginy* 
</dt> <dd>

Tipo: **FLOAT**

Posição vertical da origem da linha de base, em DIPs.

</dd> <dt>

*glifoRunAnalysis* \[ out\]
</dt> <dd>

Tipo: **[ **IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis)\*\***

Recebe um ponteiro para o objeto recém-criado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Aplicativos UWP de aplicativos da área \[ de trabalho \| R2\]<br/>                          |
| Telefone mínimo com suporte<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 e Windows runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 


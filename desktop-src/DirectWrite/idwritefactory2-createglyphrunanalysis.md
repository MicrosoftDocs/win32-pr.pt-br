---
title: Método IDWriteFactory2 CreateGlyphRunAnalysis
description: Cria um objeto de análise de execução de glifos, que encapsula informações usadas para renderizar uma execução de glifo.
ms.assetid: 13cecfbf-8bb6-88a2-c8b2-3243f6cb92fd
keywords:
- Gravação direta do método CreateGlyphRunAnalysis
- Método CreateGlyphRunAnalysis Direct Write, interface IDWriteFactory2
- IDWriteFactory2 interface de gravação direta, método CreateGlyphRunAnalysis
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
ms.openlocfilehash: abd944c45fc271a22a0942556038073ebcc591cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369750"
---
# <a name="idwritefactory2createglyphrunanalysis-method"></a>Método IDWriteFactory2:: CreateGlyphRunAnalysis

Cria um objeto de análise de execução de glifos, que encapsula informações usadas para renderizar uma execução de glifo.

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

*GlyphRun* \[ no\]
</dt> <dd>

Tipo: **const [**DWRITE \_ glifo \_ Run**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) \** _

Estrutura que especifica as propriedades da execução de glifo.

</dd> <dt>

_transform * \[ in, opcional\]
</dt> <dd>

Tipo: **const [**DWRITE \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \** _

Transformação opcional aplicada aos glifos e às suas posições. Essa transformação é aplicada após o dimensionamento especificado por emSize e pixelsPerDip.

</dd> <dt>

_renderingMode * 
</dt> <dd>

Tipo: **\_ \_ modo de renderização DWRITE**

Especifica o modo de renderização, que deve ser um dos modos de renderização de rasterização (ou seja, não padrão e não contorno).

</dd> <dt>

*medirmode* 
</dt> <dd>

Tipo: **[ **\_ \_ modo de medição DWRITE**](/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode)**

Especifica o método para medir glifos.

</dd> <dt>

*gridFitMode* 
</dt> <dd>

Tipo: **[ **\_ modo de \_ ajuste \_ da grade DWRITE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**

Como ajustar os contornos de glifo de grade. Isso deve ser não padrão.

</dd> <dt>

*antialiasmode* 
</dt> <dd>

Tipo: **[ **\_ modo de \_ AntiAlias \_ de texto DWRITE**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode)**

Especifica o modo AntiAlias.

</dd> <dt>

*baselineOriginX* 
</dt> <dd>

Tipo: **float**

Posição horizontal da origem da linha de base, em DIPs.

</dd> <dt>

*baselineOriginY* 
</dt> <dd>

Tipo: **float**

Posição vertical da origem da linha de base, em DIPs.

</dd> <dt>

*glyphRunAnalysis* \[ fora\]
</dt> <dd>

Tipo: **[ **IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis)\*\***

Recebe um ponteiro para o objeto recém-criado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]<br/>                          |
| Número mínimo de telefone com suporte<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 


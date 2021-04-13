---
title: Método IDWriteFactory2 CreateCustomRenderingParams
description: Cria um objeto de parâmetros de renderização com as propriedades especificadas.
ms.assetid: 947d50fd-888c-2f0b-25c2-b19b0e6fad58
keywords:
- Gravação direta do método CreateCustomRenderingParams
- Método CreateCustomRenderingParams Direct Write, interface IDWriteFactory2
- IDWriteFactory2 interface de gravação direta, método CreateCustomRenderingParams
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateCustomRenderingParams
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bd69cde6858061b69b8143dcdd0560342e65f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369751"
---
# <a name="idwritefactory2createcustomrenderingparams-method"></a>Método IDWriteFactory2:: CreateCustomRenderingParams

Cria um objeto de parâmetros de renderização com as propriedades especificadas.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT CreateCustomRenderingParams(
        FLOAT                   gamma,
        FLOAT                   enhancedContrast,
        FLOAT                   grayscaleEnhancedContrast,
        FLOAT                   clearTypeLevel,
        DWRITE_PIXEL_GEOMETRY   pixelGeometry,
        DWRITE_RENDERING_MODE   renderingMode,
        DWRITE_GRID_FIT_MODE    gridFitMode,
  [out] IDWriteRenderingParams2 **renderingParams
) = 0;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*gama* 
</dt> <dd>

Tipo: **float**

O valor de gama usado para correção gama, que deve ser maior que zero e não pode exceder 256.

</dd> <dt>

*enhancedContrast* 
</dt> <dd>

Tipo: **float**

O valor de aumento de contraste, zero ou maior.

</dd> <dt>

*grayscaleEnhancedContrast* 
</dt> <dd>

Tipo: **float**

O valor de aumento de contraste, zero ou maior.

</dd> <dt>

*clearTypeLevel* 
</dt> <dd>

Tipo: **float**

O grau de nível de ClearType, de 0,0 f (sem ClearType) a 1,0 f (ClearType completo).

</dd> <dt>

*pixelGeometry* 
</dt> <dd>

Tipo: **[ **DWRITE \_ pixel \_ Geometry**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry)**

A geometria de um pixel de dispositivo.

</dd> <dt>

*RenderingMode* 
</dt> <dd>

Tipo: **[ **\_ \_ modo de renderização DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)**

Método de renderização de glifos. Na maioria dos casos, deve ser o \_ modo de RENDERIZAÇÃO DWRITE \_ \_ padrão para usar automaticamente um modo apropriado.

</dd> <dt>

*gridFitMode* 
</dt> <dd>

Tipo: **[ **\_ modo de \_ ajuste \_ da grade DWRITE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**

Como colocar em grade os contornos de glifos. Na maioria dos casos, deve ser DWRITE \_ grade \_ se ajustar \_ ao padrão para escolher automaticamente um modo apropriado.

</dd> <dt>

*renderingParams* \[ fora\]
</dt> <dd>

Tipo: **[ **IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2)\*\***

Mantém o objeto de parâmetros de renderização recém-criado ou nulo em caso de falha.

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

 


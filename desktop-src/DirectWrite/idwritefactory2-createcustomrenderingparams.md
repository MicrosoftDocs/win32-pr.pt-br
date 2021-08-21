---
title: Método CreateCustomRenderingParams de IDWriteFactory2
description: Cria um objeto de parâmetros de renderização com as propriedades especificadas.
ms.assetid: 947d50fd-888c-2f0b-25c2-b19b0e6fad58
keywords:
- Gravação direta do método CreateCustomRenderingParams
- CreateCustomRenderingParams método Direct Write , interface IDWriteFactory2
- Método IDWriteFactory2 interface Direct Write , CreateCustomRenderingParams
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
ms.openlocfilehash: 2e85057c28e1ad969fe72711c86aab9657126c760ea3041a08bc5101877686a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071681"
---
# <a name="idwritefactory2createcustomrenderingparams-method"></a>Método IDWriteFactory2::CreateCustomRenderingParams

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

*Gama* 
</dt> <dd>

Tipo: **FLOAT**

O valor gama usado para correção gama, que deve ser maior que zero e não pode exceder 256.

</dd> <dt>

*enhancedContrast* 
</dt> <dd>

Tipo: **FLOAT**

A quantidade de aprimoramento de contraste, zero ou maior.

</dd> <dt>

*grayscaleEnhancedContrast* 
</dt> <dd>

Tipo: **FLOAT**

A quantidade de aprimoramento de contraste, zero ou maior.

</dd> <dt>

*clearTypeLevel* 
</dt> <dd>

Tipo: **FLOAT**

O grau de nível ClearType, de 0,0f (sem ClearType) a 1,0f (ClearType completo).

</dd> <dt>

*pixelGeometry* 
</dt> <dd>

Tipo: **[ **GEOMETRIA DE \_ PIXEL \_ DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry)**

A geometria de um pixel de dispositivo.

</dd> <dt>

*renderingMode* 
</dt> <dd>

Tipo: **[ **MODO DE \_ RENDERIZAÇÃO \_ DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)**

Método de renderização de glifos. Na maioria dos casos, esse deve ser o MODO DE RENDERIZAÇÃO DE DWRITE \_ \_ PADRÃO para usar \_ automaticamente um modo apropriado.

</dd> <dt>

*gridFitMode* 
</dt> <dd>

Tipo: **[ **MODO DE AJUSTE DE \_ GRADE \_ \_ DWRITE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**

Como ajustar a grade de contornos de glifo. Na maioria dos casos, deve ser DWRITE \_ GRID FIT DEFAULT para escolher \_ \_ automaticamente um modo apropriado.

</dd> <dt>

*renderingParams* \[ out\]
</dt> <dd>

Tipo: **[ **IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2)\*\***

Contém o objeto de parâmetros de renderização recém-criado ou NULL em caso de falha.

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

 


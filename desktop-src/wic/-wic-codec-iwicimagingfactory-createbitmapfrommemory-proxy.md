---
description: Função proxy para o método CreateBitmapFromMemory.
ms.assetid: 5aa455d5-23e3-4738-b028-b84da0fb0c50
title: IWICImagingFactory_CreateBitmapFromMemory_Proxy função
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e7f5567f2ead2b68440e448a9a03f36fdedceb5d31ecfc579f7df956988dfc01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118033909"
---
# <a name="iwicimagingfactory_createbitmapfrommemory_proxy-function"></a>Função proxy IWICImagingFactory \_ CreateBitmapFromMemory \_

Função proxy para o [**método CreateBitmapFromMemory.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfrommemory)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICImagingFactory_CreateBitmapFromMemory_Proxy(
  _In_  IWICImagingFactory    *pFactory,
  _In_  UINT                  uiWidth,
  _In_  UINT                  uiHeight,
  _In_  REFWICPixelFormatGUID pixelFormat,
  _In_  UINT                  cbStride,
  _In_  UINT                  cbBufferSize,
  _In_  BYTE                  *pbBuffer,
  _Out_ IWICBitmap            **ppIBitmap
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFactory* \[ Em\]
</dt> <dd>

Tipo: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

</dd> <dt>

*uiWidth* \[ Em\]
</dt> <dd>

Tipo: **UINT**

A largura do novo bitmap.

</dd> <dt>

*uiHeight* \[ Em\]
</dt> <dd>

Tipo: **UINT**

A altura do novo bitmap.

</dd> <dt>

*pixelFormat* \[ Em\]
</dt> <dd>

Tipo: **REFWICPixelFormatGUID**

O formato de pixel do novo bitmap.

</dd> <dt>

*cbStride* \[ Em\]
</dt> <dd>

Tipo: **UINT**

O [*passo*](/windows) dos dados de pixel determinados.

</dd> <dt>

*cbBufferSize* \[ Em\]
</dt> <dd>

Tipo: **UINT**

O tamanho de *pbBuffer.*

</dd> <dt>

*pbBuffer* \[ Em\]
</dt> <dd>

Tipo: **BYTE \***

O buffer usado para criar o bitmap.

</dd> <dt>

*ppIBitmap* \[ out\]
</dt> <dd>

Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***

Um ponteiro que recebe um ponteiro para o novo bitmap.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se essa função for bem-sucedida, ela retornará **S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP com SP2, Windows aplicativos da área de trabalho do Vista \[\]<br/>                                                                                              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 


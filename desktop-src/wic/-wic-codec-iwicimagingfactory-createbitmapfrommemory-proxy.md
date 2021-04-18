---
description: Função de proxy para o método CreateBitmapFromMemory.
ms.assetid: 5aa455d5-23e3-4738-b028-b84da0fb0c50
title: Função IWICImagingFactory_CreateBitmapFromMemory_Proxy
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
ms.openlocfilehash: 79893952bb6dcdbab6c4a1cea4f57355831d31c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753378"
---
# <a name="iwicimagingfactory_createbitmapfrommemory_proxy-function"></a>\_Função de \_ proxy IWICImagingFactory CreateBitmapFromMemory

Função de proxy para o método [**CreateBitmapFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfrommemory) .

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

*pFactory* \[ no\]
</dt> <dd>

Tipo: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_uiWidth * \[ in\]
</dt> <dd>

Tipo: **uint**

A largura do novo bitmap.

</dd> <dt>

*uiHeight* \[ no\]
</dt> <dd>

Tipo: **uint**

A altura do novo bitmap.

</dd> <dt>

*PixelFormat* \[ no\]
</dt> <dd>

Tipo: **REFWICPixelFormatGUID**

O formato de pixel do novo bitmap.

</dd> <dt>

*cbStride* \[ no\]
</dt> <dd>

Tipo: **uint**

O [*Stride*](/windows) dos dados de pixel fornecidos.

</dd> <dt>

*cbBufferSize* \[ no\]
</dt> <dd>

Tipo: **uint**

O tamanho de *pbBuffer*.

</dd> <dt>

*pbBuffer* \[ no\]
</dt> <dd>

Tipo: **byte \** _

O buffer usado para criar o bitmap.

</dd> <dt>

_ppIBitmap * \[ out\]
</dt> <dd>

Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***

Um ponteiro que recebe um ponteiro para o novo bitmap.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 


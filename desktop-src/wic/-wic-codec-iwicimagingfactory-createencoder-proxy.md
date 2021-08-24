---
description: Função proxy para o método CreateEncoder.
ms.assetid: e3ffad7f-eb0e-481d-81ee-caf18e14ba59
title: IWICImagingFactory_CreateEncoder_Proxy função
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateEncoder_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 20e1a95253c0943383842b9667d93e4fc98c48ab2abf229bae7c0b3ad3f3fe63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812276"
---
# <a name="iwicimagingfactory_createencoder_proxy-function"></a>Função proxy IWICImagingFactory \_ CreateEncoder \_

Função proxy para o [**método CreateEncoder.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createencoder)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICImagingFactory_CreateEncoder_Proxy(
  _In_           IWICImagingFactory *pFactory,
  _In_           REFGUID            guidContainerFormat,
  _In_opt_ const GUID               *pguidVendor,
  _Out_          IWICBitmapEncoder  **ppIEncoder
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFactory* \[ Em\]
</dt> <dd>

Tipo: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

</dd> <dt>

*guidContainerFormat* \[ Em\]
</dt> <dd>

Tipo: **REFGUID**

O GUID para o formato de contêiner desejado.

</dd> <dt>

*pguidVendor* \[ in, opcional\]
</dt> <dd>

Tipo: **const \* GUID**

O GUID do fornecedor para o codificador.

</dd> <dt>

*ppIEncoder* \[ out\]
</dt> <dd>

Tipo: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\*\***

Um ponteiro que recebe um ponteiro para um [**novo IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).

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



 

 





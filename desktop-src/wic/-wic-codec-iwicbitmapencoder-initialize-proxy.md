---
description: IWICBitmapEncoder_Initialize_Proxy função - função proxy para o método Initialize.
ms.assetid: 0db79eb4-dcb2-491a-9bea-a0dec418f80f
title: IWICBitmapEncoder_Initialize_Proxy função
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ef1c51ac9693d81eb7c6cdc88c28431eacda3137a5ad73e4fa20c08c16d32509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812646"
---
# <a name="iwicbitmapencoder_initialize_proxy-function"></a>Função Inicializar Proxy IWICBitmapEncoder \_ \_

Função proxy para o [**método Initialize.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICBitmapEncoder_Initialize_Proxy(
  _In_ IWICBitmapEncoder           *THIS_PTR,
  _In_ IStream                     *pIStream,
  _In_ WICBitmapEncoderCacheOption cacheOption
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ESTE \_ PTR* \[ em\]
</dt> <dd>

Tipo: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***

Ponteiro para este [**objeto IWICBitmapEncoder.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)

</dd> <dt>

*pIStream* \[ Em\]
</dt> <dd>

Tipo: **[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\***

O fluxo de saída.

</dd> <dt>

*cacheOption* \[ Em\]
</dt> <dd>

Tipo: **[ **WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption)**

O [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) usado na inicialização.

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



 


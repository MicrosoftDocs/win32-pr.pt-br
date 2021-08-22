---
description: Função de proxy para o método CreateBitmapScaler.
ms.assetid: 27fcb17e-bdcd-44cc-9fe6-f93816589b50
title: Função IWICImagingFactory_CreateBitmapScaler_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapScaler_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: dd72049f72d14be41f1ef3601d04fd692af54271011849486ae72c1cce0e0e42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711422"
---
# <a name="iwicimagingfactory_createbitmapscaler_proxy-function"></a>\_Função de \_ proxy IWICImagingFactory CreateBitmapScaler

Função de proxy para o método [**CreateBitmapScaler**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapscaler) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICImagingFactory_CreateBitmapScaler_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICBitmapScaler   **ppIBitmapScaler
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFactory* \[ no\]
</dt> <dd>

Tipo: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

</dd> <dt>

*ppIBitmapScaler* \[ fora\]
</dt> <dd>

Tipo: **[ **IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\*\***

Um ponteiro que recebe um ponteiro para um novo [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP com SP2, somente aplicativos do Windows Vista \[ desktop\]<br/>                                                                                              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 





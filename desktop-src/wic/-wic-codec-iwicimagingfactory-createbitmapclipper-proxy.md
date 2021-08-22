---
description: Função de proxy para o método CreateBitmapClipper.
ms.assetid: 163a8d7b-f22b-4ab5-9dba-00b0cdaab440
title: Função IWICImagingFactory_CreateBitmapClipper_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapClipper_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 67104e9d2864ba5f94f0ac0594dfbbe9d7bc11d128b01430b0aacaf12acd8df1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088381"
---
# <a name="iwicimagingfactory_createbitmapclipper_proxy-function"></a>\_Função de \_ proxy IWICImagingFactory CreateBitmapClipper

Função de proxy para o método [**CreateBitmapClipper**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapclipper) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICImagingFactory_CreateBitmapClipper_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICBitmapClipper  **ppIBitmapClipper
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFactory* \[ no\]
</dt> <dd>

Tipo: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

</dd> <dt>

*ppIBitmapClipper* \[ fora\]
</dt> <dd>

Tipo: **[ **IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\*\***

Um ponteiro que recebe um ponteiro para um novo [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper).

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



 

 





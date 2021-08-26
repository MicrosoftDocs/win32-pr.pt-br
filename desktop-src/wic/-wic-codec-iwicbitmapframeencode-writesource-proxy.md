---
description: Função de proxy para o método WriteState.
ms.assetid: d95ad80f-7a26-45a7-8103-2673989143b7
title: Função IWICBitmapFrameEncode_WriteSource_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_WriteSource_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8fe4970fbc6d50e19b917fe9364169089199ac17fa5ca15be1e65ec0c0e71b8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090036"
---
# <a name="iwicbitmapframeencode_writesource_proxy-function"></a>Função de proxy de \_ gravação de IWICBitmapFrameEncode \_

Função de proxy para o método [**WriteState**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICBitmapFrameEncode_WriteSource_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IWICBitmapSource      *pIBitmapSource,
  _In_ WICRect               *prc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Isso \_ PTR* \[\]
</dt> <dd>

Tipo: **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***

Ponteiro para este objeto [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .

</dd> <dt>

*pIBitmapSource* \[ no\]
</dt> <dd>

Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

A origem do bitmap a ser codificada.

</dd> <dt>

*prc* \[ no\]
</dt> <dd>

Tipo: **[ **WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\***

O tamanho do retângulo da origem do bitmap.

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



 

 





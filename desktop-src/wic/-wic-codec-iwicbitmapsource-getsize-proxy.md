---
description: Função de proxy para o método GetSize.
ms.assetid: a9b7d01c-78d9-47b8-a373-a7c49f7bccfd
title: Função IWICBitmapSource_GetSize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetSize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 1a0892fea469180a0d06eded30e4459667513acbf66d56161d81788c1a17820f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711638"
---
# <a name="iwicbitmapsource_getsize_proxy-function"></a>\_Função de \_ proxy IWICBitmapSource GetSize

Função de proxy para o método [**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICBitmapSource_GetSize_Proxy(
  _In_  IWICBitmapSource *THIS_PTR,
  _Out_ UINT             *puiWidth,
  _Out_ UINT             *puiHeight
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Isso \_ PTR* \[\]
</dt> <dd>

Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

Ponteiro para este objeto [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .

</dd> <dt>

*puiWidth* \[ fora\]
</dt> <dd>

Tipo: **uint \***

Um ponteiro que recebe a largura de pixel do bitmap.

</dd> <dt>

*puiHeight* \[ fora\]
</dt> <dd>

Tipo: **uint \***

Um ponteiro que recebe a altura do pixel do bitmap

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



 

 





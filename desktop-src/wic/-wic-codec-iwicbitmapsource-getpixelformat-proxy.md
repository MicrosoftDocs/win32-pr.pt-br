---
description: Função de proxy para o método GetPixelFormat.
ms.assetid: 0879bfb7-0175-4275-a093-a69b39c66a41
title: Função IWICBitmapSource_GetPixelFormat_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetPixelFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ff795dd028c8d8f1e18a944df60a87f1e7cee670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784552"
---
# <a name="iwicbitmapsource_getpixelformat_proxy-function"></a>\_Função de proxy IWICBitmapSource GetPixelFormat \_

Função de proxy para o método [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICBitmapSource_GetPixelFormat_Proxy(
  _In_  IWICBitmapSource   *THIS_PTR,
  _Out_ WICPixelFormatGUID *pPixelFormat
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Isso \_ PTR* \[\]
</dt> <dd>

Tipo: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _

Ponteiro para este objeto [_ *IWICBitmapSource* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .

</dd> <dt>

*pPixelFormat* \[ fora\]
</dt> <dd>

Tipo: **WICPixelFormatGUID \** _

Um ponteiro que recebe o formato de pixel GUID no qual o bitmap está armazenado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: _ *HRESULT**

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 





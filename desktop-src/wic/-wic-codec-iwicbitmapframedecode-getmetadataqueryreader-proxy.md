---
description: Função de proxy de função IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy para o método GetMetadataQueryReader.
ms.assetid: 2a3e0a59-3524-4da4-993a-607a3727faba
title: Função IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c6c00cc4463bd8540e5baeb41a10577e9f67e85c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091134"
---
# <a name="iwicbitmapframedecode_getmetadataqueryreader_proxy-function"></a>\_Função de \_ proxy GetMetadataQueryReader IWICBitmapFrameDecode

Função de proxy para o método [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy(
  _In_  IWICBitmapFrameDecode   *THIS_PTR,
  _Out_ IWICMetadataQueryReader **ppIMetadataQueryReader
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Isso \_ PTR* \[\]
</dt> <dd>

Tipo: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***

Ponteiro para este objeto [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .

</dd> <dt>

*ppIMetadataQueryReader* \[ fora\]
</dt> <dd>

Tipo: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***

Um ponteiro que recebe um ponteiro para um [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 





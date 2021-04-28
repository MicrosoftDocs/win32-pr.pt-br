---
description: Função de proxy de função IWICBitmapDecoder_GetMetadataQueryReader_Proxy para o método GetMetadataQueryReader.
ms.assetid: cc32bdf1-d807-46ac-87b7-77bf2d498e72
title: Função IWICBitmapDecoder_GetMetadataQueryReader_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetMetadataQueryReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ebda8edb5c2007b1dfb39ca9f406855da05c456a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100644"
---
# <a name="iwicbitmapdecoder_getmetadataqueryreader_proxy-function"></a>\_Função de \_ proxy IWICBitmapDecoder GetMetadataQueryReader

Função de proxy para o método [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICBitmapDecoder_GetMetadataQueryReader_Proxy(
  _In_  IWICBitmapDecoder       *THIS_PTR,
  _Out_ IWICMetadataQueryReader **ppIMetadataQueryReader
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Isso \_ PTR* \[\]
</dt> <dd>

Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***

Ponteiro para este objeto [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .

</dd> <dt>

*ppIMetadataQueryReader* \[ fora\]
</dt> <dd>

Tipo: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***

Um ponteiro que recebe um ponteiro para os metadados.

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



 

 





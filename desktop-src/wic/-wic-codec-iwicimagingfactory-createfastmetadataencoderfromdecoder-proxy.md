---
description: Função de proxy para o método CreateFastMetadataEncoderFromDecoder.
ms.assetid: eae7ed9c-9205-4e41-91b2-461fd1f5d093
title: Função IWICImagingFactory_CreateFastMetadataEncoderFromDecoder_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFastMetadataEncoderFromDecoder_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cdeb682139feb03c19cd66e999b6e3b8b7b366d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783782"
---
# <a name="iwicimagingfactory_createfastmetadataencoderfromdecoder_proxy-function"></a>\_Função de \_ proxy IWICImagingFactory CreateFastMetadataEncoderFromDecoder

Função de proxy para o método [**CreateFastMetadataEncoderFromDecoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromdecoder) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICImagingFactory_CreateFastMetadataEncoderFromDecoder_Proxy(
  _In_  IWICImagingFactory      *pFactory,
  _In_  IWICBitmapDecoder       *pIDecoder,
  _Out_ IWICFastMetadataEncoder **ppIFME
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFactory* \[ no\]
</dt> <dd>

Tipo: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_pIDecoder * \[ in\]
</dt> <dd>

Tipo: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _

O decodificador do qual criar o [_ *IWICFastMetadataEncoder* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) .

</dd> <dt>

*ppIFME* \[ fora\]
</dt> <dd>

Tipo: **[ **IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***

Um ponteiro que recebe um ponteiro para o novo [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder).

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



 

 





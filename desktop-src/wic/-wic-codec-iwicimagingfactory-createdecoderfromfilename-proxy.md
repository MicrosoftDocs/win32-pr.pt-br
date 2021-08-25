---
description: Função proxy para o método CreateDecoderFromFilename.
ms.assetid: 12c60899-0fe0-47d0-9026-48c74df328ef
title: IWICImagingFactory_CreateDecoderFromFilename_Proxy função
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromFilename_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: dabc24d17fdac881537d45e47a8cc6808a1cf805ac14025d7fdfcfa50eea8500
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056626"
---
# <a name="iwicimagingfactory_createdecoderfromfilename_proxy-function"></a>Função proxy IWICImagingFactory \_ CreateDecoderFromFilename \_

Função proxy para o [**método CreateDecoderFromFilename.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICImagingFactory_CreateDecoderFromFilename_Proxy(
  _In_        IWICImagingFactory  *pFactory,
  _In_        LPCWSTR             wzFilename,
  _In_  const GUID                *pguidVendor,
  _In_        DWORD               dwDesiredAccess,
  _In_        WICDecodeOptions    metadataOptions,
  _Out_       IWICBitmapDecoder   **ppIDecoder
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFactory* \[ Em\]
</dt> <dd>

Tipo: **IWICImagingFactory \***

</dd> <dt>

*wzFilename* \[ Em\]
</dt> <dd>

Tipo: **LPCWSTR**

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome de um objeto a ser criado ou aberto.

</dd> <dt>

*pguidVendor* \[ Em\]
</dt> <dd>

Tipo: **const \* GUID**

O GUID do fornecedor para o decodificador.

</dd> <dt>

*dwDesiredAccess* \[ Em\]
</dt> <dd>

Tipo: **DWORD**

O acesso ao objeto, que pode ser lido, escrito ou ambos.

Para obter mais informações, consulte [Arquivos de direitos de acesso e segurança de \[ arquivo \] ](../fileio/file-security-and-access-rights.md).

</dd> <dt>

*metadataOptions* \[ Em\]
</dt> <dd>

Tipo: **[ **WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**

O [**WICDecodeOptions a**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) ser usado ao criar o decodificador.

</dd> <dt>

*ppIDecoder* \[ out\]
</dt> <dd>

Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***

Um ponteiro que recebe um ponteiro para o [**novo IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).

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



 


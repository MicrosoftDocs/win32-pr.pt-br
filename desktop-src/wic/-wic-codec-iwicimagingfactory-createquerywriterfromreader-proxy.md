---
description: Função de proxy para o método CreateQueryWriterFromReader.
ms.assetid: 7784c5e9-38e0-43de-83db-4de3361fa20e
title: Função IWICImagingFactory_CreateQueryWriterFromReader_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateQueryWriterFromReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ee6e03da055b5e48e21c044ce1708a8a8871c30fabeb860e486cde398650c23f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711441"
---
# <a name="iwicimagingfactory_createquerywriterfromreader_proxy-function"></a>\_Função de \_ proxy IWICImagingFactory CreateQueryWriterFromReader

Função de proxy para o método [**CreateQueryWriterFromReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriterfromreader) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICImagingFactory_CreateQueryWriterFromReader_Proxy(
  _In_        IWICImagingFactory      *pFactory,
  _In_        IWICMetadataQueryReader *pIQueryReader,
  _In_  const GUID                    *pguidVendor,
  _Out_       IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFactory* \[ no\]
</dt> <dd>

Tipo: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

</dd> <dt>

*pIQueryReader* \[ no\]
</dt> <dd>

Tipo: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\***

O leitor de consulta de metadados do qual criar o gravador de metadados.

</dd> <dt>

*pguidVendor* \[ no\]
</dt> <dd>

Tipo: **GUID \* const**

O GUID do fornecedor para o gravador de consulta de metadados.

</dd> <dt>

*ppIQueryWriter* \[ fora\]
</dt> <dd>

Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***

Um ponteiro que recebe um ponteiro para um novo [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).

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



 

 





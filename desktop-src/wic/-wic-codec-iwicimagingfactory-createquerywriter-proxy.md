---
description: Função de proxy para o método CreateQueryWriter.
ms.assetid: 7f925117-6244-4be6-bcef-fa852672ac64
title: Função IWICImagingFactory_CreateQueryWriter_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fe37af1ebcc4c8fd95b578d363fdb498cb06c22f354b7e2ef8f5ed7a3b29ac01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088268"
---
# <a name="iwicimagingfactory_createquerywriter_proxy-function"></a>\_Função de \_ proxy IWICImagingFactory CreateQueryWriter

Função de proxy para o método [**CreateQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriter) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICImagingFactory_CreateQueryWriter_Proxy(
  _In_        IWICImagingFactory      *pFactory,
  _In_        REFGUID                 guidMetadataFormat,
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

*guidMetadataFormat* \[ no\]
</dt> <dd>

Tipo: **REFGUID**

O GUID para o formato de metadados desejado.

</dd> <dt>

*pguidVendor* \[ no\]
</dt> <dd>

Tipo: **GUID \* const**

O GUID do fornecedor do gravador de metadados.

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



 

 





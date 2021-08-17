---
description: Função proxy para o método CreateMetadataWriterFromReader.
ms.assetid: da9e80d3-3265-428d-987e-8b344472527a
title: IWICComponentFactory_CreateMetadataWriterFromReader_Proxy função
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentFactory_CreateMetadataWriterFromReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e08ca8b42a0ddf0997ee5945c11fa75257d82f1b3655969f3f29a50264b561fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206657"
---
# <a name="iwiccomponentfactory_createmetadatawriterfromreader_proxy-function"></a>Função proxy IWICComponentFactory \_ CreateMetadataWriterFromReader \_

Função proxy para o [**método CreateMetadataWriterFromReader.**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatawriterfromreader)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICComponentFactory_CreateMetadataWriterFromReader_Proxy(
  _In_        IWICComponentFactory *THIS_PTR,
  _In_        IWICMetadataReader   *pIReader,
  _In_  const GUID                 *pguidVendor,
  _Out_       IWICMetadataWriter   **ppIWriter
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ESTE \_ PTR* \[ em\]
</dt> <dd>

Tipo: **[ **IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)\***

Ponteiro para este [**objeto IWICComponentFactory.**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)

</dd> <dt>

*pIReader* \[ Em\]
</dt> <dd>

Tipo: **[ **IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)\***

</dd> <dt>

*pguidVendor* \[ Em\]
</dt> <dd>

Tipo: **const \* GUID**

</dd> <dt>

*ppIWriter* \[ out\]
</dt> <dd>

Tipo: **[ **IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)\*\***

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



 

 





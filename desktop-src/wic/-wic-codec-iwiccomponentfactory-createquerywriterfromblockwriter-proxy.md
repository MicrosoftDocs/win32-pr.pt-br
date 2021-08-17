---
description: Função proxy para o método CreateQueryWriterFromBlockWriter.
ms.assetid: f941e3b1-1645-4ed6-b2c5-180cb4c43fca
title: IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy função
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 44af8d96d39afff1eba582f9dea283a09acd69dbd4fc6dc95b3f568919621efe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965255"
---
# <a name="iwiccomponentfactory_createquerywriterfromblockwriter_proxy-function"></a>Função proxy IWICComponentFactory \_ CreateQueryWriterFromBlockWriter \_

Função proxy para o [**método CreateQueryWriterFromBlockWriter.**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createquerywriterfromblockwriter)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy(
  _In_  IWICComponentFactory    *THIS_PTR,
  _In_  IWICMetadataBlockWriter *pIBlockWriter,
  _Out_ IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ESTE \_ PTR* \[ em\]
</dt> <dd>

Tipo: **[ **IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)\***

Ponteiro para este [**objeto IWICComponentFactory.**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)

</dd> <dt>

*pIBlockWriter* \[ Em\]
</dt> <dd>

Tipo: **[ **IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)\***

</dd> <dt>

*ppIQueryWriter* \[ out\]
</dt> <dd>

Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***

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



 

 





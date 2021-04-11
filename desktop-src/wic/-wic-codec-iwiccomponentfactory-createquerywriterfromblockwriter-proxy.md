---
description: Função de proxy para o método CreateQueryWriterFromBlockWriter.
ms.assetid: f941e3b1-1645-4ed6-b2c5-180cb4c43fca
title: Função IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy
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
ms.openlocfilehash: c8c94b351e72fd7de367e5dd74a0c7ed62ce84f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170875"
---
# <a name="iwiccomponentfactory_createquerywriterfromblockwriter_proxy-function"></a>\_Função de \_ proxy IWICComponentFactory CreateQueryWriterFromBlockWriter

Função de proxy para o método [**CreateQueryWriterFromBlockWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createquerywriterfromblockwriter) .

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

*Isso \_ PTR* \[\]
</dt> <dd>

Tipo: **[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) \** _

Ponteiro para este objeto [_ *IWICComponentFactory* *](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) .

</dd> <dt>

*pIBlockWriter* \[ no\]
</dt> <dd>

Tipo: **[**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) \** _

</dd> <dt>

_ppIQueryWriter * \[ out\]
</dt> <dd>

Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***

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



 

 





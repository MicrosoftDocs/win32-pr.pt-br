---
description: Função de proxy para o método GetMetadataByName.
ms.assetid: 5685e282-637e-4db0-8654-fee12ae25112
title: Função IWICMetadataQueryReader_GetMetadataByName_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 96afa63f83e79f399b1c345d38ff2914307c2fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811977"
---
# <a name="iwicmetadataqueryreader_getmetadatabyname_proxy-function"></a>\_Função de \_ proxy IWICMetadataQueryReader GetMetadataByName

Função de proxy para o método [**GetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getmetadatabyname) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICMetadataQueryReader_GetMetadataByName_Proxy(
  _In_    IWICMetadataQueryReader *THIS_PTR,
  _In_    LPCWSTR                 wzName,
  _Inout_ PROPVARIANT             *pvarValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Isso \_ PTR* \[\]
</dt> <dd>

Tipo: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _

Ponteiro para este objeto [_ *IWICMetadataQueryReader* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .

</dd> <dt>

*wzName* \[ no\]
</dt> <dd>

Tipo: **LPCWSTR**

O nome do item de metadados solicitado.

</dd> <dt>

*pvarValue* \[ entrada, saída\]
</dt> <dd>

Tipo: **[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _

Ponteiro que recebe a propriedade de metadados.

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



 


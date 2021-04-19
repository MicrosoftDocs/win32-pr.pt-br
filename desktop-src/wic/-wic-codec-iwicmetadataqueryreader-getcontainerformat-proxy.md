---
description: Função de proxy para o método GetContainerFormat.
ms.assetid: 3a909151-53c2-4f82-9ead-f689b73f5faf
title: Função IWICMetadataQueryReader_GetContainerFormat_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8d8138a1217611ff60be9001ce038f9ecfbe7e34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764397"
---
# <a name="iwicmetadataqueryreader_getcontainerformat_proxy-function"></a>\_Função de \_ proxy IWICMetadataQueryReader GetContainerFormat

Função de proxy para o método [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICMetadataQueryReader_GetContainerFormat_Proxy(
  _In_  IWICMetadataQueryReader *THIS_PTR,
  _Out_ GUID                    *pguidContainerFormat
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Isso \_ PTR* \[\]
</dt> <dd>

Tipo: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _

Ponteiro para este objeto [_ *IWICMetadataQueryReader* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .

</dd> <dt>

*pguidContainerFormat* \[ fora\]
</dt> <dd>

Tipo: **GUID \** _

Ponteiro que recebe o GUID de formato cointainer.

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



 

 





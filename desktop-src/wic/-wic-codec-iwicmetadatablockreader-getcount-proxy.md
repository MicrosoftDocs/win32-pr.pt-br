---
description: Função de proxy para o método GetCount.
ms.assetid: 441bbbaf-5a6a-4d1e-bb8d-f79af6aa2708
title: Função IWICMetadataBlockReader_GetCount_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataBlockReader_GetCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 09c3c33185791c2c2eefd3963a3d39977c706963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171007"
---
# <a name="iwicmetadatablockreader_getcount_proxy-function"></a>Função de proxy do IWICMetadataBlockReader \_ GetCount \_

Função de proxy para o método [**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICMetadataBlockReader_GetCount_Proxy(
  _In_  IWICMetadataBlockReader *THIS_PTR,
  _Out_ UINT                    *pcCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Isso \_ PTR* \[\]
</dt> <dd>

Tipo: **[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) \** _

Ponteiro para este objeto [_ *IWICMetadataBlockReader* *](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) .

</dd> <dt>

*pcCount* \[ fora\]
</dt> <dd>

Tipo: **uint \** _

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



 

 





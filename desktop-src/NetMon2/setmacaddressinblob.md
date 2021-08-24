---
description: A função SetMacAddressInBlob define o endereço MAC solicitado de um BLOB.
ms.assetid: f44d0cec-ced7-4d2a-a58e-aeb476bfe800
title: Função SetMacAddressInBlob (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetMacAddressInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 20ed4a0358bc0aecada66858f9814bce94252ff9d705c971be947ca5af788ab3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364054"
---
# <a name="setmacaddressinblob-function"></a>Função SetMacAddressInBlob

A **função SetMacAddressInBlob** define o endereço MAC solicitado de um BLOB.

## <a name="syntax"></a>Sintaxe


```C++
DWORD SetMacAddressInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const BYTE  *pMacAddress
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hBlob* \[ Em\]
</dt> <dd>

Lidar com o BLOB que está sendo definido.

</dd> <dt>

*pOwnerName* \[ Em\]
</dt> <dd>

Ponteiro para o nome do **Proprietário do** BLOB que está sendo definido.

</dd> <dt>

*pCategoryName* \[ Em\]
</dt> <dd>

Ponteiro para o nome da **Categoria** BLOB que está sendo definido.

</dd> <dt>

*pTagName* \[ Em\]
</dt> <dd>

Ponteiro para o nome da **marca** BLOB que está sendo definido.

</dd> <dt>

*pMacAddress* \[ Em\]
</dt> <dd>

Ponteiro para o endereço MAC do BLOB que está sendo definido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será NMERR \_ SUCCESS.

Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[GetMacAddressFromBlob](getmacaddressfromblob.md)
</dt> <dt>

[SetBoolInBlob](setboolinblob.md)
</dt> <dt>

[SetClassIDInBlob](setclassidinblob.md)
</dt> <dt>

[SetDwordInBlob](setdwordinblob.md)
</dt> <dt>

[SetNetworkInfoInBlob](setnetworkinfoinblob.md)
</dt> <dt>

[SetNPPAddressFilterInBlob](setnppaddressfilterinblob.md)
</dt> <dt>

[SetNPPPatternFilterInBlob](setnpppatternfilterinblob.md)
</dt> <dt>

[SetNPPTriggerInBlob](setnpptriggerinblob.md)
</dt> <dt>

[SetStringInBlob](setstringinblob.md)
</dt> </dl>

 

 





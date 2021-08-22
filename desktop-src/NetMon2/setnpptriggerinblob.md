---
description: Define o gatilho BLOB.
ms.assetid: 88bfd5cd-f563-4d0c-81a3-54a846805b87
title: Função SetNPPTriggerInBlob (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPTriggerInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5ed344b3434e8ae53fe88e7ee97b77a6efa5bd3f0941af6cc9cbc6f2ff10304b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363774"
---
# <a name="setnpptriggerinblob-function"></a>Função SetNPPTriggerInBlob

A **função SetNPPTriggerInBlob** define o gatilho BLOB.

## <a name="syntax"></a>Sintaxe


```C++
DWORD SetNPPTriggerInBlob(
  _In_  HBLOB     hBlob,
  _In_  LPTRIGGER pTrigger,
  _Out_ HBLOB     hErrorBlob
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hBlob* \[ Em\]
</dt> <dd>

O alça para o BLOB.

</dd> <dt>

*pTrigger* \[ Em\]
</dt> <dd>

Um ponteiro para o valor do gatilho.

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

O handle para um BLOB de erro que especifica onde no BLOB original ocorreu o erro (se algum).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será NMERR \_ SUCCESS.

Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.

## <a name="remarks"></a>Comentários

Esses dados de gatilho são armazenados na **categoria Gatilho** do BLOB.

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

[GetNPPTriggerFromBlob](getnpptriggerfromblob.md)
</dt> <dt>

[SetBoolInBlob](setboolinblob.md)
</dt> <dt>

[SetClassIDInBlob](setclassidinblob.md)
</dt> <dt>

[SetDwordInBlob](setdwordinblob.md)
</dt> <dt>

[SetMacAddressInBlob](setmacaddressinblob.md)
</dt> <dt>

[SetNetworkInfoInBlob](setnetworkinfoinblob.md)
</dt> <dt>

[SetNPPAddressFilterInBlob](setnppaddressfilterinblob.md)
</dt> <dt>

[SetNPPPatternFilterInBlob](setnpppatternfilterinblob.md)
</dt> <dt>

[SetStringInBlob](setstringinblob.md)
</dt> </dl>

 

 





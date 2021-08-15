---
description: A função RegOpenBlobKey recupera um BLOB armazenado na chave do registro fornecida.
ms.assetid: f6b16c07-c705-47f1-a21c-6155368551c7
title: Função RegOpenBlobKey (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegOpenBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5d372d6cc69c4e80691f96075aaa0d9030c90d06fc8256f85a7ed2dc894f3fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364145"
---
# <a name="regopenblobkey-function"></a>Função RegOpenBlobKey

A função **RegOpenBlobKey** recupera um blob armazenado na chave do registro fornecida.

## <a name="syntax"></a>Sintaxe


```C++
DWORD RegOpenBlobKey(
  _In_        HKEY  hkey,
  _In_  const char  *szBlobName,
  _Out_       HBLOB *phBlob
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HKEY* \[ no\]
</dt> <dd>

Identificador para a chave do registro que contém o BLOB.

</dd> <dt>

*szBlobName* \[ no\]
</dt> <dd>

Nome que identifica o BLOB especificado no registro.

</dd> <dt>

*phBlob* \[ fora\]
</dt> <dd>

Ponteiro para o BLOB que é recuperado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.

Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[RegCreateBlobKey](regcreateblobkey.md)
</dt> </dl>

 

 





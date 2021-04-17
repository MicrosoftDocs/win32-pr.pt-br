---
description: A função RegCreateBlobKey armazena um BLOB na chave do registro fornecida.
ms.assetid: 14f3763e-aa04-4d51-b388-81ebf0d3952c
title: Função RegCreateBlobKey (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegCreateBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: fc46b38919b37dc004c1065b0cc8d5f80e65984c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768586"
---
# <a name="regcreateblobkey-function"></a>Função RegCreateBlobKey

A função **RegCreateBlobKey** armazena um blob na chave do registro fornecida.

## <a name="syntax"></a>Sintaxe


```C++
DWORD RegCreateBlobKey(
  _Out_       HKEY  hkey,
  _In_  const char  *szBlobName,
  _In_        HBLOB hBlob
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HKEY* \[ fora\]
</dt> <dd>

Manipule a chave do registro onde o BLOB será armazenado.

</dd> <dt>

*szBlobName* \[ no\]
</dt> <dd>

Nome (definido pelo aplicativo) que representa o BLOB no registro.

</dd> <dt>

*hBlob* \[ no\]
</dt> <dd>

Identificador para o BLOB que é salvo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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

[RegOpenBlobKey](regopenblobkey.md)
</dt> </dl>

 

 





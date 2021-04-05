---
description: A função GetProtocolFromName retorna um identificador para um protocolo de um determinado nome.
ms.assetid: 18f5a9a7-4245-479d-a0da-2ede362a60b8
title: Função GetProtocolFromName (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolFromName
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e104c066be2a5465083c7983aaefebd46f548b7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646793"
---
# <a name="getprotocolfromname-function"></a>Função GetProtocolFromName

A função **GetProtocolFromName** retorna um identificador para um protocolo de um determinado nome.

## <a name="syntax"></a>Sintaxe


```C++
HPROTOCOL WINAPI GetProtocolFromName(
  _In_ LPSTR ProtocolName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ProtocolName* \[ no\]
</dt> <dd>

Nome do protocolo (por exemplo, IP).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será um identificador de protocolo.

Se a função não for bem-sucedida, o valor de retorno será **nulo**.

## <a name="remarks"></a>Comentários

Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetProtocolFromName** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





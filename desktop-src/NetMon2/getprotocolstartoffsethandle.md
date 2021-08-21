---
description: A função GetProtocolStartOffsetHandle retorna o deslocamento de quadro de um determinado protocolo.
ms.assetid: b1e3a03b-f211-4c2c-8810-9e220c40136b
title: Função GetProtocolStartOffsetHandle (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolStartOffsetHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 18513b2b26233a5fc6680e5830f053fe2551d87bb9f09a95d39ab92cc4f7897a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117981824"
---
# <a name="getprotocolstartoffsethandle-function"></a>Função GetProtocolStartOffsetHandle

A função **GetProtocolStartOffsetHandle** retorna o deslocamento de quadro de um determinado protocolo.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI GetProtocolStartOffsetHandle(
  _In_ HFRAME    hFrame,
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFrame* \[ no\]
</dt> <dd>

Identificador para um quadro.

</dd> <dt>

*hProtocol* \[ no\]
</dt> <dd>

Identificador para um protocolo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será o deslocamento do quadro medido em bytes.

Se a função não for bem-sucedida, o valor de retorno será um (1).

## <a name="remarks"></a>Comentários

Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetProtocolStartOffsetHandle** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





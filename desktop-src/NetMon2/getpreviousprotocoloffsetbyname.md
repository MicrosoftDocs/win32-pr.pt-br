---
description: A função GetPreviousProtocolOffsetByName retorna a instância anterior de um determinado protocolo.
ms.assetid: 94f80776-564f-4089-9e3a-fdf38d9dfe8a
title: Função GetPreviousProtocolOffsetByName (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPreviousProtocolOffsetByName
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 17b472bbdead74612ccc6d76f1059443ce6f62dd122f7933ae31c99fb82900a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743756"
---
# <a name="getpreviousprotocoloffsetbyname-function"></a>Função GetPreviousProtocolOffsetByName

A função **GetPreviousProtocolOffsetByName** retorna a instância anterior de um determinado protocolo.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI GetPreviousProtocolOffsetByName(
  _In_  HFRAME hFrame,
  _In_  DWORD  dwStartOffset,
  _In_  LPSTR  szProtocolName,
  _Out_ DWORD  *pdwPreviousOffset
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFrame* \[ no\]
</dt> <dd>

Identificador para o quadro.

</dd> <dt>

*dwStartOffset* \[ no\]
</dt> <dd>

Deslocamento no quadro.

</dd> <dt>

*szProtocolName* \[ no\]
</dt> <dd>

Nome do protocolo que você deseja pesquisar.

</dd> <dt>

*pdwPreviousOffset* \[ fora\]
</dt> <dd>

Ponteiro para um **DWORD** que contém o deslocamento para o protocolo anterior (se a função tiver sucesso).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.

Se a função não for bem-sucedida, o valor de retorno será o \_ protocolo NMERR \_ não \_ encontrado.

## <a name="remarks"></a>Comentários

Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar o **GetPreviousProtocolOffsetByName**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





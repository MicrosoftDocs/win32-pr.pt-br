---
description: A função BERGetString decodifica uma cadeia de caracteres codificada em BER.
ms.assetid: 1f72f061-c0ed-4634-9709-e08c2b9468bb
title: Função BERGetString (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 6f8f864b8042ad49502ae53061e157575192e7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828232"
---
# <a name="bergetstring-function"></a>Função BERGetString

A função **BERGetString** decodifica uma cadeia de caracteres codificada em ber.

## <a name="syntax"></a>Sintaxe


```C++
BOOL BERGetString(
   LPBYTE  pCurrentPointer,
   LPBYTE  *ppValuePointer,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCurrentPointer* 
</dt> <dd>

Ponteiro para a cadeia de caracteres decodificada.

</dd> <dt>

*ppValuePointer* 
</dt> <dd>

Ponteiro para o ponteiro da cadeia de caracteres decodificada.

</dd> <dt>

*pHeaderLength* 
</dt> <dd>

Ponteiro para o comprimento do cabeçalho retornado.

</dd> <dt>

*pDataLength* 
</dt> <dd>

Ponteiro para o comprimento da cadeia de caracteres.

</dd> <dt>

*ppNext* 
</dt> <dd>

Ponteiro para o ponteiro da próxima entrada do BER.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida (ou seja, se uma cadeia de caracteres codificada em BER válida for decodificada), o valor de retorno será **true**.

Se a função não for bem-sucedida, o valor de retorno será **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 





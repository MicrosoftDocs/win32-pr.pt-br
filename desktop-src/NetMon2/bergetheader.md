---
description: A função BERGetHeader decodifica um cabeçalho Choice.
ms.assetid: 2574a9b3-c28e-43d1-904f-d45888617584
title: Função BERGetHeader (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetHeader
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5e2213b15b6b4d2cbaa15b3b9aa9de028e20a62d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766365"
---
# <a name="bergetheader-function"></a>Função BERGetHeader

A função **BERGetHeader** decodifica um cabeçalho Choice.

## <a name="syntax"></a>Sintaxe


```C++
BOOL BERGetHeader(
   LPBYTE  pCurrentPointer,
   LPBYTE  pTag,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCurrentPointer* 
</dt> <dd>

Ponteiro para o cabeçalho Choice.

</dd> <dt>

*pTag* 
</dt> <dd>

Ponteiro para a marca retornada.

</dd> <dt>

*pHeaderLength* 
</dt> <dd>

Ponteiro para o comprimento do cabeçalho retornado.

</dd> <dt>

*pDataLength* 
</dt> <dd>

Ponteiro para o comprimento dos dados retornados.

</dd> <dt>

*ppNext* 
</dt> <dd>

Ponteiro para o conteúdo do cabeçalho.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida (ou seja, um cabeçalho de escolha válido do BER for encontrado) o valor de retorno será **true**.

Se a função não for bem-sucedida, o valor de retorno será **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 





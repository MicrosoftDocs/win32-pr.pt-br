---
description: A função GetFrameTimeStamp retorna o carimbo de data/hora de um determinado quadro.
ms.assetid: 4ac50400-6674-40fa-9a69-9c0ccb55b92c
title: Função GetFrameTimeStamp (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameTimeStamp
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 37a75f946a5fc0ddb2b32d99334368a272fdf2e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757499"
---
# <a name="getframetimestamp-function"></a>Função GetFrameTimeStamp

A função **GetFrameTimeStamp** retorna o carimbo de data/hora de um determinado quadro.

## <a name="syntax"></a>Sintaxe


```C++
__int64 WINAPI GetFrameTimeStamp(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFrame* \[ no\]
</dt> <dd>

Identificador para o quadro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será o carimbo de data/hora do quadro em microssegundos.

Se a função não for bem-sucedida, o valor de retorno será menos um (-1).

## <a name="remarks"></a>Comentários

A função **GetFrameTimeStamp** retorna um carimbo de data/hora que mostra o tempo decorrido entre o início do processo de captura e a gravação do quadro.

Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetFrameTimeStamp** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





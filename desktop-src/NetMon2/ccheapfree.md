---
description: A função CCHeapFree libera a memória alocada pela função CCHeapAlloc.
ms.assetid: 4e1f3332-b0cb-4c21-8c36-59e14c9686cd
title: Função CCHeapFree (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapFree
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5e89ca9a7d00559724edc6679a0ed99e4bdf9c2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091726"
---
# <a name="ccheapfree-function"></a>Função CCHeapFree

A função **CCHeapFree** libera a memória alocada pela função **CCHeapAlloc** .

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI CCHeapFree(
   LPVOID lpMem
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpMem* 
</dt> <dd>

Ponteiro para a memória que esta função libera.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função **CCHeapFree** for bem-sucedida, o valor de retorno será **true**.

Se a função não for bem-sucedida, o valor de retorno será **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[SetCCInstPtr](setccinstptr.md)
</dt> <dt>

[GetCCInstPtr](getccinstptr.md)
</dt> <dt>

[CCHeapAlloc](ccheapalloc.md)
</dt> <dt>

[CCHeapReAlloc](ccheaprealloc.md)
</dt> <dt>

[CCHeapSize](ccheapsize.md)
</dt> </dl>

 

 





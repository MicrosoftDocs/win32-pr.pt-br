---
description: A função CCHeapSize retorna o tamanho da memória alocada pela função CCHeapAlloc.
ms.assetid: 45d0fd89-bcd1-4298-8cc3-834d86301f93
title: Função CCHeapSize (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapSize
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b086777b571af417662bd60a582fbc53a07c49300d21d2c59b6a36d2247b9d14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012296"
---
# <a name="ccheapsize-function"></a>Função CCHeapSize

A **função CCHeapSize** retorna o tamanho da memória alocada pela **função CCHeapAlloc.**

## <a name="syntax"></a>Sintaxe


```C++
SIZE_T WINAPI CCHeapSize(
   LPVOID lpMem
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpMem* 
</dt> <dd>

Ponteiro para a memória alocada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será o tamanho do bloco de memória solicitado medido em bytes.

Se a função não for bem-sucedida, o valor de retorno será **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[SetCCInstPtr](setccinstptr.md)
</dt> <dt>

[GetCCInstPtr](getccinstptr.md)
</dt> <dt>

[CCHeapAlloc](ccheapalloc.md)
</dt> <dt>

[CCHeapFree](ccheapfree.md)
</dt> <dt>

[CCHeapReAlloc](ccheaprealloc.md)
</dt> </dl>

 

 





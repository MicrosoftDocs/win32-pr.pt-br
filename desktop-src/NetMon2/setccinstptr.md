---
description: A função SetCCInstPtr captura um ponteiro de instância de contexto.
ms.assetid: 31924608-4aa1-4801-a5de-d8de054e12d9
title: Função SetCCInstPtr (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetCCInstPtr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 323e6334c90358dd8725f3f9092142275cfe491a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501889"
---
# <a name="setccinstptr-function"></a>Função SetCCInstPtr

A função **SetCCInstPtr** captura um ponteiro de instância de contexto.

## <a name="syntax"></a>Sintaxe


```C++
VOID WINAPI SetCCInstPtr(
   LPVOID lpCurCaptureInst
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpCurCaptureInst* 
</dt> <dd>

Ponteiro para os dados da instância adicionados à captura.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Nenhum.

## <a name="remarks"></a>Comentários

Use essa função para armazenar um ponteiro para um bloco que foi alocado com a função **CCHeapAlloc** . Cada analisador pode definir uma única instância de dados em uma captura.

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

[GetCCInstPtr](getccinstptr.md)
</dt> <dt>

[CCHeapAlloc](ccheapalloc.md)
</dt> <dt>

[CCHeapFree](ccheapfree.md)
</dt> <dt>

[CCHeapReAlloc](ccheaprealloc.md)
</dt> <dt>

[CCHeapSize](ccheapsize.md)
</dt> </dl>

 

 





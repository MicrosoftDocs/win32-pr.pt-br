---
description: A função CCHeapReAlloc realoca a memória alocada pela função CCHeapAlloc.
ms.assetid: 82365ce2-3980-44ff-be0f-062a65f676fc
title: Função CCHeapReAlloc (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapReAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e1619e2e6e81e8a265600f8437a6633e18065f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662139"
---
# <a name="ccheaprealloc-function"></a>Função CCHeapReAlloc

A função **CCHeapReAlloc** realoca a memória alocada pela função **CCHeapAlloc** .

## <a name="syntax"></a>Sintaxe


```C++
LPVOID WINAPI CCHeapReAlloc(
   LPVOID lpMem,
   DWORD  dwBytes,
   BOOL   bZeroInit
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpMem* 
</dt> <dd>

Ponteiro para a memória alocada original.

</dd> <dt>

*dwBytes* 
</dt> <dd>

Tamanho da memória realocada, medida em bytes.

</dd> <dt>

*bZeroInit* 
</dt> <dd>

Indicador de se a memória realocada foi inicializada. Se o valor do parâmetro for **true**, a memória realocada recentemente será inicializada para zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será um ponteiro para a memória realocada.

Se a função não for bem-sucedida, o valor de retorno será **nulo**.

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

[CCHeapFree](ccheapfree.md)
</dt> <dt>

[CCHeapSize](ccheapsize.md)
</dt> </dl>

 

 





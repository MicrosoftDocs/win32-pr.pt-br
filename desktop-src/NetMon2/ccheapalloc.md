---
description: A função CCHeapAlloc aloca memória em uma base captura por captura.
ms.assetid: 6403c35f-d78f-48dc-90cc-0b76260bbab7
title: Função CCHeapAlloc (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 14fce9f56103803e575d295799a5c5971ed1c459
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828229"
---
# <a name="ccheapalloc-function"></a>Função CCHeapAlloc

A função **CCHeapAlloc** aloca memória em uma base captura por captura.

## <a name="syntax"></a>Sintaxe


```C++
LPVOID WINAPI CCHeapAlloc(
   DWORD dwBytes,
   BOOL  bZeroInit
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwBytes* 
</dt> <dd>

Comprimento solicitado da memória alocada.

</dd> <dt>

*bZeroInit* 
</dt> <dd>

Indicador de se a memória alocada foi inicializada. Se o valor do parâmetro for **true**, a memória alocada será inicializada para zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será um ponteiro para a memória alocada. Quando você terminar de usar a memória alocada, libere a memória chamando a função [**CCHeapFree**](ccheapfree.md) .

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

[**SetCCInstPtr**](setccinstptr.md)
</dt> <dt>

[**GetCCInstPtr**](getccinstptr.md)
</dt> <dt>

[**CCHeapFree**](ccheapfree.md)
</dt> <dt>

[**CCHeapReAlloc**](ccheaprealloc.md)
</dt> <dt>

[**CCHeapSize**](ccheapsize.md)
</dt> </dl>

 

 





---
description: Copia o conteúdo de um bloco de memória de origem para um bloco de memória de destino e dá suporte a blocos de memória de origem e destino sobrepostos.
ms.assetid: D374F14D-24C7-4771-AD40-3AC37E7A2D2F
title: Função RtlMoveMemory (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlMoveMemory
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 65f8c8490224213e0bef27fab5239a21eca24344
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753889"
---
# <a name="rtlmovememory-function"></a>Função RtlMoveMemory

Copia o conteúdo de um bloco de memória de origem para um bloco de memória de destino e dá suporte a blocos de memória de origem e destino sobrepostos.

## <a name="syntax"></a>Sintaxe


```C++
VOID RtlMoveMemory(
  _Out_       VOID UNALIGNED *Destination,
  _In_  const VOID UNALIGNED *Source,
  _In_        SIZE_T         Length
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Destino* \[ fora\]
</dt> <dd>

Um ponteiro para o bloco de memória de destino para o qual copiar os bytes.

</dd> <dt>

*Origem* \[ do no\]
</dt> <dd>

Um ponteiro para o bloco de memória de origem para o qual copiar os bytes.

</dd> <dt>

*Comprimento* \[ no\]
</dt> <dd>

O número de bytes a serem copiados da origem para o destino.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Nenhum

## <a name="remarks"></a>Comentários

O bloco de memória de origem, que é definido pela *origem* e o *comprimento*, pode se sobrepor ao bloco de memória de destino, que é definido pelo *destino* e pelo *comprimento*.

A rotina [**RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory) é executada mais rápido que **RtlMoveMemory**, mas o **RtlCopyMemory** requer que os blocos de memória de origem e destino não se sobreponham.

Os chamadores de **RtlMoveMemory** podem ser executados em qualquer IRQL se os blocos de memória de origem e destino estiverem em memória de sistema não paginável. Caso contrário, o chamador deve estar em execução em IRQL <= nível da APC \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                    |
| Plataforma de destino<br/>          | <dl> <dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| parâmetro<br/>                   | <dl> <dt>WDM. h (incluindo WDM. h, Ntddk. h ou Ntifs. h)</dt> </dl>                   |
| Biblioteca<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory)
</dt> </dl>

 

 

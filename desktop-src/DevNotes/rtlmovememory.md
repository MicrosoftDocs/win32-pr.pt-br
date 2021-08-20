---
description: Copia o conteúdo de um bloco de memória de origem para um bloco de memória de destino e dá suporte a blocos de memória de origem e de destino sobrepostos.
ms.assetid: D374F14D-24C7-4771-AD40-3AC37E7A2D2F
title: Função RtlMoveMemory (Wdm.h)
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
ms.openlocfilehash: bf4366633de321e27f6d3cdc0396fcdce81b0dac30b0d09a4c2c4675706d939e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161658"
---
# <a name="rtlmovememory-function"></a>Função RtlMoveMemory

Copia o conteúdo de um bloco de memória de origem para um bloco de memória de destino e dá suporte a blocos de memória de origem e de destino sobrepostos.

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

*Destino* \[ out\]
</dt> <dd>

Um ponteiro para o bloco de memória de destino para o que copiar os bytes.

</dd> <dt>

*Origem* \[ Em\]
</dt> <dd>

Um ponteiro para o bloco de memória de origem do que copiar os bytes.

</dd> <dt>

*Comprimento* \[ Em\]
</dt> <dd>

O número de bytes a copiar da origem para o destino.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Nenhum

## <a name="remarks"></a>Comentários

O bloco de memória de origem, que é definido por *Origem* e *Comprimento,* pode sobrepor o bloco de memória de destino, que é definido por *Destino* e *Comprimento*.

A [**rotina RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory) é executado mais rapidamente do que **RtlMoveMemory,** mas **RtlCopyMemory** requer que os blocos de memória de origem e de destino não se sobreponham.

Os chamadores **de RtlMoveMemory** poderão ser executados em qualquer IRQL se os blocos de memória de origem e de destino estão na memória do sistema não papagada. Caso contrário, o chamador deverá estar em execução em IRQL <= APC \_ LEVEL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                    |
| Plataforma de destino<br/>          | <dl> <dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Cabeçalho<br/>                   | <dl> <dt>Wdm.h (inclua Wdm.h, Ntddk.h ou Ntifs.h)</dt> </dl>                   |
| Biblioteca<br/>                  | <dl> <dt>Ntdll.lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory)
</dt> </dl>

 

 

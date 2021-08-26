---
description: Evento de rastreamento de gerenciamento de memória para uma operação de alocação de heap.
ms.assetid: 572DEC3B-F909-45E5-849F-707AA62F2F5E
title: ETW_HEAP_EVENT_ALLOC evento (Ntwmi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_ALLOC
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: 111c9268cb6ad174dc79323a9b867923e6264428f939caeae7089685e62f4318
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963196"
---
# <a name="etw_heap_event_alloc-event"></a>Evento ETW \_ HEAP \_ EVENT \_ ALLOC

O **evento ETW \_ HEAP EVENT \_ \_ ALLOC** é um evento de rastreamento de gerenciamento de memória para uma operação de alocação de heap.


```C++
typedef struct ETW_HEAP_EVENT_ALLOC
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HeapHandle* 
</dt> <dd>

O alça do heap em que a memória foi alocada. Esse é o heap handle de um aplicativo passado para a [**função AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) quando a memória foi alocada.

</dd> <dt>

*Tamanho* 
</dt> <dd>

O tamanho em bytes alocados do heap.

</dd> <dt>

*Endereço* 
</dt> <dd>

O endereço da memória que foi alocada.

</dd> <dt>

*Origem* 
</dt> <dd>

A origem da memória que o alocador usou para a alocação de heap.

A tabela a seguir lista os valores possíveis para *o parâmetro Source* conforme definido no arquivo de *header ntetw.h:*



| Valor                                                                                                                                                                                                                                                                               | Significado                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <dt>**MEMORY \_ FROM \_ LOOKASIDE**</dt> <dt>1</dt> </dl>                                       | Memória da lista lookaside.<br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <dt>**MEMORY \_ FROM \_ LOWFRAG**</dt> <dt>2</dt> </dl>                                             | Memória do heap de baixa fragmentação.<br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <dt>**MEMORY \_ FROM \_ MAINPATH**</dt> <dt>3</dt> </dl>                                          | Memória do caminho do código principal.<br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <dt> **MEMÓRIA \_ DE \_ SLOWPATH**</dt> <dt>4</dt> </dl> | Memória do caminho lento.<br/>                                            |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <dt>**MEMORY \_ FROM \_ INVALID**</dt> <dt>5</dt> </dl>                                             | Memória que não era válida.<br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <dt>**MEMORY \_ DO \_ \_ HEAP DE SEGMENTO**</dt> <dt>6</dt> </dl>                             | Esse valor é reservado para uso futuro e nunca será retornado.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

O **evento ETW \_ HEAP EVENT \_ \_ ALLOC** é registrado em todas as alocações de heap.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>Ntwmi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de rastreamento de gerenciamento de memória](memory-management-tracing-events.md)
</dt> </dl>

 

 

---
description: Evento de rastreamento de gerenciamento de memória para uma operação de realocação de heap.
ms.assetid: D8080B7B-CECC-40DB-B52A-2C3E4F04ABA9
title: ETW_HEAP_EVENT_REALLOC evento (Ntwmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_REALLOC
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: 7aec225793967c38b97fecae88d28141e48a3cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787088"
---
# <a name="etw_heap_event_realloc-event"></a>\_Evento de \_ realocação de evento de heap do ETW \_

O evento de **\_ \_ \_ realocação do evento de heap do ETW** é um evento de rastreamento de gerenciamento de memória para uma operação de realocação de heap.


```C++
typedef struct ETW_HEAP_EVENT_REALLOC
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HeapHandle* 
</dt> <dd>

O identificador do heap em que a memória foi alocada. Esse é o identificador de heap que um aplicativo passou para a função [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) quando a memória foi alocada.

</dd> <dt>

*NewAddress* 
</dt> <dd>

O novo endereço da memória que foi alocada.

</dd> <dt>

*OldAddress* 
</dt> <dd>

O endereço antigo da memória que foi alocada anteriormente.

</dd> <dt>

*NewSize* 
</dt> <dd>

O novo tamanho em bytes alocado a partir do heap.

</dd> <dt>

*OldSize* 
</dt> <dd>

O tamanho antigo em bytes alocados anteriormente do heap.

</dd> <dt>

*Origem* 
</dt> <dd>

A origem da memória que o alocador usou para a alocação de heap.

A tabela a seguir lista os possíveis valores para o parâmetro de *origem* , conforme definido no arquivo de cabeçalho *ntetw. h* :



| Valor                                                                                                                                                                                                                                                                               | Significado                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <dt>**Memória \_ do DA \_ parte da**</dt> parte <dt>1</dt> </dl>                                       | Memória da lista à parte.<br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <dt>**Memória \_ do DO \_ LOWFRAG**</dt> <dt>2</dt> </dl>                                             | Memória do heap de baixa fragmentação.<br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <dt>**Memória \_ do DO \_ MAINPATH**</dt> <dt>3</dt> </dl>                                          | Memória do caminho de código principal.<br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <dt> **Memória \_ do \_ SLOWPATH**</dt> <dt>4</dt> </dl> | Memória de c lento.<br/>                                               |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <dt>**Memória \_ do DE \_**</dt> <dt>5</dt> inválido </dl>                                             | Memória inválida.<br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <dt>**Memória \_ do DO \_ \_ heap de segmento**</dt> <dt>6</dt> </dl>                             | Esse valor é reservado para uso futuro e nunca será retornado.<br/> |



 

</dd> </dl>

Este evento não tem parâmetros.

## <a name="remarks"></a>Comentários

O evento de **\_ \_ \_ realocação do evento de heap do ETW** é registrado em todas as realocações de heap.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Ntwmi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de rastreamento de gerenciamento de memória](memory-management-tracing-events.md)
</dt> </dl>

 

 

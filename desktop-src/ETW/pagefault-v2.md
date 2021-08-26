---
description: Essa classe é a classe pai para eventos de falha de página. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: cc349e75-fe81-427e-8cf9-15c76e8e4dad
title: PageFault_V2 classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_V2
api_type:
- NA
api_location: ''
ms.openlocfilehash: bd8adfa698975f7661abdbd849136d04049b5539ff3fed3b52b61660791add0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900746"
---
# <a name="pagefault_v2-class"></a>Classe PageFault \_ V2

Essa classe é a classe pai para eventos de falha de página.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Guid("{3d6fa8d3-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class PageFault_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membros

A **classe PageFault \_ V2** não define nenhum membro.

## <a name="remarks"></a>Comentários

Para habilitar todos os eventos de falha de página em uma sessão de log do Kernel NT, especifique o sinalizador **EVENT TRACE MEMORY PAGE \_ \_ \_ \_ \_ FAULTS** no membro **EnableFlags** de uma estrutura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a [**função StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea) Você também pode especificar os seguintes sinalizadores:

-   **FALHAS DE MEMÓRIA DE SINALIZADOR DE RASTREAMENTO \_ \_ DE \_ \_ \_ EVENTO**
-   **ALOCUIDADE \_ VIRTUAL DO SINALIZADOR DE RASTREAMENTO DE \_ \_ \_ EVENTOS**

Os consumidores de rastreamento de eventos podem implementar o processamento especial para todos os eventos de falha de página chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**PageFaultGuid**](nt-kernel-logger-constants.md) como o *parâmetro pGuid.* Use os seguintes tipos de evento para identificar o evento de memória real ao consumir eventos.



| Tipo de evento                                                     | Descrição                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EVENT \_ TRACE TYPE MM MM MM \_ \_ \_ (O valor do tipo de evento é 12)<br/> | Evento copy-on-write. A [**classe MOF \_ PageFault TypeGroup1**](pagefault-typegroup1.md) define os dados de evento para esse evento. Antes de Windows Vista, a classe [**MOF PageFault \_ TransitionFault**](pagefault-transitionfault.md) define o evento .     |
| EVENT \_ TRACE TYPE MM \_ \_ \_ DZF(O valor do tipo de evento é 11)<br/> | Exigir zero evento de falha. A [**classe MOF \_ PageFault TypeGroup1**](pagefault-typegroup1.md) define os dados de evento para esse evento. Antes de Windows Vista, a classe [**MOF PageFault \_ TransitionFault**](pagefault-transitionfault.md) define o evento . |
| EVENT \_ TRACE TYPE MM \_ \_ \_ GPF(O valor do tipo de evento é 13)<br/> | Evento de falha de página de proteção. A [**classe MOF \_ PageFault TypeGroup1**](pagefault-typegroup1.md) define os dados de evento para esse evento. Antes de Windows Vista, a classe [**MOF PageFault \_ TransitionFault**](pagefault-transitionfault.md) define o evento .  |
| EVENT \_ TRACE TYPE MM \_ \_ \_ HPF(O valor do tipo de evento é 14)<br/> | Evento de falha de página dura. A [**classe MOF \_ PageFault TypeGroup1**](pagefault-typegroup1.md) define os dados de evento para esse evento. Antes de Windows Vista, a classe [**MOF PageFault \_ TransitionFault**](pagefault-transitionfault.md) define o evento .   |
| EVENT \_ TRACE TYPE MM \_ \_ \_ TF(O valor do tipo de evento é 10)<br/>  | Evento de falha de transição. A [**classe MOF \_ PageFault TypeGroup1**](pagefault-typegroup1.md) define os dados de evento para esse evento. Antes de Windows Vista, a classe [**MOF PageFault \_ TransitionFault**](pagefault-transitionfault.md) define o evento .  |
| EVENT \_ TRACE TYPE MM \_ \_ \_ AV(O valor do tipo de evento é 15)<br/>  | Evento de violação de acesso. A [**classe MOF \_ PageFault TypeGroup1**](pagefault-typegroup1.md) define os dados de evento para esse evento.                                                                                                                           |
| Valor do tipo de evento, 32                                           | Evento de falha de página dura. A [**classe MOF \_ PageFault HardFault**](pagefault-hardfault.md) define os dados de evento para esse evento.                                                                                                                               |
| Valor do tipo de evento, 105                                          | Carregamento de imagem no evento de arquivo de página. A [**classe \_ MOF PageFault ImageLoadBacked**](pagefault-imageloadbacked.md) define os dados de evento para esse evento.                                                                                                          |
| Valor do tipo de evento, 98                                           | Evento de alocação virtual. A [**classe MOF VirtualAlloc**](pagefault-virtualalloc.md) define os dados de evento para esse evento.                                                                                                                                |
| Valor do tipo de evento, 99                                           | Evento virtual gratuito. A [**classe MOF VirtualAlloc**](pagefault-virtualalloc.md) define os dados de evento para esse evento.                                                                                                                                      |



 

Você pode usar os **membros ProcessId** e **ThreadId** do [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) para identificar o processo ou thread com falha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/> |



 

 

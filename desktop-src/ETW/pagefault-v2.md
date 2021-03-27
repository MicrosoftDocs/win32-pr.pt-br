---
description: Essa classe é a classe pai para eventos de falha de página. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: cc349e75-fe81-427e-8cf9-15c76e8e4dad
title: Classe PageFault_V2
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
ms.openlocfilehash: a545e8ae7c5afb000c26d89d9359f620fa7a653d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967422"
---
# <a name="pagefault_v2-class"></a>\_Classe falhadepágina v2

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

A classe **falhadepágina \_ v2** não define nenhum membro.

## <a name="remarks"></a>Comentários

Para habilitar todos os eventos de falha de página em uma sessão de log de kernel NT, especifique o sinalizador de **\_ \_ \_ \_ \_ falhas de página do sinalizador de rastreamento de eventos** no membro **EnableFlags** de uma estrutura de [**\_ \_ Propriedades de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a função [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) . Você também pode especificar os seguintes sinalizadores:

-   **\_falhas de \_ memória do sinalizador de rastreamento de \_ \_ eventos \_**
-   **\_ \_ alocação virtual do sinalizador de rastreamento de \_ eventos \_**

Os consumidores de rastreamento de eventos podem implementar processamento especial para todos os eventos de falha de página chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**PageFaultGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* . Use os tipos de evento a seguir para identificar o evento de memória real ao consumir eventos.



| Tipo de evento                                                     | Descrição                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ Tipo de rastreamento \_ de evento mm \_ vaca (o valor do tipo de evento é 12)<br/> | Evento de cópia em gravação. A classe [**falhadepágina \_ TypeGroup1**](pagefault-typegroup1.md) MOF define os dados do evento para esse evento. Antes do Windows Vista, a classe [**falhadepágina \_ TransitionFault**](pagefault-transitionfault.md) MOF define o evento.     |
| \_ \_ Tipo de rastreamento \_ de evento mm \_ DZF (o valor do tipo de evento é 11)<br/> | Evento de falha de demanda zero. A classe [**falhadepágina \_ TypeGroup1**](pagefault-typegroup1.md) MOF define os dados do evento para esse evento. Antes do Windows Vista, a classe [**falhadepágina \_ TransitionFault**](pagefault-transitionfault.md) MOF define o evento. |
| \_ \_ Tipo de rastreamento \_ de evento mm \_ GPF (o valor do tipo de evento é 13)<br/> | Evento de falha de página de proteção. A classe [**falhadepágina \_ TypeGroup1**](pagefault-typegroup1.md) MOF define os dados do evento para esse evento. Antes do Windows Vista, a classe [**falhadepágina \_ TransitionFault**](pagefault-transitionfault.md) MOF define o evento.  |
| \_ \_ Tipo de rastreamento \_ de evento mm \_ HPF (o valor do tipo de evento é 14)<br/> | Evento de falha de página de hardware. A classe [**falhadepágina \_ TypeGroup1**](pagefault-typegroup1.md) MOF define os dados do evento para esse evento. Antes do Windows Vista, a classe [**falhadepágina \_ TransitionFault**](pagefault-transitionfault.md) MOF define o evento.   |
| \_ \_ Tipo de rastreamento \_ de evento mm \_ TF (o valor do tipo de evento é 10)<br/>  | Evento de falha de transição. A classe [**falhadepágina \_ TypeGroup1**](pagefault-typegroup1.md) MOF define os dados do evento para esse evento. Antes do Windows Vista, a classe [**falhadepágina \_ TransitionFault**](pagefault-transitionfault.md) MOF define o evento.  |
| \_ \_ Tipo de rastreamento \_ de evento mm \_ AV (o valor do tipo de evento é 15)<br/>  | Evento de violação de acesso. A classe [**falhadepágina \_ TypeGroup1**](pagefault-typegroup1.md) MOF define os dados do evento para esse evento.                                                                                                                           |
| Valor do tipo de evento, 32                                           | Evento de falha de página de hardware. A classe [**falhadepágina \_ HardFault**](pagefault-hardfault.md) MOF define os dados do evento para esse evento.                                                                                                                               |
| Valor do tipo de evento, 105                                          | Carregamento de imagem no evento de arquivo de paginação. A classe [**falhadepágina \_ ImageLoadBacked**](pagefault-imageloadbacked.md) MOF define os dados do evento para esse evento.                                                                                                          |
| Valor do tipo de evento, 98                                           | Evento de alocação virtual. A classe do [**VirtualAlloc**](pagefault-virtualalloc.md) MOF define os dados do evento para esse evento.                                                                                                                                |
| Valor do tipo de evento, 99                                           | Evento livre virtual. A classe do [**VirtualAlloc**](pagefault-virtualalloc.md) MOF define os dados do evento para esse evento.                                                                                                                                      |



 

Você pode usar os membros **ProcessId** e **ThreadID** do [**\_ \_ cabeçalho de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) para identificar o processo ou thread com falha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



 

 

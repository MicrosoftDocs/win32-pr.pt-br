---
description: Essa classe é a classe pai para eventos de contador de desempenho. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 2606fea3-0651-4f7f-83a6-63021039eb95
title: Classe PerfInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PerfInfo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 93f12242fef86e5eab81bb702b783eb1f4c1915c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967439"
---
# <a name="perfinfo-class"></a>Classe PerfInfo

Essa classe é a classe pai para eventos de contador de desempenho.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Guid("{ce1dbfb4-137e-4da6-87b0-3f59aa102cbc}"), EventVersion(2)]
class PerfInfo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membros

A classe **PerfInfo** não define nenhum membro.

## <a name="remarks"></a>Comentários

Para habilitar eventos de DPC (chamada de procedimento deferida) em uma sessão de log do kernel NT, especifique o sinalizador de DPC do sinalizador de rastreamento de eventos no membro **EnableFlags** de uma [](/windows/win32/api/evntrace/nf-evntrace-starttracea) estrutura de [**Propriedades de \_ rastreamento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a função StartTrace. **\_ \_ \_** Você também pode especificar um ou mais dos seguintes sinalizadores:

-   **\_interrupção do \_ sinalizador de rastreamento de eventos \_**
-   **\_perfil do \_ sinalizador de rastreamento de eventos \_**
-   **sinalizador de rastreamento de eventos \_ \_ \_ SYSTEMCALL**

Os consumidores de rastreamento de eventos podem implementar processamento especial para eventos DPC chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**PerfInfoGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* . Use os tipos de evento a seguir para identificar o evento real ao consumir eventos.



| Tipo de evento           | Descrição                                                                                                          |
|----------------------|----------------------------------------------------------------------------------------------------------------------|
| Valor do tipo de evento, 46 | Exemplo de evento de perfil. A classe MOF [**SampledProfile**](sampledprofile.md) define os dados do evento para esse evento. |
| Valor do tipo de evento, 51 | Evento de entrada de chamada do sistema. A classe MOF [**SysCallEnter**](syscallenter.md) define os dados do evento para esse evento.   |
| Valor do tipo de evento, 52 | Evento de saída de chamada do sistema. A classe MOF [**SysCallExit**](syscallexit.md) define os dados do evento para esse evento.      |
| Valor do tipo de evento, 66 | Evento de DPC threaded. A classe do MOF [**DPC**](dpc.md) define os dados do evento para esse evento.                          |
| Valor do tipo de evento, 67 | Evento da rotina de serviço de interrupção (ISR). A classe do MOF do [**ISR**](isr.md) define os dados do evento para esse evento.       |
| Valor do tipo de evento, 68 | Evento DPC. A classe do MOF [**DPC**](dpc.md) define os dados do evento para esse evento.                                   |
| Valor do tipo de evento, 69 | Evento de timer de DPC. A classe do MOF [**DPC**](dpc.md) define os dados do evento para esse evento.                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 

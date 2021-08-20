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
ms.openlocfilehash: 641ebb361d14fa8abb0c8199cf113cfd85a2e6700e262447c1302f3f1b66231a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151402"
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

A **classe PerfInfo** não define nenhum membro.

## <a name="remarks"></a>Comentários

Para habilitar eventos DPC (chamada de procedimento adiado) em uma sessão de log do Kernel NT, especifique o sinalizador **\_ \_ \_ DPC DO** SINALIZADOR DE RASTREAMENTO DE EVENTOS no membro **EnableFlags** de uma estrutura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a [**função StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea) Você também pode especificar um ou mais dos seguintes sinalizadores:

-   **INTERRUPÇÃO \_ DO SINALIZADOR DE RASTREAMENTO DE \_ \_ EVENTO**
-   **PERFIL DO \_ SINALIZADOR DE RASTREAMENTO DE \_ \_ EVENTOS**
-   **SYSTEMCALL \_ DO SINALIZADOR DE RASTREAMENTO DE \_ \_ EVENTOS**

Os consumidores de rastreamento de eventos podem implementar o processamento especial para eventos DPC chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**PerfInfoGuid**](nt-kernel-logger-constants.md) como o *parâmetro pGuid.* Use os seguintes tipos de evento para identificar o evento real ao consumir eventos.



| Tipo de evento           | Descrição                                                                                                          |
|----------------------|----------------------------------------------------------------------------------------------------------------------|
| Valor do tipo de evento, 46 | Evento de perfil de exemplo. A [**classe MOF SampledProfile**](sampledprofile.md) define os dados de evento para esse evento. |
| Valor do tipo de evento, 51 | Evento de entrada de chamada do sistema. A [**classe MOF SysCallEnter**](syscallenter.md) define os dados de evento para esse evento.   |
| Valor do tipo de evento, 52 | Evento de saída de chamada do sistema. A [**classe MOF SysCallExit**](syscallexit.md) define os dados de evento para esse evento.      |
| Valor do tipo de evento, 66 | Evento DPC threaded. A [**classe MOF DPC**](dpc.md) define os dados de evento para esse evento.                          |
| Valor do tipo de evento, 67 | Evento ISR (rotina de serviço de interrupção). A [**classe ISR**](isr.md) MOF define os dados de evento para esse evento.       |
| Valor do tipo de evento, 68 | Evento DPC. A [**classe MOF DPC**](dpc.md) define os dados de evento para esse evento.                                   |
| Valor do tipo de evento, 69 | Evento de temporizador DPC. A [**classe MOF DPC**](dpc.md) define os dados de evento para esse evento.                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 

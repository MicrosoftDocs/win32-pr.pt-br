---
description: Classe UdpIp – essa classe é a classe pai para eventos UDP/IP. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 0fbecad2-0221-408e-9f43-859547efa803
title: Classe UdpIp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp
api_type:
- NA
api_location: ''
ms.openlocfilehash: d76aeb00ece18b026d9e5515a74ce830eb14af32
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105384"
---
# <a name="udpip-class"></a>Classe UdpIp

Essa classe é a classe pai para eventos UDP/IP.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Guid("{bf3a50c5-a9c9-4988-a005-2df0b7c80f80}"), EventVersion(2)]
class UdpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membros

A classe **UdpIp** não define nenhum membro.

## <a name="remarks"></a>Comentários

Para habilitar eventos UDP/IP em uma sessão de log de kernel NT, especifique o sinalizador **\_ \_ \_ \_ tcpip de rede sinalizador de rastreamento de eventos** no membro **EnableFlags** de uma estrutura de [**\_ \_ Propriedades de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a função [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .

Os consumidores de rastreamento de eventos podem implementar processamento especial para eventos UDP/IP chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**UdpIpGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* . Use os seguintes tipos de evento para identificar o evento de rede (UDP/IP) real ao consumir eventos.



| Tipo de evento                                                         | Descrição                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ de Tipo de rastreamento \_ \_ Receive**(o valor do tipo de evento é 11)<br/> | Receber evento para o protocolo IPv4. A classe [**UdpIp \_ TypeGroup1**](udpip-typegroup1.md) MOF define os dados do evento para esse evento. |
| **Evento \_ de Tipo de rastreamento \_ \_ Send**(o valor do tipo de evento é 10)<br/>    | Enviar evento para o protocolo IPv4. A classe [**UdpIp \_ TypeGroup1**](udpip-typegroup1.md) MOF define os dados do evento para esse evento.    |
| Valor do tipo de evento, 17                                               | Evento Fail. A classe [**UdpIp \_ Fail**](udpip-fail.md) MOF define os dados do evento para esse evento.                                  |
| Valor do tipo de evento, 26                                               | Enviar evento para o protocolo IPv6. A classe [**UdpIp \_ TypeGroup2**](udpip-typegroup2.md) MOF define os dados do evento para esse evento.    |
| Valor do tipo de evento, 27                                               | Receber evento para o protocolo IPv6. A classe [**UdpIp \_ TypeGroup2**](udpip-typegroup2.md) MOF define os dados do evento para esse evento. |



 

Você pode rastrear eventos de rede para um processo de origem e de destino usando a propriedade **ProcessId** . Como alguns eventos de rede são registrados por threads separados, talvez você não possa usar os membros **ProcessId** e **ThreadID** do [**\_ \_ cabeçalho de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) para identificar o processo ou thread que originou as atividades de rede.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**Falha de UdpIp \_**](udpip-fail.md)
</dt> <dt>

[**UdpIp \_ TypeGroup1**](udpip-typegroup1.md)
</dt> <dt>

[**UdpIp \_ TypeGroup2**](udpip-typegroup2.md)
</dt> <dt>

[**UdpIp \_ V0**](udpip-v0.md)
</dt> <dt>

[**UdpIp \_ v1**](udpip-v1.md)
</dt> </dl>

 

 

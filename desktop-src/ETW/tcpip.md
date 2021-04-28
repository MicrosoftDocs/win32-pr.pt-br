---
description: Classe TcpIp-essa classe é a classe pai para eventos TCP/IP. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: f9d6ea8f-c777-4747-89f4-f389c6eeac35
title: Classe TcpIp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp
api_type:
- NA
api_location: ''
ms.openlocfilehash: abcd805b417451adf2122e7baf3310be101a35ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105724"
---
# <a name="tcpip-class"></a>Classe TcpIp

Essa classe é a classe pai para eventos TCP/IP.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Guid("{9a280ac0-c8e0-11d1-84e2-00c04fb998a2}"), EventVersion(2)]
class TcpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membros

A classe **tcpip** não define nenhum membro.

## <a name="remarks"></a>Comentários

Para habilitar eventos TCP/IP em uma sessão de log de kernel NT, especifique o sinalizador **\_ \_ \_ \_ tcpip de rede sinalizador de rastreamento de eventos** no membro **EnableFlags** de uma estrutura de [**\_ \_ Propriedades de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a função [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .

Os consumidores de rastreamento de eventos podem implementar processamento especial para eventos TCP/IP chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**TcpIpGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* . Use os seguintes tipos de evento para identificar o evento de rede (TCP/IP) real ao consumir eventos.



| Tipo de evento                                                            | Descrição                                                                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ de Tipo de rastreamento \_ \_ Accept**(o valor do tipo de evento é 15)<br/>     | Aceite o evento para o protocolo IPv4. A classe [**tcpip \_ TypeGroup2**](tcpip-typegroup2.md) MOF define os dados do evento para esse evento.                                                            |
| **Evento \_ de Tipo de rastreamento \_ \_ Connect**(o valor do tipo de evento é 12)<br/>    | Evento Connect para o protocolo IPv4. A classe [**tcpip \_ TypeGroup2**](tcpip-typegroup2.md) MOF define os dados do evento para esse evento.                                                           |
| **Evento \_ de Tipo de rastreamento \_ \_ Desconectar**(o valor do tipo de evento é 13)<br/> | Evento de desconexão para o protocolo IPv4. A classe [**tcpip \_ TypeGroup1**](tcpip-typegroup1.md) MOF define os dados do evento para esse evento.                                                        |
| **Evento \_ de Tipo de rastreamento \_ \_ Receive**(o valor do tipo de evento é 11)<br/>    | Receber evento para o protocolo IPv4. A classe [**tcpip \_ TypeGroup1**](tcpip-typegroup1.md) MOF define os dados do evento para esse evento.                                                           |
| **Evento \_ de \_Reconectar \_ tipo de rastreamento**(o valor do tipo de evento é 16)<br/>  | Evento de reconexão para o protocolo IPv4. (Uma tentativa de conexão falhou e outra tentativa foi feita.) A classe [**tcpip \_ TypeGroup1**](tcpip-typegroup1.md) MOF define os dados do evento para esse evento. |
| **Evento \_ de \_Retransmissão \_ do tipo de rastreamento**(o valor do tipo de evento é 14)<br/> | Retransmitir evento para o protocolo IPv4. A classe [**tcpip \_ TypeGroup1**](tcpip-typegroup1.md) MOF define os dados do evento para esse evento.                                                        |
| **Evento \_ de Tipo de rastreamento \_ \_ Send**(o valor do tipo de evento é 10)<br/>       | Enviar evento para o protocolo IPv4. A classe [**tcpip \_ SendIPV4**](tcpip-sendipv4.md) MOF define os dados do evento para esse evento.                                                                  |
| Valor do tipo de evento, 17                                                  | Evento Fail. A classe do MOF [**\_ falha de tcpip**](tcpip-fail.md) define os dados do evento para esse evento.                                                                                            |
| Valor do tipo de evento, 18                                                  | Evento de cópia TCP para protocolo IPv4. A classe [**tcpip \_ TypeGroup1**](tcpip-typegroup1.md) MOF define os dados do evento para esse evento.                                                          |
| Valor do tipo de evento, 26                                                  | Enviar evento para o protocolo IPv6. A classe [**tcpip \_ SendIPV6**](tcpip-sendipv6.md) MOF define os dados do evento para esse evento.                                                                  |
| Valor do tipo de evento, 27                                                  | Receber evento para o protocolo IPv6. A classe [**tcpip \_ TypeGroup3**](tcpip-typegroup3.md) MOF define os dados do evento para esse evento.                                                           |
| Valor do tipo de evento, 28                                                  | Evento Connect para protocolo IPv6. A classe [**tcpip \_ TypeGroup4**](tcpip-typegroup4.md) MOF define os dados do evento para esse evento.                                                           |
| Valor do tipo de evento, 29                                                  | Evento de desconexão para o protocolo IPv6. A classe [**tcpip \_ TypeGroup3**](tcpip-typegroup3.md) MOF define os dados do evento para esse evento.                                                        |
| Valor do tipo de evento, 30                                                  | Retransmitir evento para o protocolo IPv6. A classe [**tcpip \_ TypeGroup3**](tcpip-typegroup3.md) MOF define os dados do evento para esse evento.                                                        |
| Valor do tipo de evento, 31                                                  | Aceite o evento para o protocolo IPv6. A classe [**tcpip \_ TypeGroup4**](tcpip-typegroup4.md) MOF define os dados do evento para esse evento.                                                            |
| Valor do tipo de evento, 32                                                  | Evento de reconexão para o protocolo IPv6. (Uma tentativa de conexão falhou e outra tentativa foi feita.) A classe [**tcpip \_ TypeGroup3**](tcpip-typegroup3.md) MOF define os dados do evento para esse evento. |
| Valor do tipo de evento, 34                                                  | Evento de cópia TCP para protocolo IPv6. A classe [**tcpip \_ TypeGroup3**](tcpip-typegroup3.md) MOF define os dados do evento para esse evento.                                                          |



 

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

[**Falha de TcpIp \_**](tcpip-fail.md)
</dt> <dt>

[**\_SendIPV4 tcpip**](tcpip-sendipv4.md)
</dt> <dt>

[**\_SendIPV6 tcpip**](tcpip-sendipv6.md)
</dt> <dt>

[**\_TypeGroup1 tcpip**](tcpip-typegroup1.md)
</dt> <dt>

[**\_TypeGroup2 tcpip**](tcpip-typegroup2.md)
</dt> <dt>

[**\_TypeGroup3 tcpip**](tcpip-typegroup3.md)
</dt> <dt>

[**\_TypeGroup4 tcpip**](tcpip-typegroup4.md)
</dt> <dt>

[**\_V0 tcpip**](tcpip-v0.md)
</dt> <dt>

[**TcpIp \_ v1**](tcpip-v1.md)
</dt> </dl>

 

 

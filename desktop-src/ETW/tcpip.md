---
description: Classe TcpIp – essa classe é a classe pai para eventos TCP/IP. A sintaxe a seguir é simplificada do código MOF.
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
ms.openlocfilehash: 0782db83d5c92a0e39578bc4e0d46e2c1d41432feb418a08bceb2e3548a45b5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069516"
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

A **classe TcpIp** não define nenhum membro.

## <a name="remarks"></a>Comentários

Para habilitar eventos TCP/IP em uma sessão de log do Kernel NT, especifique o sinalizador **\_ \_ \_ \_ TCPIP** DE REDE DO SINALIZADOR DE RASTREAMENTO DE EVENTOS no membro **EnableFlags** de uma estrutura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a [**função StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)

Os consumidores de rastreamento de eventos podem implementar o processamento especial para eventos TCP/IP chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**TcpIpGuid**](nt-kernel-logger-constants.md) como o *parâmetro pGuid.* Use os seguintes tipos de evento para identificar o evento de rede real (TCP/IP) ao consumir eventos.



| Tipo de evento                                                            | Descrição                                                                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENTO \_ TRACE \_ TYPE \_ ACCEPT**(o valor do tipo de evento é 15)<br/>     | Aceitar evento para o protocolo IPv4. A [**classe TcpIp \_ TypeGroup2**](tcpip-typegroup2.md) MOF define os dados de evento para esse evento.                                                            |
| **EVENTO \_ TRACE \_ TYPE \_ CONNECT**(o valor do tipo de evento é 12)<br/>    | Conexão evento para protocolo IPv4. A [**classe TcpIp \_ TypeGroup2**](tcpip-typegroup2.md) MOF define os dados de evento para esse evento.                                                           |
| **EVENTO \_ TRACE \_ TYPE \_ DISCONNECT**(o valor do tipo de evento é 13)<br/> | Desconectar evento para o protocolo IPv4. A [**classe TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) MOF define os dados de evento para esse evento.                                                        |
| **EVENTO \_ TRACE \_ TYPE \_ RECEIVE**(o valor do tipo de evento é 11)<br/>    | Receber evento para o protocolo IPv4. A [**classe TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) MOF define os dados de evento para esse evento.                                                           |
| **EVENTO \_ TRACE \_ TYPE \_ RECONNECT**(o valor do tipo de evento é 16)<br/>  | Reconectar evento para protocolo IPv4. (Falha em uma tentativa de conexão e outra tentativa é feita.) A [**classe TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) MOF define os dados de evento para esse evento. |
| **EVENTO \_ TRACE \_ TYPE \_ RETRANSMIT**(o valor do tipo de evento é 14)<br/> | Retransmitir evento para o protocolo IPv4. A [**classe TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) MOF define os dados de evento para esse evento.                                                        |
| **EVENTO \_ TRACE \_ TYPE \_ SEND**(o valor do tipo de evento é 10)<br/>       | Enviar evento para o protocolo IPv4. A [**classe TcpIp \_ SendIPV4**](tcpip-sendipv4.md) MOF define os dados de evento para esse evento.                                                                  |
| Valor do tipo de evento, 17                                                  | Evento de falha. A [**classe TcpIp \_ Fail**](tcpip-fail.md) MOF define os dados de evento para esse evento.                                                                                            |
| Valor do tipo de evento, 18                                                  | Evento de cópia TCP para protocolo IPv4. A [**classe TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) MOF define os dados de evento para esse evento.                                                          |
| Valor do tipo de evento, 26                                                  | Enviar evento para o protocolo IPv6. A [**classe TcpIp \_ SendIPV6**](tcpip-sendipv6.md) MOF define os dados de evento para esse evento.                                                                  |
| Valor do tipo de evento, 27                                                  | Receber evento para o protocolo IPv6. A [**classe TcpIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF define os dados de evento para esse evento.                                                           |
| Valor do tipo de evento, 28                                                  | Conexão evento para protocolo IPv6. A [**classe TcpIp \_ TypeGroup4**](tcpip-typegroup4.md) MOF define os dados de evento para esse evento.                                                           |
| Valor do tipo de evento, 29                                                  | Desconectar evento para o protocolo IPv6. A [**classe TcpIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF define os dados de evento para esse evento.                                                        |
| Valor do tipo de evento, 30                                                  | Retransmitir evento para o protocolo IPv6. A [**classe TcpIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF define os dados de evento para esse evento.                                                        |
| Valor do tipo de evento, 31                                                  | Aceitar evento para o protocolo IPv6. A [**classe TcpIp \_ TypeGroup4**](tcpip-typegroup4.md) MOF define os dados de evento para esse evento.                                                            |
| Valor do tipo de evento, 32                                                  | Reconectar evento para protocolo IPv6. (Falha em uma tentativa de conexão e outra tentativa é feita.) A [**classe TcpIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF define os dados de evento para esse evento. |
| Valor do tipo de evento, 34                                                  | Evento de cópia TCP para protocolo IPv6. A [**classe TcpIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF define os dados de evento para esse evento.                                                          |



 

Você pode rastrear eventos de rede para um processo de origem e destino usando a **propriedade ProcessId.** Como alguns eventos de rede são registrados por threads separados, talvez você não possa usar os membros **ProcessId** e **ThreadId** do [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) para identificar o processo ou o thread que originou as atividades de rede.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemTrace do MSNT \_**](msnt-systemtrace.md)
</dt> <dt>

[**Falha de \_ TcpIp**](tcpip-fail.md)
</dt> <dt>

[**TcpIp \_ SendIPV4**](tcpip-sendipv4.md)
</dt> <dt>

[**TcpIp \_ SendIPV6**](tcpip-sendipv6.md)
</dt> <dt>

[**TcpIp \_ TypeGroup1**](tcpip-typegroup1.md)
</dt> <dt>

[**TcpIp \_ TypeGroup2**](tcpip-typegroup2.md)
</dt> <dt>

[**TcpIp \_ TypeGroup3**](tcpip-typegroup3.md)
</dt> <dt>

[**TcpIp \_ TypeGroup4**](tcpip-typegroup4.md)
</dt> <dt>

[**TcpIp \_ V0**](tcpip-v0.md)
</dt> <dt>

[**TcpIp \_ V1**](tcpip-v1.md)
</dt> </dl>

 

 

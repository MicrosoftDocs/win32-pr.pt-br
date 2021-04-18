---
title: Enumerações de log de eventos do Windows
description: O log de eventos do Windows define as seguintes enumerações.
ms.assetid: 2dd0e9ef-057b-4d0a-8b21-e7f14e5ae6e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c019a090d1a12e30948e5ed1f5672853caed848c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105760907"
---
# <a name="windows-event-log-enumerations"></a>Enumerações de log de eventos do Windows

O log de eventos do Windows define as seguintes enumerações.



| Enumeração                                                                          | Descrição                                                                                                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**\_tipo de \_ relógio de canal EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_clock_type)                          | Define os valores que especificam o tipo de carimbo de data/hora a ser usado ao registrar em log o canal de eventos.                                         |
| [**\_ID da \_ propriedade de configuração do canal EVT \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_config_property_id)         | Define os identificadores que identificam as propriedades de configuração de um canal.                                                   |
| [**\_tipo de \_ isolamento do canal EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_isolation_type)                  | Define as permissões de acesso padrão a serem aplicadas ao canal.                                                                    |
| [**\_sinalizadores de \_ referência de canal EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_reference_flags)                | Define os valores que especificam como um canal é referenciado.                                                                       |
| [**\_tipo de \_ Sid de canal EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_sid_type)                              | Define os valores que determinam se o evento inclui o identificador de segurança (SID) do principal que registrou o evento. |
| [**\_tipo de canal EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_type)                                       | Define o tipo de um canal.                                                                                                     |
| [**\_ID da \_ propriedade de metadados do evento EVT \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_event_metadata_property_id)         | Define os identificadores que identificam as propriedades de metadados de uma definição de evento.                                              |
| [**\_ID da \_ propriedade de evento EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_event_property_id)               | Define os valores que determinam as informações de consulta a serem recuperadas.                                                               |
| [**\_sinalizadores de EXPORTLOG de EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_exportlog_flags)                                 | Define valores que indicam se os eventos são provenientes de um canal ou arquivo de log.                                                   |
| [**\_sinalizadores de \_ mensagem de formato EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_format_message_flags)                      | Define os valores que especificam a cadeia de caracteres de mensagem do evento a ser formatado.                                                       |
| [**\_ID da \_ propriedade de log EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_log_property_id)                                | Define os identificadores que identificam as propriedades de metadados do arquivo de log de um canal ou arquivo de log.                                   |
| [**\_classe de logon EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_login_class)                                         | Define os tipos de métodos de conexão que você pode usar para se conectar ao computador remoto.                                             |
| [**EVT \_ abrir \_ sinalizadores de log \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_open_log_flags)                                  | Define os valores que especificam se um canal ou um arquivo de log exportado deve ser aberto.                                                    |
| [**\_ID de \_ propriedade de metadados do editor EVT \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_publisher_metadata_property_id) | Define os identificadores que identificam as propriedades de metadados de um provedor.                                                       |
| [**\_sinalizadores de consulta EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags)                                         | Define os valores que especificam como retornar os resultados da consulta e se você está consultando em um canal ou arquivo de log.           |
| [**\_ID da \_ propriedade de consulta EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_property_id)                            | Define os identificadores que identificam as informações de consulta que você pode recuperar.                                                 |
| [**EVT \_ de \_ processar \_ sinalizadores de contexto**](/windows/desktop/api/WinEvt/ne-winevt-evt_render_context_flags)                      | Define os valores que especificam o tipo de informações a serem acessadas a partir do evento.                                                  |
| [**\_sinalizadores de RENDERIZAÇÃO EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_render_flags)                                       | Define os valores que especificam o que renderizar.                                                                                    |
| [**\_sinalizadores de \_ logon de RPC EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_rpc_login_flags)                                | Define os tipos de autenticação que você pode usar para autenticar o usuário ao se conectar a um computador remoto.                |
| [**\_sinalizadores de busca de EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_seek_flags)                                           | Define a posição relativa no conjunto de resultados a partir do qual procurar.                                                                |
| [**\_sinalizadores de assinatura EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_subscribe_flags)                                 | Define os valores possíveis que especificam quando iniciar a assinatura de eventos.                                                      |
| [**\_ação de \_ notificação de assinatura EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_subscribe_notify_action)                | Define os possíveis tipos de dados que o serviço de assinatura pode entregar ao seu retorno de chamada.                                     |
| [**\_ID da \_ Propriedade do sistema EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_system_property_id)                          | Define os identificadores que identificam as propriedades definidas pelo sistema de um evento.                                                   |
| [**\_tipo de variante EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_variant_type)                                       | Define os tipos de dados possíveis de um item de dados variante.                                                                            |



 

 

 





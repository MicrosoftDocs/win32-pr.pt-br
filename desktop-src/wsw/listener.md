---
title: Ouvinte
description: Um ouvinte é usado pelo cliente para aceitar um canal de entrada de um serviço.
ms.assetid: fffda587-23f5-4c7a-93c5-f03d9d3fafb2
keywords:
- Serviços Web de ouvinte para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e372f3fa9109647e009f0258c059cc4c2065f6bc
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104368947"
---
# <a name="listener"></a>Ouvinte

Um ouvinte é usado pelo cliente para aceitar um [canal](channel.md) de entrada de um serviço.

Para criar um ouvinte, você especifica o tipo de canal como um valor de enumeração de [**\_ \_ tipo de canal do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) , as informações de [Associação](binding.md) e a [URL](url.md) a ser escutada.


Para iniciar a escuta na URL, chame a função [**WsOpenListener**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener) .

Para aceitar comunicações de entrada, chame [**WsAcceptChannel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel).

Para cancelar a e/s pendente para um ouvinte, chame [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener).

Para obter informações sobre as transições de estado para um ouvinte, consulte a enumeração de [**\_ \_ estado do WS Listener**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) .

As seguintes chamadas de retorno fazem parte do ouvinte:

-   [**\_retorno de \_ chamada de ouvinte WS Abort \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [**\_retorno de \_ chamada do canal WS Accept \_**](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [**\_retorno de \_ chamada de ouvinte WS Close \_**](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [**WS- \_ criar \_ canal \_ para \_ retorno de chamada do ouvinte \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [**\_retorno de \_ chamada de ouvinte WS Create \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [**\_retorno de \_ chamada do ouvinte gratuito WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [**\_retorno de \_ \_ chamada de propriedade WS Get Listener \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [**retorno de chamada do WS \_ Open \_ Listener \_**](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [**\_retorno de \_ chamada do ouvinte WS Reset \_**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [**\_retorno de \_ \_ chamada da propriedade WS Set Listener \_**](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)

As seguintes enumerações fazem parte do ouvinte:

-   [**versão do WS \_ IP \_**](/windows/desktop/api/WebServices/ne-webservices-ws_ip_version)
-   [**\_ID da \_ Propriedade WS Listener \_**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id)
-   [**Estado do WS \_ Listener \_**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state)

As funções a seguir fazem parte do ouvinte:

-   [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)
-   [**WsAcceptChannel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel)
-   [**WsCloseListener**](/windows/desktop/api/WebServices/nf-webservices-wscloselistener)
-   [**WsCreateListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener)
-   [**WsFreeListener**](/windows/desktop/api/WebServices/nf-webservices-wsfreelistener)
-   [**WsGetListenerProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetlistenerproperty)
-   [**WsOpenListener**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener)
-   [**WsResetListener**](/windows/desktop/api/WebServices/nf-webservices-wsresetlistener)
-   [**WsSetListenerProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetlistenerproperty)

O identificador a seguir faz parte do ouvinte:

-   [\_ouvinte WS](ws-listener.md)

As seguintes estruturas fazem parte do ouvinte:

-   [**\_ \_ retornos de chamada de ouvinte personalizado WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_listener_callbacks)
-   [**\_SUBcadeias de \_ agente do usuário não permitidas do WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_disallowed_user_agent_substrings)
-   [**\_nomes de host do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_host_names)
-   [**\_Propriedades do ouvinte WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_listener_properties)
-   [**\_Propriedade WS Listener \_**](/windows/desktop/api/WebServices/ns-webservices-ws_listener_property)

 

 





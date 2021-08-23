---
title: Ouvinte
description: Um ouvinte é usado pelo cliente para aceitar um canal de entrada de um serviço.
ms.assetid: fffda587-23f5-4c7a-93c5-f03d9d3fafb2
keywords:
- Serviços Web do ouvinte para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26a2f9951dedefd5fb686de7935a76ce3b6ef24dcea140d5414b713e89ad1f1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026374"
---
# <a name="listener"></a>Ouvinte

Um ouvinte é usado pelo cliente para aceitar um canal [de entrada](channel.md) de um serviço.

Para criar um listner, especifique o tipo de canal [](binding.md) como um valor de enumeração [**WS \_ CHANNEL \_ TYPE,**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) as informações de associação e a [URL](url.md) na qual escutar.


Para começar a escutar na URL, chame a [**função WsOpenListener.**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener)

Para aceitar comunicações de entrada, [**chame WsAcceptChannel.**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel)

Para cancelar a E/S pendente de um ouvinte, [**chame WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener).

Para obter informações sobre as transições de estado de um ouvinte, consulte a [**enumeração \_ WS LISTENER \_ STATE.**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state)

Os retornos de chamada a seguir fazem parte do ouvinte:

-   [**WS \_ ABORT \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [**WS \_ ACCEPT \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [**RETORNO DE \_ CHAMADA DO OUVINTE DE FECHAMENTO \_ \_ DO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [**WS \_ CREATE \_ CHANNEL \_ FOR \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [**WS \_ CREATE \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [**RETORNO DE \_ CHAMADA DE OUVINTE LIVRE \_ \_ do WS**](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [**WS \_ GET \_ LISTENER \_ PROPERTY \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [**WS \_ OPEN \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [**RETORNO DE \_ CHAMADA DO OUVINTE DE \_ \_ REDEFINIÇÃO DE WS**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [**RETORNO DE CHAMADA \_ DA PROPRIEDADE DE OUVINTE SET \_ \_ \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)

As enumerações a seguir fazem parte do ouvinte:

-   [**VERSÃO DE \_ IP do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_ip_version)
-   [**ID DA \_ PROPRIEDADE DO OUVINTE DO \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id)
-   [**ESTADO DO \_ OUVINTE \_ DO WS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state)

As seguintes funções fazem parte do ouvinte:

-   [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)
-   [**WsAcceptChannel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel)
-   [**WsCloseListener**](/windows/desktop/api/WebServices/nf-webservices-wscloselistener)
-   [**WsCreateListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener)
-   [**WsFreeListener**](/windows/desktop/api/WebServices/nf-webservices-wsfreelistener)
-   [**WsGetListenerProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetlistenerproperty)
-   [**WsOpenListener**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener)
-   [**WsResetListener**](/windows/desktop/api/WebServices/nf-webservices-wsresetlistener)
-   [**WsSetListenerProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetlistenerproperty)

O seguinte handle faz parte do ouvinte:

-   [OUVINTE do \_ WS](ws-listener.md)

As seguintes estruturas fazem parte do ouvinte:

-   [**RETORNOS DE \_ CHAMADA DE OUVINTE PERSONALIZADO DO \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_listener_callbacks)
-   [**SUBSTRINGS DO \_ AGENTE DO USUÁRIO NÃO \_ \_ \_ PERMITIDOS DO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_disallowed_user_agent_substrings)
-   [**NOMES DE HOST DO WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_host_names)
-   [**PROPRIEDADES \_ DO OUVINTE DO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_listener_properties)
-   [**PROPRIEDADE \_ LISTENER \_ DO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_listener_property)

 

 





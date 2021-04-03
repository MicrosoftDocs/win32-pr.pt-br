---
title: Funções de retorno de chamada do Windows Web Services
description: Os retornos de chamada permitem que um aplicativo chame uma função definida em outra camada ou nível.
ms.assetid: 7398ec42-388a-494c-9fe4-5bd62aa009cb
keywords:
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a385ca21d00e8845f89bda0d9b04221a922ba421
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084033"
---
# <a name="windows-web-services-callback-functions"></a>Funções de retorno de chamada do Windows Web Services

Os retornos de chamada permitem que um aplicativo chame uma função definida em outra camada ou nível. O aplicativo registra o argumento da função como um manipulador que deve ser chamado de forma assíncrona em um momento posterior, conforme necessário. O retorno de chamada será invocado se a função for concluída de forma assíncrona indicando êxito ou erro da função. O retorno de chamada não será chamado se a operação for concluída de forma síncrona.

A API dos serviços Web do Windows inclui as seguintes funções de retorno de chamada:

-   [**\_retorno de \_ chamada de mensagem WS ABANDON \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abandon_message_callback)
-   [**\_retorno de \_ chamada de canal WS Abort \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_channel_callback)
-   [**\_retorno de \_ chamada de ouvinte WS Abort \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [**\_retorno de \_ chamada do canal WS Accept \_**](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [**\_retorno de \_ chamada WS Async**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
-   [**\_função WS Async \_**](/windows/desktop/api/WebServices/nc-webservices-ws_async_function)
-   [**\_retorno de \_ chamada de \_ notificação da lista de emissores do \_ WS CERT \_**](/windows/desktop/api/WebServices/nc-webservices-ws_cert_issuer_list_notification_callback)
-   [**\_retorno de \_ chamada de validação de certificado WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_certificate_validation_callback)
-   [**\_retorno de \_ chamada de canal WS Close \_**](/windows/desktop/api/WebServices/nc-webservices-ws_close_channel_callback)
-   [**\_retorno de \_ chamada de ouvinte WS Close \_**](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [**\_retorno de \_ chamada de canal WS Create \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_callback)
-   [**WS- \_ criar \_ canal \_ para \_ retorno de chamada do ouvinte \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [**\_retorno de chamada WS Create \_ Decoder \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_decoder_callback)
-   [**retorno de chamada do WS \_ Create \_ Encoder \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_encoder_callback)
-   [**\_retorno de \_ chamada de ouvinte WS Create \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [**\_retorno de \_ chamada de decodificação WS Decoder \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_decode_callback)
-   [**\_retorno de \_ chamada de término do WS Decoder \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_end_callback)
-   [**\_retorno de \_ \_ chamada de tipo de conteúdo de Get do \_ WS Decoder \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_get_content_type_callback)
-   [**\_retorno de \_ chamada de início do WS Decoder \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_start_callback)
-   [**\_retorno de \_ chamada de comparação de duração WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_duration_comparison_callback)
-   [**\_retorno de \_ chamada de cadeia de caracteres dinâmica WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [**\_retorno de \_ chamada de codificação do CODIFICAdor WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_encode_callback)
-   [**\_retorno de \_ chamada de término do CODIFICAdor WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_end_callback)
-   [**\_retorno de \_ \_ chamada de \_ tipo de conteúdo \_ do WS Encoder**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_get_content_type_callback)
-   [**\_retorno de \_ chamada de início do CODIFICAdor WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_start_callback)
-   [**\_retorno de \_ chamada de canal livre do WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_channel_callback)
-   [**\_retorno de \_ chamada de decodificador gratuito WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_decoder_callback)
-   [**\_retorno de \_ chamada do codificador gratuito WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_encoder_callback)
-   [**\_retorno de \_ chamada do ouvinte gratuito WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [**\_retorno de chamada WS get \_ CERT \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)
-   [**\_retorno de \_ \_ chamada de propriedade WS Get Channel \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_channel_property_callback)
-   [**\_retorno de \_ \_ chamada de propriedade WS Get Listener \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [**\_retorno de \_ chamada de redirecionamento http WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_http_redirect_callback)
-   [**WS \_ é \_ \_ retorno de chamada de valor padrão \_**](/windows/desktop/api/WebServices/nc-webservices-ws_is_default_value_callback)
-   [**retorno de chamada do WS \_ Message \_ concluído \_**](/windows/desktop/api/WebServices/nc-webservices-ws_message_done_callback)
-   [**retorno de chamada do WS \_ Open \_ Channel \_**](/windows/desktop/api/WebServices/nc-webservices-ws_open_channel_callback)
-   [**retorno de chamada do WS \_ Open \_ Listener \_**](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [**\_retorno de \_ chamada Cancelar operação \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)
-   [**\_retorno de \_ \_ chamada de estado livre de operação WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback)
-   [**\_retorno de \_ chamada de mensagem de proxy WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback)
-   [**\_retorno de \_ chamada de bytes WS pull \_**](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [**\_retorno de \_ chamada de bytes do WS Push \_**](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [**\_retorno de \_ chamada WS Read**](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)
-   [**retorno de chamada do WS \_ Read \_ Message \_ end \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_end_callback)
-   [**\_retorno de \_ chamada de início de mensagem de leitura WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_start_callback)
-   [**\_retorno de \_ chamada do tipo leitura WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback)
-   [**\_retorno de \_ chamada do canal WS Reset \_**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_channel_callback)
-   [**\_retorno de \_ chamada do ouvinte WS Reset \_**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [**\_retorno de \_ chamada de canal de aceitação de serviço WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback)
-   [**\_retorno de \_ chamada de canal de fechamento de serviço WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)
-   [**\_retorno de \_ chamada de recebimento de mensagem de serviço WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)
-   [**\_retorno de \_ chamada de segurança do serviço WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback)
-   [**\_retorno de \_ chamada de stub de serviço WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_stub_callback)
-   [**\_retorno de \_ chamada de Propriedade do canal \_ \_ do WS Set**](/windows/desktop/api/WebServices/nc-webservices-ws_set_channel_property_callback)
-   [**\_retorno de \_ \_ chamada da propriedade WS Set Listener \_**](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)
-   [**\_retorno de \_ chamada de canal de sessão \_ \_ do WS-Shutdown**](/windows/desktop/api/WebServices/nc-webservices-ws_shutdown_session_channel_callback)
-   [**\_retorno de \_ chamada de senha do WS Validate \_**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback)
-   [**\_retorno de \_ \_ chamada SAML do WS Validate**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)
-   [**\_retorno de \_ chamada WS Write**](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)
-   [**\_retorno de \_ chamada de end de mensagem de gravação WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_end_callback)
-   [**\_retorno de \_ chamada de início de mensagem de gravação WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_start_callback)
-   [**\_retorno de \_ chamada de tipo de gravação WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback)

 

 





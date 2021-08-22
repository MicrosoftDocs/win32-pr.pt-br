---
title: Windows Funções de retorno de chamada dos Serviços Web
description: Os retornos de chamada permitem que um aplicativo chame uma função definida em outra camada ou nível.
ms.assetid: 7398ec42-388a-494c-9fe4-5bd62aa009cb
keywords:
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a78bce5c4023d889748af103148088462cb4b267192b1c0b3845fc735fd1bb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926866"
---
# <a name="windows-web-services-callback-functions"></a>Windows Funções de retorno de chamada dos Serviços Web

Os retornos de chamada permitem que um aplicativo chame uma função definida em outra camada ou nível. O aplicativo registra o argumento de função como um manipulador que deve ser chamado de forma assíncrona em um momento posterior, conforme necessário. O retorno de chamada será invocado se a função for concluída de forma assíncrona, indicando êxito ou erro da função. O retorno de chamada não será chamado se a operação for concluída de forma síncrona.

A Windows API de Serviços Web inclui as seguintes funções de retorno de chamada:

-   [**WS \_ ABANDON \_ MESSAGE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_abandon_message_callback)
-   [**WS \_ ABORT \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_channel_callback)
-   [**WS \_ ABORT \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [**WS \_ ACCEPT \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [**RETORNO DE \_ CHAMADA \_ ASSÍNCRONO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
-   [**FUNÇÃO \_ ASSÍNCRONA \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_async_function)
-   [**WS \_ CERT \_ ISSUER \_ LIST \_ NOTIFICATION \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_cert_issuer_list_notification_callback)
-   [**RETORNO DE CHAMADA DE \_ \_ VALIDAÇÃO \_ DE CERTIFICADO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_certificate_validation_callback)
-   [**WS \_ CLOSE \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_close_channel_callback)
-   [**RETORNO DE \_ CHAMADA DO OUVINTE DE FECHAMENTO \_ \_ DO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [**WS \_ CREATE \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_callback)
-   [**WS \_ CREATE \_ CHANNEL \_ FOR \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [**WS \_ CREATE \_ DECODER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_decoder_callback)
-   [**WS \_ CREATE \_ ENCODER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_encoder_callback)
-   [**WS \_ CREATE \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [**RETORNO DE CHAMADA \_ DE DECODIFICADOR \_ \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_decode_callback)
-   [**RETORNO DE CHAMADA FINAL \_ DO \_ DECODIFICADOR \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_end_callback)
-   [**WS \_ DECODER \_ GET \_ CONTENT \_ TYPE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_get_content_type_callback)
-   [**RETORNO DE CHAMADA INICIAL \_ DO DECODIFICADOR \_ \_ DO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_start_callback)
-   [**RETORNO DE CHAMADA \_ DE \_ COMPARAÇÃO DE DURAÇÃO DO \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_duration_comparison_callback)
-   [**RETORNO DE CHAMADA \_ DE CADEIA DE \_ \_ CARACTERES DINÂMICA DO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [**RETORNO DE CHAMADA \_ DE \_ CODIFICAÇÃO \_ DO CODIFICADOR WS**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_encode_callback)
-   [**RETORNO DE CHAMADA \_ FINAL DO \_ \_ CODIFICADOR WS**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_end_callback)
-   [**RETORNO DE CHAMADA DO TIPO DE CONTEÚDO \_ \_ GET \_ \_ DO \_ CODIFICADOR WS**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_get_content_type_callback)
-   [**RETORNO DE CHAMADA \_ INICIAL DO \_ \_ CODIFICADOR WS**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_start_callback)
-   [**RETORNO DE \_ CHAMADA DE CANAL LIVRE \_ \_ do WS**](/windows/desktop/api/WebServices/nc-webservices-ws_free_channel_callback)
-   [**WS \_ FREE \_ DECODER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_free_decoder_callback)
-   [**RETORNO DE \_ CHAMADA \_ DO CODIFICADOR LIVRE \_ DO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_free_encoder_callback)
-   [**RETORNO DE \_ CHAMADA DE OUVINTE LIVRE \_ \_ do WS**](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [**WS \_ GET \_ CERT \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)
-   [**WS \_ GET \_ CHANNEL \_ PROPERTY \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_get_channel_property_callback)
-   [**WS \_ GET \_ LISTENER \_ PROPERTY \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [**RETORNO DE \_ CHAMADA DE REDIRECIONAMENTO HTTP \_ \_ DO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_http_redirect_callback)
-   [**WS \_ É RETORNO DE CHAMADA DE VALOR \_ \_ \_ PADRÃO**](/windows/desktop/api/WebServices/nc-webservices-ws_is_default_value_callback)
-   [**RETORNO DE \_ CHAMADA FEITO DA MENSAGEM \_ \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_message_done_callback)
-   [**WS \_ OPEN \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_open_channel_callback)
-   [**WS \_ OPEN \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [**WS \_ OPERATION \_ CANCEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)
-   [**RETORNO DE CHAMADA DE ESTADO LIVRE DA OPERAÇÃO \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback)
-   [**RETORNO DE \_ CHAMADA DE MENSAGEM PROXY \_ \_ DO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback)
-   [**RETORNO DE \_ CHAMADA DE BYTES DE PULL \_ \_ DO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [**WS \_ PUSH \_ BYTES \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [**WS \_ READ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)
-   [**WS \_ READ \_ MESSAGE \_ END \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_end_callback)
-   [**WS \_ READ \_ MESSAGE \_ START \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_start_callback)
-   [**WS \_ READ \_ TYPE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback)
-   [**RETORNO DE \_ CHAMADA DO CANAL DE \_ \_ REDEFINIÇÃO DO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_channel_callback)
-   [**RETORNO DE \_ CHAMADA DO OUVINTE DE \_ \_ REDEFINIÇÃO DE WS**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [**RETORNO DE CHAMADA DE CANAL \_ \_ DE ACEITAÇÃO \_ \_ DO SERVIÇO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback)
-   [**RETORNO DE CHAMADA DE CANAL FECHADO \_ \_ \_ \_ DO SERVIÇO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)
-   [**RETORNO DE CHAMADA \_ DE RECEBIMENTO DE MENSAGEM \_ \_ \_ DO SERVIÇO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)
-   [**RETORNO DE CHAMADA \_ DE SEGURANÇA DO SERVIÇO \_ \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback)
-   [**RETORNO DE \_ CHAMADA \_ STUB \_ DO SERVIÇO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_stub_callback)
-   [**WS \_ SET \_ CHANNEL \_ PROPERTY \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_set_channel_property_callback)
-   [**RETORNO DE CHAMADA \_ DA PROPRIEDADE DE OUVINTE SET \_ \_ \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)
-   [**RETORNO DE CHAMADA DO CANAL DE SESSÃO DE DESLIGAMENTO \_ \_ \_ \_ DO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_shutdown_session_channel_callback)
-   [**WS \_ VALIDATE \_ PASSWORD \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback)
-   [**WS \_ VALIDATE \_ SAML \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)
-   [**WS \_ WRITE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)
-   [**WS \_ WRITE \_ MESSAGE \_ END \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_end_callback)
-   [**WS \_ WRITE \_ MESSAGE \_ START \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_start_callback)
-   [**WS \_ WRITE \_ TYPE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback)

 

 





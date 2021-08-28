---
title: canal (Windows serviços Web)
description: Os canais encapsulam um contexto de comunicação entre duas ou mais partes e são usados para enviar e receber mensagens.
ms.assetid: 5a04580d-c89f-4505-a4b7-0724ffb788fd
keywords:
- Serviços Web do canal para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ff11601f372416527f1d521f8fb9880c98821f9421b633f9eed059cc5b4f672
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026644"
---
# <a name="channel-windows-web-services"></a>canal (Windows serviços Web)

Os canais encapsulam um contexto de comunicação entre duas ou mais partes e são usados para enviar e receber mensagens.


No cliente, use [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) para criar um canal. No servidor, use [**WsCreateChannelForListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannelforlistener) para criar um canal que pode ser aceito pelo cliente usando um [ouvinte](listener.md).

Ao criar um canal, você especifica as informações a seguir, que determinam o comportamento local do canal e o protocolo de conexão a ser usado.

-   Um [**\_ \_ tipo de canal do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type), que identifica o padrão de troca de mensagens do canal.
-   Uma [**\_ \_ associação do WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), que identifica o protocolo de transferência a ser usado.
-   Uma [**\_ \_ Descrição do WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), que especifica a segurança usada para o canal. Ao criar canais para uso em um servidor, isso é especificado uma vez para todos os canais que serão aceitos para um determinado ouvinte.
-   Um conjunto [**de \_ \_ Propriedades do WS Channel**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property), que especificam configurações opcionais adicionais (para obter uma lista dessas configurações, consulte Enumerações de [**ID de Propriedade do WS \_ \_ \_ Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) ).

Antes de usar o canal, você deve abri-lo chamando a função [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) e especificando o canal e o [endereço do ponto de extremidade](endpoint-address.md), juntamente com outras informações opcionais.

Para obter informações sobre as transições de estado para um canal, consulte o tópico [**Estados de canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) .

Para obter mais informações sobre canais, consulte o tópico [visão geral da camada de canal](channel-layer-overview.md) .

Os seguintes elementos de API são usados com canais.

| Callback                                                                                  | Descrição                                                                                                                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_retorno de \_ chamada de mensagem WS ABANDON \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abandon_message_callback)                     | Manipula a chamada [**WsAbandonMessage**](/windows/desktop/api/WebServices/nf-webservices-wsabandonmessage) para um canal com associação de canal personalizada.                                              |
| [**\_retorno de \_ chamada de canal WS Abort \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_channel_callback)                         | Manipula a chamada [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) para um canal com associação de canal personalizada.                                                  |
| [**\_retorno de \_ chamada de canal WS Close \_**](/windows/desktop/api/WebServices/nc-webservices-ws_close_channel_callback)                         | Manipula a chamada [**WsCloseChannel**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel) para um canal com associação de canal personalizada.                                                  |
| [**\_retorno de \_ chamada de canal WS Create \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_callback)                       | Manipula a chamada [**WsCloseChannel**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel) para um canal com associação de canal personalizada.                                                  |
| [**\_retorno de chamada WS Create \_ Decoder \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_decoder_callback)                       | Manipula a criação de uma instância de decodificador.                                                                                                                  |
| [**retorno de chamada do WS \_ Create \_ Encoder \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_encoder_callback)                       | Manipula a criação de uma instância de codificador.                                                                                                                 |
| [**\_retorno de \_ chamada de decodificação WS Decoder \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_decode_callback)                       | Decodifica uma mensagem.                                                                                                                                    |
| [**\_retorno de \_ chamada de término do WS Decoder \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_end_callback)                             | Decodifica o final de uma mensagem.                                                                                                                         |
| [**\_retorno de \_ \_ chamada de tipo de conteúdo de Get do \_ WS Decoder \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_get_content_type_callback) | Obtém o tipo de conteúdo da mensagem.                                                                                                                 |
| [**\_retorno de \_ chamada de início do WS Decoder \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_start_callback)                         | Inicia a decodificação de uma mensagem.                                                                                                                            |
| [**\_retorno de \_ chamada de codificação do CODIFICAdor WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_encode_callback)                       | Codifica uma mensagem.                                                                                                                                    |
| [**\_retorno de \_ chamada de término do CODIFICAdor WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_end_callback)                             | Codifica o fim de uma mensagem.                                                                                                                         |
| [**\_retorno de \_ \_ chamada de \_ tipo de conteúdo \_ do WS Encoder**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_get_content_type_callback) | Obtém o tipo de conteúdo da mensagem.                                                                                                                 |
| [**\_retorno de \_ chamada de início do CODIFICAdor WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_start_callback)                         | Inicia a codificação de uma mensagem.                                                                                                                            |
| [**\_retorno de \_ chamada de canal livre do WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_channel_callback)                           | Manipula a chamada [**WsFreeChannel**](/windows/desktop/api/WebServices/nf-webservices-wsfreechannel) para um canal com associação de canal personalizada.                                                    |
| [**\_retorno de \_ chamada de decodificador gratuito WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_decoder_callback)                           | Manipula a liberação de uma instância de decodificador.                                                                                                                   |
| [**\_retorno de \_ chamada do codificador gratuito WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_encoder_callback)                           | Lida com a liberação de uma instância do codificador.                                                                                                                  |
| [**\_retorno de \_ \_ chamada de propriedade WS Get Channel \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_channel_property_callback)          | Manipula a chamada [**WsGetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetchannelproperty) para um canal com associação de canal personalizada.                                      |
| [**\_retorno de \_ chamada de redirecionamento http WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_http_redirect_callback)                         | Chamado quando uma mensagem está prestes a ser redirecionada automaticamente para outro serviço utilizando a funcionalidade de redirecionamento automático de HTTP, conforme descrito em RFC2616. |
| [**retorno de chamada do WS \_ Open \_ Channel \_**](/windows/desktop/api/WebServices/nc-webservices-ws_open_channel_callback)                           | Manipula a chamada [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) para um canal com associação de canal personalizada.                                                    |
| [**retorno de chamada do WS \_ Read \_ Message \_ end \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_end_callback)                  | Manipula a chamada [**WsReadMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend) para um canal com associação de canal personalizada.                                              |
| [**\_retorno de \_ chamada de início de mensagem de leitura WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_start_callback)              | Manipula a chamada [**WsReadMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend) para um canal com associação de canal personalizada.                                              |
| [**\_retorno de \_ chamada do canal WS Reset \_**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_channel_callback)                         | Manipula a chamada [**WsResetChannel**](/windows/desktop/api/WebServices/nf-webservices-wsresetchannel) para um canal com associação de canal personalizada.                                                  |
| [**\_retorno de \_ chamada de Propriedade do canal \_ \_ do WS Set**](/windows/desktop/api/WebServices/nc-webservices-ws_set_channel_property_callback)          | Manipula a chamada [**WsSetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetchannelproperty) para um canal com associação de canal personalizada.                                      |
| [**\_retorno de \_ chamada de canal de sessão \_ \_ do WS-Shutdown**](/windows/desktop/api/WebServices/nc-webservices-ws_shutdown_session_channel_callback)  | Manipula a chamada [**WsShutdownSessionChannel**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel) para um canal com associação de canal personalizada.                              |
| [**\_retorno de \_ chamada de end de mensagem de gravação WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_end_callback)                | Manipula a chamada [**WsWriteMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wswritemessageend) para um canal com associação de canal personalizada.                                            |
| [**\_retorno de \_ chamada de início de mensagem de gravação WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_start_callback)            | Manipula a chamada [**WsWriteMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wswritemessagestart) para um canal com associação de canal personalizada.                                        |



 



| Enumeração                                                 | Descrição                                                                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Associação de WS \_ Channel \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)          | Indica a pilha de protocolos a ser usada para o canal.                                                                                      |
| [**ID de Propriedade do WS \_ Channel \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) | Identifica cada propriedade de canal por uma ID.                                                                                                |
| [**Estado do WS \_ Channel \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state)              | O estado do canal.                                                                                                                 |
| [**\_tipo de canal do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)                | Indica as características básicas do canal, como se ele é sessão e as direções de comunicação com suporte. |
| [**\_codificação WS**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding)                         | As codificações diferentes (formatos de mensagem).                                                                                                |
| [**\_opção WS Receive \_**](/windows/desktop/api/WebServices/ne-webservices-ws_receive_option)            | Especifica se uma mensagem é necessária ao receber de um canal.                                                                    |
| [**\_modo de transferência WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_transfer_mode)              | Especifica se as mensagens enviadas ou recebidas são transmitidas ou armazenadas em buffer.                                                            |



 



| Função                                                         | Descrição                                                                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**WsAbandonMessage**](/windows/desktop/api/WebServices/nf-webservices-wsabandonmessage)                     | Ignora o restante de uma mensagem para um canal.                                                              |
| [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)                         | Anula todas as e/s pendentes em um canal especificado e define o estado do canal para o **estado do WS \_ Channel com \_ \_ falha**. |
| [**WsCloseChannel**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel)                         | Fecha um canal quando ele não é mais necessário.                                                                |
| [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel)                       | Cria um canal.                                                                                           |
| [**WsCreateChannelForListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannelforlistener) | Cria um canal para um ouvinte.                                                                            |
| [**WsFreeChannel**](/windows/desktop/api/WebServices/nf-webservices-wsfreechannel)                           | Libera os recursos de memória associados a um canal.                                                     |
| [**WsGetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetchannelproperty)             | Recupera uma propriedade do canal referenciado pelo parâmetro Channel.                                     |
| [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel)                           | Abre um canal para um ponto de extremidade.                                                                              |
| [**WsReadMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend)                     | Lê os elementos de fechamento de uma mensagem de um canal.                                                      |
| [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart)                 | Lê os cabeçalhos da próxima mensagem do canal e se prepara para ler os elementos do corpo.               |
| [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage)                     | Recebe uma mensagem e desserializa o corpo da mensagem como um valor.                                      |
| [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply)                         | Envia uma mensagem de solicitação e recebe uma mensagem de resposta correlacionada.                                             |
| [**WsResetChannel**](/windows/desktop/api/WebServices/nf-webservices-wsresetchannel)                         | Redefina um canal para que ele possa ser reutilizado.                                                                         |
| [**WsSendMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage)                           | Envia uma mensagem em um canal usando a serialização para gravar o elemento body.                                  |
| [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage)                 | Envia uma mensagem que é uma resposta a uma mensagem recebida.                                                       |
| [**WsSetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetchannelproperty)             | Define uma propriedade de um canal.                                                                                |
| [**WsSetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetmessageproperty)             | Define uma propriedade de uma mensagem.                                                                                |
| [**WsWriteMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wswritemessageend)                   | Grava os elementos de fechamento de uma mensagem no canal.                                                     |
| [**WsWriteMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wswritemessagestart)               | Anote os cabeçalhos de uma mensagem no canal e prepare-se para gravar os elementos do corpo.                   |



 



| Handle                        | Descrição                                 |
|-------------------------------|---------------------------------------------|
| [WS \_ Channel](ws-channel.md) | Um tipo opaco usado para fazer referência a um canal. |



 



| Estrutura                                                                          | Descrição                                                                                                                                                                                      |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**decodificador do WS \_ Channel \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_decoder)                                 | Um conjunto de retornos de chamada que transforma o tipo de conteúdo e os bytes codificados de uma mensagem recebida.                                                                                                      |
| [**\_codificador do WS Channel \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_encoder)                                 | Um conjunto de retornos de chamada que podem transformar o tipo de conteúdo e os bytes codificados de uma mensagem enviada.                                                                                                      |
| [**\_Propriedades do canal WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_properties)                           | Um conjunto de estruturas de [**\_ \_ Propriedade do canal WS**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) .                                                                                                                        |
| [**\_Propriedade WS Channel \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)                               | Uma configuração específica do canal.                                                                                                                                                                      |
| [**\_ \_ retornos de chamada de canal personalizado WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_channel_callbacks)              | Um conjunto de retornos de chamada que formam a implementação de um canal personalizado.                                                                                                                             |
| [**\_ \_ proxy HTTP personalizado \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_http_proxy)                            | usado para especificar o proxy personalizado para o canal, usando o valor de proxy **\_ \_ \_ \_ http personalizado da propriedade WS Channel** \_ da enumeração de [**\_ \_ \_ ID de Propriedade do WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) . |
| [**\_mapeamento de \_ cabeçalho \_ http do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_mapping)                        | Representa um cabeçalho individual que é mapeado como parte do [**\_ mapeamento de \_ mensagem \_ http do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping).                                                                         |
| [**\_mapeamento de \_ mensagem \_ http do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping)                      | Informações sobre como uma solicitação HTTP ou resposta devem ser representadas em um objeto Message.                                                                                                     |
| [**\_contexto de \_ retorno de \_ chamada de redirecionamento http WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_redirect_callback_context) | Especifica a função de retorno de chamada e o estado para controlar o comportamento de redirecionamento automático de HTTP.                                                                                               |
| [**\_Descrição da mensagem WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description)                         | O esquema para a [ \_ mensagem WS](ws-message.md) de entrada e saída para uma determinada descrição da operação.                                                                                             |



 

 

 





---
title: Mensagem (Serviços Web do Windows)
description: Uma mensagem é um objeto que encapsula dados transmitidos ou recebidos.
ms.assetid: edc810d9-7d78-4b79-8cbb-e87401f6ae41
keywords:
- Serviços Web de mensagens para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1722cbe4a956ef16a1b7195158b695f551419ad600c64f552e92700d3e4ee57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657087"
---
# <a name="message-windows-web-services"></a>Mensagem (Serviços Web do Windows)

Uma mensagem é um objeto que encapsula dados transmitidos ou recebidos. A estrutura de uma mensagem é definida pelo SOAP e inclui um conjunto de cabeçalhos e um corpo. Os cabeçalhos são sempre armazenados em buffer na memória, mas o corpo é lido e gravado com uma API de streaming.

![Diagrama mostrando uma mensagem com o cabeçalho que está sendo armazenado em buffer e o corpo que está sendo transmitido.](images/messageenvelope.png)


As mensagens têm um conjunto de propriedades que podem ser usadas para especificar configurações opcionais que controlam o comportamento de uma mensagem e para fornecer uma maneira de recuperar informações adicionais sobre mensagens recebidas (como informações de segurança). Consulte [**\_ ID de \_ propriedade \_ da mensagem WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) para obter uma lista completa de propriedades de mensagem.

Uma mensagem é endereçada a um [endereço de ponto de extremidade](endpoint-address.md)específico.

Uma [**\_ falha WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) é um tipo especial de conteúdo de mensagem usado para representar as falhas retornadas de um ponto de extremidade remoto.

As mensagens passam pela codificação que transforma o XML em um formato de conexão linear antes de ser transmitido.

Para obter mais informações sobre mensagens, consulte o tópico [visão geral da camada de canal](channel-layer-overview.md) .

Os exemplos a seguir ilustram o uso de mensagens em WWSAPI.

| Exemplo                                              | Descrição                                  |
|------------------------------------------------------|----------------------------------------------|
| [CustomHeaderExample](customheaderexample.md)       | Ilustra o uso de cabeçalhos de mensagem personalizados.    |
| [MessageEncodingExample](messageencodingexample.md) | Ilustra a codificação e a decodificação de uma mensagem. |
| [ForwardMessageExample](forwardmessageexample.md)   | Ilustra o encaminhamento de uma mensagem.            |



 

Os seguintes elementos de API são usados com mensagens.

| Callback                                                        | Descrição                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**retorno de chamada do WS \_ Message \_ concluído \_**](/windows/desktop/api/WebServices/nc-webservices-ws_message_done_callback) | Notifica o chamador de que a mensagem concluiu seu uso da \_ estrutura de leitor XML do WS \_ que foi fornecida para a função WsReadEnvelopeStart ou da estrutura do \_ gravador XML WS \_ fornecida para a função WsWriteEnvelopeStart. |



 



| Enumeração                                                      | Descrição                                                                                              |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**\_versão de endereçamento do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version)         | A versão da especificação usada para os cabeçalhos de endereçamento.                                        |
| [**\_versão do envelope WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_envelope_version)             | A versão da especificação usada para a estrutura do envelope.                                        |
| [**\_atributos de cabeçalho WS \_**](/windows/win32/api/webservices/ne-webservices-ws_xml_text_type)           | Um conjunto de sinalizadores que representa os atributos mustUnderstand SOAP e retransmissão de um cabeçalho.                    |
| [**\_tipo de cabeçalho WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_header_type)                       | O tipo do cabeçalho.                                                                                  |
| [**\_inicialização de mensagem WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) | Especifica quais cabeçalhos o [**WsInitializeMessage**](/windows/desktop/api/WebServices/nf-webservices-wsinitializemessage) deve adicionar à mensagem. |
| [**\_ID da \_ propriedade da mensagem WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id)      | A ID de cada propriedade de mensagem.                                                                         |
| [**\_estado da mensagem WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_state)                   | O estado da mensagem.                                                                                |



 



| Função                                                             | Descrição                                                                                                                                            |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage)                         | Atribui um endereço de destino a uma mensagem.                                                                                                            |
| [**WsCheckMustUnderstandHeaders**](/windows/desktop/api/WebServices/nf-webservices-wscheckmustunderstandheaders) | Verifica se os cabeçalhos especificados foram adequadamente compreendidos pelo destinatário.                                                                         |
| [**WsCreateMessage**](/windows/desktop/api/WebServices/nf-webservices-wscreatemessage)                           | Cria uma instância de um objeto de [ \_ mensagem do WS](ws-message.md) .                                                                                         |
| [**WsCreateMessageForChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatemessageforchannel)       | Cria uma mensagem que é apropriada para uso com um canal específico.                                                                                 |
| [**WsFillBody**](/windows/desktop/api/WebServices/nf-webservices-wsfillbody)                                     | Garante que haja um número suficiente de bytes disponíveis em uma mensagem para leitura.                                                                |
| [**WsFlushBody**](/windows/desktop/api/WebServices/nf-webservices-wsflushbody)                                   | Libera todos os dados de corpo de mensagem acumulados que foram gravados.                                                                                       |
| [**WsFreeMessage**](/windows/desktop/api/WebServices/nf-webservices-wsfreemessage)                               | Libera o recurso de memória associado a uma mensagem.                                                                                                |
| [**WsGetCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader)                       | Localiza o cabeçalho definido pelo aplicativo da mensagem e o desserializa.                                                                               |
| [**WsGetHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader)                                   | Localiza um cabeçalho padrão específico na mensagem e o desserializa.                                                                                 |
| [**WsGetHeaderAttributes**](/windows/desktop/api/WebServices/nf-webservices-wsgetheaderattributes)               | Popula um parâmetro ULONG com os [**atributos de \_ cabeçalho \_ WS**](/windows/win32/api/webservices/ne-webservices-ws_xml_text_type) do elemento Header no qual o leitor está posicionado. |
| [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty)                 | Recupera uma propriedade de objeto de mensagem especificada.                                                                                                         |
| [**WsInitializeMessage**](/windows/desktop/api/WebServices/nf-webservices-wsinitializemessage)                   | Inicializa os cabeçalhos da mensagem em preparação para o processamento.                                                                                 |
| [**WsMarkHeaderAsUnderstood**](/windows/desktop/api/WebServices/nf-webservices-wsmarkheaderasunderstood)         | Marca um cabeçalho como compreendido pelo aplicativo.                                                                                                       |
| [**WsReadBody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody)                                     | Desserializa um valor do leitor XML da mensagem.                                                                                               |
| [**WsReadEnvelopeEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopeend)                       | Lê os elementos de fechamento de uma mensagem.                                                                                                               |
| [**WsReadEnvelopeStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopestart)                   | Lê os cabeçalhos da mensagem e se prepara para ler os elementos do corpo.                                                                               |
| [**WsRemoveCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsremovecustomheader)                 | Remove um cabeçalho personalizado da mensagem.                                                                                                              |
| [**WsRemoveHeader**](/windows/desktop/api/WebServices/nf-webservices-wsremoveheader)                             | Remove o objeto [**de \_ \_ tipo de cabeçalho WS**](/windows/desktop/api/WebServices/ne-webservices-ws_header_type) padrão de uma mensagem.                                                                 |
| [**WsResetMessage**](/windows/desktop/api/WebServices/nf-webservices-wsresetmessage)                             | Define o estado da mensagem de volta para o **\_ estado da mensagem WS \_ \_ vazio**.                                                                                          |
| [**WsSetHeader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader)                                   | Adiciona ou substitui o cabeçalho padrão especificado na mensagem.                                                                                         |
| [**WsWriteBody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody)                                   | Grava um valor no corpo de uma mensagem.                                                                                                               |
| [**WsWriteEnvelopeEnd**](/windows/desktop/api/WebServices/nf-webservices-wswriteenvelopeend)                     | Grava os elementos de fechamento de uma mensagem.                                                                                                              |
| [**WsWriteEnvelopeStart**](/windows/desktop/api/WebServices/nf-webservices-wswriteenvelopestart)                 | Grava o início da mensagem, incluindo o conjunto atual de cabeçalhos da mensagem e se prepara para gravar os elementos do corpo.                           |



 



| Handle                        | Descrição                                         |
|-------------------------------|-----------------------------------------------------|
| [\_mensagem WS](ws-message.md) | O tipo opaco usado para fazer referência a um objeto de mensagem. |



 



| Estrutura                                                | Descrição                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**WS- \_ falha**](/windows/desktop/api/WebServices/ns-webservices-ws_fault)                            | Um valor de falha no corpo de uma mensagem que indica uma falha de processamento. |
| [**\_código de falha WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code)                 | Representa um código de falha.                                                             |
| [**\_motivo da falha do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason)             | Contém uma explicação da falha.                                                |
| [**\_Propriedades da mensagem WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_properties) | Especifica um conjunto de estruturas de [**\_ \_ propriedade de mensagem WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_property) .  |
| [**\_propriedade de mensagem WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_property)     | Especifica uma configuração específica da mensagem.                                                |



 

 

 





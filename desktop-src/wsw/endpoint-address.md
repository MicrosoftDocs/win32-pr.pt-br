---
title: Endereço de ponto de extremidade
description: Um endereço de ponto de extremidade representa o endereço de um serviço na rede.
ms.assetid: 5df9c0da-6648-42a0-ae87-06844461042a
keywords:
- Endpoint Address Web Services para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb0bffecf49299b73863ddf32d758e4b62ceaa186b876d63e887d69c5b9ef94c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118026250"
---
# <a name="endpoint-address"></a>Endereço de ponto de extremidade

Um endereço de ponto de extremidade representa o endereço de um serviço na rede. Ao abrir um canal [,](channel.md)chamando a função [**WsOpenChannel,**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) você precisa fornecer o endereço do ponto de extremidade do serviço com o qual se comunicar, bem como especificar o canal que deseja abrir.


Um endereço de ponto de extremidade consiste em:

-   uma [URL](url.md)
-   um conjunto de headers (opcional)
-   um conjunto de extensões (opcional)
-   uma identidade [opcional](endpoint-identity.md) que representa a identidade de segurança do serviço.

Quando uma mensagem é endereçada, a URL se torna o título "Para" da mensagem. Todos os headers que fazem parte do endereço do ponto de extremidade também são adicionados à mensagem.

![Diagrama mostrando os headers de endereço do ponto de extremidade sendo adicionados a uma mensagem.](images/endpointaddress.png)

Os canais abordam automaticamente todas as mensagens enviadas, usando a estrutura [**ENDEREÇO \_ DO PONTO \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) DE EXTREMIDADE do WS que foi passada para [**o WsOpenChannel.**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) Você também pode usar a [**função WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) para substituir esse comportamento padrão.

Quando o ENDEREÇO DE PONTO DE EXTREMIDADE do WS é passado como um parâmetro, as funções [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) e [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) criam uma cópia do parâmetro **\_ ENDPOINT \_ ADDRESS** do WS na memória e seu tamanho é limitado por 65536 bytes. [**\_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) não tem essa limitação porque não requer a criação de uma cópia do **parâmetro \_ ENDPOINT \_ ADDRESS do WS.**

As extensões especificadas  no campo de extensões de ENDEREÇO DE PONTO DE EXTREMIDADE [**do WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) não são usadas para endereçamento da mensagem, mas são um mecanismo de extensibilidade que pode ser usado para fornecer informações adicionais (por exemplo, metadados) sobre o serviço. Extensões comuns podem ser lidas com a [**função WsReadEndpointAddressExtension.**](/windows/desktop/api/WebServices/nf-webservices-wsreadendpointaddressextension)

O campo de identidade opcional do endereço do ponto de extremidade pode incluir, por exemplo, o nome DNS do computador no qual o serviço está sendo executado ou o UPN da conta Windows na qual o serviço está sendo executado. O campo de identidade não é usado no endereçamento da mensagem, mas pode ser usado para obter um token de segurança para o serviço (por exemplo, para obter um tíquete Kerberos para o UPN de destino) e para verificar a identidade das respostas do serviço (por exemplo, uma identidade DNS usada para verificações de nome no certificado de serviço retornado durante o SSL).

Os endereços de ponto de extremidade podem ser lidos e gravados usando [a serialização](serialization.md) com o valor de enumeração **WS \_ ENDPOINT \_ ADDRESS \_ TYPE** de [**WS \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type). Observe que, para serializar um endereço de ponto de extremidade, você deve saber a versão da especificação usada para os títulos de endereçamento, conforme especificado na enumeração [**WS \_ ADDRESSING \_ VERSION.**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version)

 

 





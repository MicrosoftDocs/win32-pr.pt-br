---
title: Endereço de ponto de extremidade
description: Um endereço de ponto de extremidade representa o endereço de um serviço na rede.
ms.assetid: 5df9c0da-6648-42a0-ae87-06844461042a
keywords:
- Endereço do ponto de extremidade serviços Web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787326197bc73d57945720c34773d33b613a4aab
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104561605"
---
# <a name="endpoint-address"></a>Endereço de ponto de extremidade

Um endereço de ponto de extremidade representa o endereço de um serviço na rede. Ao abrir um [canal](channel.md), chamando a função [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) , você precisa fornecer o endereço do ponto de extremidade do serviço com o qual deseja se comunicar, bem como especificar o canal que você deseja abrir.


Um endereço de ponto de extremidade consiste em:

-   uma [URL](url.md)
-   um conjunto de cabeçalhos (opcional)
-   um conjunto de extensões (opcional)
-   uma [identidade](endpoint-identity.md) opcional que representa a identidade de segurança do serviço.

Quando uma mensagem é endereçada, a URL se torna o cabeçalho "para" da mensagem. Todos os cabeçalhos que fazem parte do endereço do ponto de extremidade também são adicionados à mensagem.

![Diagrama mostrando cabeçalhos de endereço do ponto de extremidade que estão sendo adicionados a uma mensagem.](images/endpointaddress.png)

Os canais abordam automaticamente todas as mensagens que são enviadas, usando a estrutura de [**\_ \_ endereço do ponto de extremidade WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) que foi passada para o [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel). Você também pode usar a função [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) para substituir esse comportamento padrão.

Quando [**o \_ \_ endereço do ponto de extremidade WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) é passado como um parâmetro, as funções [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) e [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) criam uma cópia do parâmetro de **\_ \_ endereço do ponto de extremidade WS** na memória e seu tamanho é limitado por 65536 bytes. [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) não tem essa limitação porque não requer a criação de uma cópia do parâmetro de **\_ \_ endereço de ponto de extremidade WS** .

As extensões especificadas no campo **extensões** do [**endereço do \_ ponto \_ de extremidade WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) não são usadas para tratar a mensagem, mas sim um mecanismo de extensibilidade que pode ser usado para fornecer informações adicionais (por exemplo, metadados) sobre o serviço. Extensões comuns podem ser lidas com a função [**WsReadEndpointAddressExtension**](/windows/desktop/api/WebServices/nf-webservices-wsreadendpointaddressextension) .

O campo de identidade opcional do endereço do ponto de extremidade pode incluir, por exemplo, o nome DNS do computador no qual o serviço está em execução ou o UPN da conta do Windows na qual o serviço está sendo executado. O campo de identidade não é usado para endereçar a mensagem, mas pode ser usado para obter um token de segurança para o serviço (por exemplo, para obter um tíquete Kerberos para o UPN de destino) e para verificar a identidade das respostas de serviço (por exemplo, uma identidade DNS usada para verificações de nome no certificado de serviço retornado durante o SSL).

Os endereços de ponto de extremidade podem ser lidos e gravados usando a [serialização](serialization.md) com o valor de enumeração do **tipo de endereço de ponto de \_ extremidade \_ \_ WS** do [**\_ tipo**](/windows/desktop/api/WebServices/ne-webservices-ws_type) Observação para serializar um endereço de ponto de extremidade, você deve saber a versão da especificação usada para os cabeçalhos de endereçamento, conforme especificado na enumeração da [**\_ \_ versão de endereçamento do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) .

 

 





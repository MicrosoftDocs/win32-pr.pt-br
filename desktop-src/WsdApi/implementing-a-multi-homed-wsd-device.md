---
description: Este tópico descreve o suporte a dispositivos multi-homed no WSDAPI e fornece recomendações de implementação para desenvolvedores de cliente e dispositivo.
ms.assetid: d30ed536-d477-4f50-8c80-aacc35f948b9
title: Implementando um dispositivo WSD multi-homed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ac83b0fe3b951e02e77ef9efc6241ce5a7e1780106b1e85e4f00b987bbbe05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991736"
---
# <a name="implementing-a-multi-homed-wsd-device"></a>Implementando um dispositivo WSD multi-homed

[O WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) e o DPWS (Perfil de Dispositivos para [Serviços Web)](https://specs.xmlsoap.org/ws/2006/02/devprof/) não descrevem a implementação de dispositivos multi-homed. Este tópico descreve o suporte a dispositivos multi-homed no WSDAPI e fornece recomendações de implementação para desenvolvedores de cliente e dispositivo. Neste tópico, supõe-se que as mensagens de descoberta sejam enviadas por IPv4 e IPv6 (se disponível) com a mesma ID de mensagem e informações de sequenciamento de aplicativo.

## <a name="discovery-in-a-multi-homed-environment"></a>Descoberta em um ambiente multi-homed

Conforme mencionado na [seção Hello](hello-message.md) e [XAddrs](xaddr-validation-rules.md) de Funcionalidade [adicional WS-Discovery](additional-ws-discovery-functionality.md), o WSDAPI nunca fornece XAddrs em uma mensagem Hello. Isso significa que a mesma mensagem Hello pode ser enviada em todos os interfaces de rede com a mesma ID de mensagem e informações de sequenciamento de aplicativo. Isso facilita a detecção de colisão do cliente para descartar várias mensagens Hello do mesmo dispositivo quando um cliente e o dispositivo compartilham mais de uma sub-rede.

Como os [XAddrs não](xaddr-validation-rules.md) são enviados na mensagem [Hello,](hello-message.md) as implementações do cliente devem enviar uma mensagem Resolver para obter o endereço do dispositivo relevante. [](resolve-message.md) A resolução deve ser enviada em todas as interfaces do cliente com a mesma ID de mensagem e o dispositivo deve filtrar mensagens duplicadas conforme necessário. Usar a mesma ID de mensagem para a mensagem Resolver permite que o dispositivo escolha uma interface preferencial para se comunicar com clientes, se necessário.

Ao enviar uma [mensagem ResolveMatch,](resolvematches-message.md) um dispositivo deve fornecer [XAddrs](xaddr-validation-rules.md) relacionados ao interface de rede sobre o qual ele está unicasando a mensagem. Essa prática ajuda a evitar várias tentativas de conexão de cliente e lógica de novas tentativas complicadas.

## <a name="metadata-exchange-in-a-multi-homed-environment"></a>Troca de metadados em um ambiente multi-homed

Implementar a troca de metadados em um ambiente de várias residências é mais difícil do que implementar a descoberta devido ao versionamento de metadados. Se um cliente solicitar metadados em várias interfaces, o cliente poderá receber várias mensagens [GetResponse](getresponse--metadata-exchange--message.md) em interfaces diferentes. Essas mensagens GetResponse podem conter **seções de** metadados de relação diferentes com a mesma versão de metadados. Isso reduz o valor do número de versão de metadados.

Há uma abordagem alternativa, em que uma única [mensagem GetResponse](getresponse--metadata-exchange--message.md) é enviada em resposta com todos os endereços para o serviço. A desvantagem desse método é que informações privadas, como a topologia de redes indiretamente acessíveis, podem ser divulgadas.

No Windows Vista, os metadados fornecidos pelo WSDAPI contêm apenas endereços válidos para a interface na qual a solicitação de metadados foi recebida.

 

 




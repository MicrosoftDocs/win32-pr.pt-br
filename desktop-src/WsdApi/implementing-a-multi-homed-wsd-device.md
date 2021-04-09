---
description: Este tópico descreve o suporte a dispositivos de hospedagem múltipla no WSDAPI e fornece recomendações de implementação para desenvolvedores de clientes e dispositivos.
ms.assetid: d30ed536-d477-4f50-8c80-aacc35f948b9
title: Implementando um dispositivo WSD de hospedagem múltipla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ac3537b96a577db47419d55cb5c6f732f8f7906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171648"
---
# <a name="implementing-a-multi-homed-wsd-device"></a>Implementando um dispositivo WSD de hospedagem múltipla

O [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) e os [dispositivos Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) não descrevem a implementação de dispositivos de hospedagem múltipla. Este tópico descreve o suporte a dispositivos de hospedagem múltipla no WSDAPI e fornece recomendações de implementação para desenvolvedores de clientes e dispositivos. Neste tópico, supõe-se que as mensagens de descoberta sejam enviadas por IPv4 e IPv6 (se disponível) com a mesma ID de mensagem e informações de sequenciamento de aplicativo.

## <a name="discovery-in-a-multi-homed-environment"></a>Descoberta em um ambiente de hospedagem múltipla

Conforme mencionado na seção [Hello](hello-message.md) e [XAddrs](xaddr-validation-rules.md) da [funcionalidade adicional de WS-Discovery](additional-ws-discovery-functionality.md), o WSDAPI nunca fornece XAddrs em uma mensagem de saudação. Isso significa que a mesma mensagem de saudação pode ser enviada em todas as interfaces de rede com a mesma ID de mensagem e informações de sequenciamento de aplicativo. Isso torna mais fácil para a detecção de colisão do cliente descartar várias mensagens de saudação do mesmo dispositivo quando um cliente e o dispositivo compartilharem mais de uma sub-rede.

Como os [XAddrs](xaddr-validation-rules.md) não são enviados na mensagem de [saudação](hello-message.md) , as implementações do cliente devem enviar uma mensagem de [resolução](resolve-message.md) para obter o endereço de dispositivo relevante. A resolução deve ser enviada em todas as interfaces de cliente com a mesma ID de mensagem e o dispositivo deve filtrar as mensagens duplicadas conforme necessário. O uso da mesma ID de mensagem para a mensagem de resolução permite que o dispositivo escolha uma interface preferencial para se comunicar com clientes, se necessário.

Ao enviar uma mensagem [ResolveMatch](resolvematches-message.md) , um dispositivo deve fornecer [XAddrs](xaddr-validation-rules.md) relacionados à interface de rede sobre a qual ele está unicast a mensagem. Essa prática ajuda a evitar várias tentativas de conexão de cliente e a lógica de repetição complicada.

## <a name="metadata-exchange-in-a-multi-homed-environment"></a>Troca de metadados em um ambiente de hospedagem múltipla

A implementação da troca de metadados em um ambiente de hospedagem múltipla é mais difícil do que implementar a descoberta devido ao controle de versão de metadados. Se um cliente solicitar metadados sobre várias interfaces, o cliente poderá receber várias mensagens [GetResponse](getresponse--metadata-exchange--message.md) em diferentes interfaces. Essas mensagens GetResponse podem conter seções diferentes de metadados de **relação** com a mesma versão de metadados. Isso reduz o valor do número de versão de metadados.

Há uma abordagem alternativa, em que uma única mensagem [GetResponse](getresponse--metadata-exchange--message.md) é enviada em resposta com todos os endereços para o serviço. A desvantagem desse método é que as informações privadas, como a topologia de redes indiretamente acessíveis, podem ser divulgadas.

No Windows Vista, os metadados fornecidos pelo WSDAPI contêm apenas endereços que são válidos para a interface na qual a solicitação de metadados foi recebida.

 

 




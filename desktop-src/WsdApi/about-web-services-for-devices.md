---
description: A API WSDAPI (Web Service on Devices) é uma implementação do DPWS (Perfil de Dispositivos para Serviços Web) do Windows Vista e Windows Server 2008.
ms.assetid: 8eaeacb3-43db-4a57-8548-e5b81213269c
title: Sobre serviços Web em dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c7facef3bfed004a834e151db0c58c83a1576e515ed89fa0d690813bc4c18bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118552501"
---
# <a name="about-web-services-on-devices"></a>Sobre serviços Web em dispositivos

A API WSDAPI (Web Service on Devices) é uma implementação do DPWS (Perfil de Dispositivos para [Serviços Web)](https://specs.xmlsoap.org/ws/2006/02/devprof/) do Windows Vista e Windows Server 2008. O DPWS restringe as especificações dos Serviços Web para que os clientes possam facilmente descobrir dispositivos. Depois que um dispositivo é descoberto, um cliente pode recuperar uma descrição dos serviços hospedados nesse dispositivo e usar esses serviços.

## <a name="devices-and-services"></a>Dispositivos e serviços

*Os* dispositivos são componentes, geralmente hardware, que são anexados à rede. Exemplos incluem impressoras, câmeras Web e sistemas de vídeo.

Os dispositivos podem incluir zero ou mais *serviços.* Por exemplo, um dispositivo de vídeo pode incluir serviços que suportam energia, controle de reprodução, ejetão de mídia e streaming de vídeo. O controle de reprodução pode dar suporte a ações como reproduzir, pausar, retroceder e avançar rapidamente.

## <a name="discovering-and-manipulating-a-device"></a>Descoberta e manipulação de um dispositivo

O WSDAPI estende o modelo de Plug and Play local, permitindo que um cliente descubra e acesse um dispositivo remoto e seus serviços associados em uma rede. Ele dá suporte à descoberta, mensagens de controle de duas vias e de descoberta e eventos.

![Diagrama mostrando como o WSDAPI permite que um cliente descubra e acesse um dispositivo remoto.](images/overview01.png)

Os dispositivos DPWS anunciam sua presença e expõem serviços (se algum) usando um endereço exclusivo e um conjunto padronizado de mensagens XML. Os clientes DPWS podem usar o processo de descoberta para encontrar o dispositivo, enumerar seus serviços e se conectar a esses serviços para executar ações específicas.

Um cliente WSDAPI primeiro consulta o dispositivo para descrições completas de seus serviços, incluindo os tipos de serviço (como um tipo de serviço de impressora ou um tipo de serviço de scanner). Em seguida, o cliente controla o dispositivo chamando comandos definidos por um tipo de serviço (por exemplo, chamando **CreatePrintJob** em um dispositivo com um tipo de serviço de impressora). Opcionalmente, o cliente também pode monitorar alterações de estado em cada serviço assinando eventos que ocorrem durante a execução do comando.

![Diagrama mostrando como um cliente WSDAPI consulta e interage com um dispositivo.](images/netdevice01.png)

Para obter mais informações sobre padrões de mensagens do dispositivo, consulte Descoberta e [metadados Exchange padrões de mensagem](discovery-and-metadata-exchange-message-patterns.md).

## <a name="logical-and-physical-addressing"></a>Endereçamento lógico e físico

O endereçamento lógico é usado para identificar exclusivamente dispositivos independentes de seus endereços físicos. WS-Discovery fornece um mecanismo para resolver endereços lógicos em endereços físicos, permitindo que mensagens de cliente para dispositivo ocorrem. Um exemplo é o NAS (armazenamento anexado à rede) que você carrega com você. Se você tiver um laptop e um NAS, seu laptop deverá ser capaz de reconhecer que ele é o mesmo dispositivo, independentemente do endereço físico (endereço IP) obtido pelo NAS conforme você se move entre sub-redes. Para fazer isso, é necessário que o dispositivo tenha uma identidade que seja independente do endereço IP obtido; como mecanismos tradicionais como DNS não estão disponíveis em um cenário de roaming normal, WS-Addressing e WS-Discovery fornecem endereçamento lógico e resolução como uma alternativa ad hoc.

Quando um dispositivo é fabricado, ele recebe um identificador global exclusivo, representado como um URI UUID. Esse identificador nunca será alterado para o dispositivo. Quando o dispositivo estiver ligado, ele sempre anunciará seu [](hello-message.md) endereço lógico por meio de uma mensagem Hello do WS-Discovery e aceitará [](resolve-message.md) solicitações para convertê-lo em um endereço físico (normalmente HTTP) por meio de mensagens WS-Discovery Resolver ou [Investigação.](probe-message.md) Depois que um endereço físico válido (endereço IP) é obtido, todas as mensagens ocorrem nesse endereço e o WS-Discovery é usado somente se o endereço muda, o dispositivo altera o estado e os clientes precisam ser notificados ou o dispositivo fica offline.

## <a name="building-applications"></a>Criando aplicativos

O WSDAPI fornece uma pilha SOAP DPWS genérica para uso por aplicativos de cliente e serviço. O gerador de código de serviços [Web](web-services-for-devices-code-generator.md) em dispositivos (WsdCodeGen.exe) pode ser usado para converter uma WSDL (descrição do serviço) em um código de proxy e stub que os aplicativos podem chamar diretamente. Esse código gerado transforma automaticamente chamadas de função e parâmetros em mensagens SOAP e campos XML e, em seguida, chama no WSDAPI para emitir solicitações para o dispositivo remoto ou cliente.

A Descoberta de Funções pode ser usada ao criar aplicativos WSDAPI para criar e ativar instâncias de função retornadas pelo PnP. Essas instâncias de função contêm dados que podem ser usados para obter mais informações por meio das APIs pnp quando mais do que apenas a descoberta simples é necessária. Para obter mais informações, consulte [Descoberta de funções](/previous-versions/windows/desktop/fundisc/fd-portal) e [PnP-X.](/previous-versions/windows/desktop/fundisc/pnp-x)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Padrões de mensagem de descoberta e Exchange metadados](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Conformidade da especificação WSDAPI](wsdapi-specification-compliance.md)
</dt> <dt>

[Visão geral das interfaces WSDAPI](overview-of-the-wsdapi-interfaces.md)
</dt> </dl>

 

 

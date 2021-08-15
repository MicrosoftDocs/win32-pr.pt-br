---
description: o serviço web na API de dispositivos (WSDAPI) é uma implementação do perfil de dispositivos para serviços Web (DPWS) para Windows Vista e Windows Server 2008.
ms.assetid: 8eaeacb3-43db-4a57-8548-e5b81213269c
title: Sobre os serviços Web em dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c7facef3bfed004a834e151db0c58c83a1576e515ed89fa0d690813bc4c18bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118552501"
---
# <a name="about-web-services-on-devices"></a>Sobre os serviços Web em dispositivos

o serviço web na API de dispositivos (WSDAPI) é uma implementação do [perfil de dispositivos para serviços Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) para Windows Vista e Windows Server 2008. O DPWS restringe as especificações de serviços da Web para que os clientes possam descobrir facilmente os dispositivos. Depois que um dispositivo é descoberto, um cliente pode recuperar uma descrição dos serviços hospedados nesse dispositivo e usar esses serviços.

## <a name="devices-and-services"></a>Dispositivos e serviços

*Dispositivos* são componentes, geralmente hardware, que são anexados à rede. Os exemplos incluem impressoras, câmeras da Web e sistemas de vídeo.

Os dispositivos podem incluir zero ou mais *Serviços*. Por exemplo, um dispositivo de vídeo pode incluir serviços que dão suporte à ativação e desativação, controle de reprodução, ejeção de mídia e streaming de vídeo. O controle de reprodução pode dar suporte a ações como reproduzir, pausar, retroceder e avançar rapidamente.

## <a name="discovering-and-manipulating-a-device"></a>Descobrindo e manipulando um dispositivo

O WSDAPI estende o modelo de Plug and Play local, permitindo que um cliente descubra e acesse um dispositivo remoto e seus serviços associados em uma rede. Ele dá suporte à descoberta, mensagens de controle unidirecional e bidirecional e eventos.

![Diagrama mostrando como o WSDAPI permite que um cliente descubra e acesse um dispositivo remoto.](images/overview01.png)

Os dispositivos DPWS anunciam sua presença e expõem serviços (se houver) usando um endereço exclusivo e um conjunto padronizado de mensagens XML. Os clientes do DPWS podem usar o processo de descoberta para localizar o dispositivo, enumerar seus serviços e conectar-se a esses serviços para executar ações específicas.

Um cliente WSDAPI primeiro consulta o dispositivo para obter descrições completas de seus serviços, incluindo os tipos de serviço (como um tipo de serviço de impressora ou um tipo de serviço de scanner). O cliente controla o dispositivo chamando comandos definidos por um tipo de serviço (por exemplo, chamando **CreatePrintJob** em um dispositivo com um tipo de serviço de impressora). Opcionalmente, o cliente também pode monitorar as alterações de estado em cada serviço assinando os eventos que ocorrem durante a execução do comando.

![Diagrama mostrando como um cliente WSDAPI consulta e interage com um dispositivo.](images/netdevice01.png)

para obter mais informações sobre padrões de mensagens de dispositivo, consulte [descoberta e metadados Exchange padrões de mensagem](discovery-and-metadata-exchange-message-patterns.md).

## <a name="logical-and-physical-addressing"></a>Endereçamento lógico e físico

O endereçamento lógico é usado para identificar exclusivamente os dispositivos independentemente de seus endereços físicos. O WS-Discovery fornece um mecanismo para resolver endereços lógicos em endereços físicos, permitindo que as mensagens de cliente para dispositivo ocorram. Um exemplo é o NAS (armazenamento anexado à rede) que você carrega com você. Se você tiver um laptop e um NAS, seu laptop deverá ser capaz de reconhecer que ele é o mesmo dispositivo, independentemente do endereço físico (endereço IP) que o NAS Obtém à medida que você se move entre sub-redes. Fazer isso requer que o dispositivo tenha identidade que seja independente do endereço IP Obtido; como os mecanismos tradicionais, como o DNS, não estão disponíveis em um cenário de roaming normal, WS-Addressing e WS-Discovery fornecem resolução e endereçamento lógico como uma alternativa ad hoc.

Quando um dispositivo é fabricado, ele recebe um identificador global exclusivo, representado como um URI UUID. Esse identificador nunca será alterado para o dispositivo. Quando o dispositivo estiver ligado, ele sempre anunciará seu endereço lógico por meio de uma WS-Discovery mensagem de [saudação](hello-message.md) e aceitará solicitações para converter isso em um endereço físico (normalmente http) via WS-Discovery [resolver](resolve-message.md) ou [investigar](probe-message.md) mensagens. Depois que um endereço físico (endereço IP) válido for obtido, todas as mensagens ocorrerão sobre esse endereço, e WS-Discovery será usada somente se o endereço for alterado, o estado do dispositivo mudar e os clientes precisarem ser notificados ou o dispositivo ficar offline.

## <a name="building-applications"></a>Criando aplicativos

O WSDAPI fornece uma pilha SOAP DPWS genérica para uso por aplicativos cliente e de serviço. Os [Serviços Web no gerador de código de dispositivos](web-services-for-devices-code-generator.md) (WsdCodeGen.exe) podem ser usados para converter uma descrição de serviço (WSDL) em código de proxy e stub que os aplicativos podem chamar diretamente. Esse código gerado transforma automaticamente chamadas de função e parâmetros em mensagens SOAP e em campos XML e, em seguida, chama o WSDAPI para emitir para solicitações para o cliente ou dispositivo remoto.

A descoberta de função pode ser usada ao criar aplicativos WSDAPI para criar e ativar instâncias de função retornadas por PnP. Essas instâncias de função contêm dados que podem ser usados para obter mais informações por meio de APIs PnP quando mais do que apenas a descoberta simples é necessária. Para obter mais informações, consulte [descoberta de função](/previous-versions/windows/desktop/fundisc/fd-portal) e [PnP-X](/previous-versions/windows/desktop/fundisc/pnp-x).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[descoberta e metadados Exchange padrões de mensagem](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Conformidade de especificação do WSDAPI](wsdapi-specification-compliance.md)
</dt> <dt>

[Visão geral das interfaces WSDAPI](overview-of-the-wsdapi-interfaces.md)
</dt> </dl>

 

 

---
description: A finalidade deste tópico é descrever a funcionalidade de descoberta implementada pelo WSDAPI, mas não descrita nas especificações DPWS ou WS-Discovery.
ms.assetid: ae7eff53-c932-4cba-9e71-c60f308f0e2d
title: Funcionalidade adicional de WS-Discovery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9856605273bec9c757e0b29c389991bf061309
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171230"
---
# <a name="additional-ws-discovery-functionality"></a>Funcionalidade adicional de WS-Discovery

Em alguns casos, o [perfil de dispositivos para serviços Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) e especificações relacionadas não definem a funcionalidade de implementação explicitamente. Por exemplo, a especificação [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) não define o comportamento de cliente e host em ambientes de hospedagem múltipla. Quando o WSDAPI foi implementado, algumas funcionalidades de descoberta foram adicionadas além da funcionalidade definida na especificação.

O WSDAPI também implementa partes selecionadas do WS-Discovery o CD1 v 1.1 para se comunicar com um proxy de descoberta sobre HTTP.

A finalidade deste tópico é descrever a funcionalidade de descoberta implementada pelo WSDAPI, mas não descrita nas especificações DPWS ou WS-Discovery.

## <a name="ipv6-addresses-and-the-soapudp-uri-format"></a>Endereços IPv6 e o formato de URI SOAP. UDP

SOAP-over-UDP e WS-Discovery não descrevem explicitamente como um endereço IPv6 literal é representado no formato de URI SOAP. UDP. [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt), "Uniform Resource Identifiers (URI): sintaxe genérica", indica que os endereços IPv6 literais não são suportados pelo formato de URI SOAP. UDP.

Para simplificar, o WSDAPI reconhece endereços IPv6 entre colchetes no esquema SOAP. UDP. Por exemplo, o endereço `soap.udp://[2001:abcd:0001:0002:0003:0004:0005:0032]:3702` é reconhecido pelo WSDAPI. Isso é semelhante a como os endereços IPv6 são tratados em HTTP.

## <a name="hello-and-xaddrs"></a>Olá e XAddrs

O objeto de hospedagem DPWS do WSDAPI nunca enviará um WS-Discovery mensagem de [saudação](hello-message.md) com [XAddrs](xaddr-validation-rules.md) no corpo da mensagem. Um cliente sempre enviará uma mensagem de [resolução](resolve-message.md) depois de receber uma mensagem de saudação, se o cliente precisar obter o XAddrs.

Há dois benefícios dessa abordagem. Primeiro, um dispositivo criado em WSDAPI nunca vai expor XAddrs que divulguem os endereços IP de redes privadas. Em segundo lugar, um dispositivo criado no WSDAPI expõe apenas XAddrs que são acessíveis para o cliente, o que significa que os endereços IPv6 nunca são enviados para um cliente IPv4.

Quando uma mensagem de [investigação](probe-message.md) ou resolução é recebida, apenas um único XAddr é enviado em resposta. O XAddr enviado corresponde ao endereço local no qual a solicitação foi recebida. Se a solicitação foi recebida em sub-redes via IPv6, o WSDAPI fornecerá um endereço IPv6 global na resposta.

## <a name="preferred-addresses"></a>Endereços preferenciais

Um dispositivo pode fornecer vários XAddrs em uma mensagem [Hello](hello-message.md), [ProbeMatch](probematches-message.md)ou [ResolveMatch](resolvematches-message.md) . Um serviço também pode estar disponível em vários pontos de extremidade com endereços de transporte diferentes. Nesses casos, o WSDAPI tentará se comunicar com o dispositivo no primeiro endereço utilizável que encontrar. Um endereço pode ser usado se for de um protocolo disponível, como IPv4 em um computador em que o IPv4 está instalado ou IPv6 em um computador em que o IPv6 está instalado. Além disso, se o endereço vier de um dispositivo ou serviço que não está na sub-rede local, ele só será utilizável se for IPv4, local de site IPv6 ou link local IPv6.

## <a name="wsdl-in-metadata-exchange"></a>WSDL na troca de metadados

Os dispositivos e serviços criados no WSDAPI não fornecem seu WSDL na troca de metadados, a menos que sejam estendidos pelo aplicativo para fornecer essas informações. Por padrão, o provisionamento de WSDL não faz parte do modelo de programação.

## <a name="app_max_delay"></a>\_atraso máximo do aplicativo \_

DPWS define \_ \_ o atraso máximo do aplicativo, o intervalo aleatório a ser atrasado entre o recebimento de uma [investigação](probe-message.md) e o envio de um [ProbeMatch](probematches-message.md), como 5.000 milissegundos. O Firewall do Windows requer que o modelo de resposta de difusão unicast/solicitação multicast para UDP funcione apenas na janela de firewall de 4 segundos. Como resultado, o WSDAPI transmitirá respostas em 2.500 MS ou menos, em vez da janela 5.000 MS descrita pelo \_ atraso máximo do aplicativo \_ .

## <a name="iana-port-reservations"></a>Reservas de porta IANA

O WSDAPI usa a porta TCP 5357 para tráfego HTTP e a porta TCP 5358 para tráfego HTTPS por padrão. Essas portas são reservadas para processos de privilégios mais baixos por meio de uma reserva de URL no HTTP.sys e também são reservadas com o IANA.

## <a name="udp-port-sharing"></a>Compartilhamento de porta UDP

O WSDAPI usa o compartilhamento de porta. Mensagens unicast enviadas à porta 3702 podem não ser manipuladas corretamente por todos os aplicativos baseados em WSDAPI. Se um aplicativo se associar exclusivamente à porta 3702, ele poderá impedir que aplicativos baseados em WSDAPI usem essa porta corretamente.

## <a name="ws-discovery-v11-cd1-proxy"></a>Proxy do CD1 do WS-Discovery v 1.1

O WSDAPI pesquisará e se comunicará com um proxy de descoberta que implementa o protocolo de modo gerenciado do CD1 do WS-Discovery v 1.1. WS-Discovery o CD1 v 1.1 é a primeira revisão de WS-Discovery incluir uma descrição explícita de um protocolo HTTP para a comunicação entre um proxy e um cliente ou dispositivo.

Para limitar o número de versões simultâneas usadas em solicitações de multicast, o WSDAPI envia uma solicitação de investigação de WS-Discovery no namespace 2005/04, mas procura o tipo de DiscoveryProxy do CD1 do WS-Discovery v 1.1. Se um proxy responder, o WSDAPI enviará uma investigação HTTP ou uma solicitação de resolução para o ponto de extremidade de proxy especificado, conforme definido em WS-Discovery o CD1 v 1.1.

 

 




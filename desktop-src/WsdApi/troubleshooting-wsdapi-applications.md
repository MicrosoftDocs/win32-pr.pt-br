---
description: Lista os procedimentos de diagnóstico a serem usados ao solucionar problemas de aplicativos WSDAPI.
ms.assetid: befe4234-8d3a-4fc5-9a7d-faca94964af6
title: Solução de problemas de outros aplicativos WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a421f26237cc14d07a43e00faeb6d8bf49aa02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797954"
---
# <a name="troubleshooting-other-wsdapi-applications"></a>Solução de problemas de outros aplicativos WSDAPI

Os aplicativos podem chamar diretamente em interfaces e funções WSDAPI para executar a descoberta de dispositivos e a troca de metadados. Os padrões de mensagem usados por esses aplicativos variam.

O objetivo deste guia de solução de problemas é ajudar os desenvolvedores de aplicativos WSDAPI a implementar com êxito um proxy de dispositivo. Este guia não destina-se a ajudar a solucionar todos os aspectos do WSDAPI. Se o proxy do dispositivo tiver sido criado com êxito e o cliente e o host puderem ver uns aos outros na rede, este guia não poderá resolver os problemas do aplicativo. Para solucionar esses problemas de aplicativos, siga as instruções em [habilitando o rastreamento WSDAPI](enabling-wsdapi-tracing.md) e entre em contato com o suporte da Microsoft para obter mais assistência.

## <a name="troubleshooting-clients-calling-wsdcreatedeviceproxy"></a>Solucionando problemas de clientes chamando WSDCreateDeviceProxy

Os aplicativos chamam [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) para criar e inicializar uma instância da interface [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) . Esse objeto de proxy de dispositivo pode ser usado para anunciar serviços em um dispositivo e também para trocar metadados.

Um aplicativo que chama [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) sempre usa as mensagens a seguir.

-   [Obter](get--metadata-exchange--http-request-and-message.md)
-   [GetResponse](getresponse--metadata-exchange--message.md)

Um aplicativo que chama [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) às vezes usa as mensagens a seguir.

-   [Resolver](resolve-message.md)
-   [ResolveMatches](resolvematches-message.md)

As mensagens [resolve](resolve-message.md) e [ResolveMatches](resolvematches-message.md) são geradas quando um endereço de dispositivo lógico (ou seja, um endereço de dispositivo do formato urn: UUID: {GUID}) é passado para *pszDeviceId*. Essas mensagens não são geradas quando um endereço de dispositivo físico é passado para *pszDeviceId*. Quando as mensagens de resolução e ResolveMatches são usadas, elas são enviadas antes das mensagens [Get](get--metadata-exchange--http-request-and-message.md) e [GetResponse](getresponse--metadata-exchange--message.md) .

Os procedimentos de diagnóstico a seguir devem ser usados (em ordem) para ajudar a identificar problemas com um aplicativo chamando [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) com um endereço de dispositivo físico.

1.  [Inspecione as configurações do adaptador e do firewall](inspecting-adapter-and-firewall-settings.md).
2.  [Use um host genérico e um cliente para a troca de metadados http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
3.  [Use o log do WinHTTP para verificar o tráfego de obtenção](using-winhttp-logging-to-verify-get-traffic.md).
4.  [Inspecione os rastreamentos de rede para a troca de metadados http](inspecting-network-traces-for-http-metadata-exchange.md).

Os procedimentos de diagnóstico a seguir devem ser usados (em ordem) para ajudar a identificar problemas com um aplicativo chamando [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) com um endereço de dispositivo lógico.

1.  [Inspecione as configurações do adaptador e do firewall](inspecting-adapter-and-firewall-settings.md).
2.  [Use um host genérico e um cliente para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).
3.  [Use o cliente de depuração WSD para verificar o tráfego multicast](using-wsddebug-client-to-verify-multicast-traffic.md).
4.  [Inspecione os rastreamentos de rede para o WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md).
5.  [Use um host genérico e um cliente para a troca de metadados http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
6.  [Use o log do WinHTTP para verificar o tráfego de obtenção](using-winhttp-logging-to-verify-get-traffic.md).
7.  [Inspecione os rastreamentos de rede para a troca de metadados http](inspecting-network-traces-for-http-metadata-exchange.md).

Verifique se as mensagens de [resolução](resolve-message.md) e [ResolveMatches](resolvematches-message.md) são geradas e atendem aos requisitos de tráfego. Não é necessário procurar mensagens de [investigação](probe-message.md) ou [ProbeMatches](probematches-message.md) na saída do cliente de depuração WSD ou nos rastreamentos de rede.

## <a name="troubleshooting-clients-calling-wsdcreatedeviceproxyadvanced"></a>Solucionando problemas de clientes chamando WSDCreateDeviceProxyAdvanced

Os aplicativos chamam [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) para criar e inicializar uma instância da interface [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) . Ao contrário de [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy), **WSDCreateDeviceProxyAdvanced** tem um parâmetro *pDeviceAddress* que é usado para definir o endereço de transporte do dispositivo. Se esse endereço de transporte for especificado, a resolução de endereço lógico não será [necessária e as](resolve-message.md) mensagens [ResolveMatches](resolvematches-message.md) não serão geradas.

Se *pDeviceAddress* for definido como **NULL** e *pszDeviceId* for um endereço lógico, a [resolução de endereço será necessária e as](resolve-message.md) mensagens [ResolveMatches](resolvematches-message.md) serão geradas.

Os procedimentos de diagnóstico a seguir devem ser usados (em ordem) para ajudar a identificar problemas com um aplicativo chamando [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) com um parâmetro _pDeviceAddress_ não **nulo**. Esses procedimentos também podem ser usados quando *pDeviceAddress* é **nulo** e *pszDeviceId* é um endereço físico.

1.  [Inspecione as configurações do adaptador e do firewall](inspecting-adapter-and-firewall-settings.md).
2.  [Use um host genérico e um cliente para a troca de metadados http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
3.  [Use o log do WinHTTP para verificar o tráfego de obtenção](using-winhttp-logging-to-verify-get-traffic.md).
4.  [Inspecione os rastreamentos de rede para a troca de metadados http](inspecting-network-traces-for-http-metadata-exchange.md).

Os procedimentos de diagnóstico a seguir devem ser usados (em ordem) para ajudar a identificar problemas com um aplicativo chamando [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) com *PDeviceAddress* definido como **nulo** e com *pszDeviceId* definido como um endereço lógico.

1.  [Inspecione as configurações do adaptador e do firewall](inspecting-adapter-and-firewall-settings.md).
2.  [Use um host genérico e um cliente para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).
3.  [Use o cliente de depuração WSD para verificar o tráfego multicast](using-wsddebug-client-to-verify-multicast-traffic.md).
4.  [Inspecione os rastreamentos de rede para o WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md).
5.  [Use um host genérico e um cliente para a troca de metadados http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
6.  [Use o log do WinHTTP para verificar o tráfego de obtenção](using-winhttp-logging-to-verify-get-traffic.md).
7.  [Inspecione os rastreamentos de rede para a troca de metadados http](inspecting-network-traces-for-http-metadata-exchange.md).

Verifique se as mensagens de [resolução](resolve-message.md) e [ResolveMatches](resolvematches-message.md) são geradas e atendem aos requisitos de tráfego. Não é necessário procurar mensagens de [investigação](probe-message.md) ou [ProbeMatches](probematches-message.md) na saída do cliente de depuração WSD ou nos rastreamentos de rede.

## <a name="troubleshooting-clients-using-the-iwsdiscoveryprovider-interface"></a>Solucionando problemas de clientes usando a interface IWSDiscoveryProvider

Os aplicativos que chamam a interface [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) não executam a troca de metadados. Essa interface é usada somente para descoberta. Os padrões de mensagem e os procedimentos de solução de problemas são diferentes para cada método chamado na interface **IWSDiscoveryProvider** .

Quando um aplicativo chama [**IWSDiscoveryProvider:: SearchByType**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype), uma mensagem de [investigação](probe-message.md) é gerada. A mensagem de investigação é enviada por multicast UDP para a porta 3702. Uma mensagem [ProbeMatches](probematches-message.md) é gerada em resposta. A mensagem ProbeMatches é enviada por UDP unicast e é originada da porta 3702.

Quando um aplicativo chama [**IWSDiscoveryProvider:: SearchById**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid), uma mensagem de [resolução](resolve-message.md) é gerada. Uma mensagem de resolução é enviada pelo multicast UDP para a porta 3702. Uma mensagem [ResolveMatches](resolvematches-message.md) é gerada em resposta. O ResolveMatches é enviado por UDP unicast e origina-se da porta 3702.

Os procedimentos de diagnóstico a seguir devem ser usados (em ordem) para ajudar a identificar problemas com um aplicativo chamando [**IWSDiscoveryProvider:: SearchByType**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype) ou [**IWSDiscoveryProvider:: SearchById**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid). Verifique se as mensagens geradas pela API chamada atendem aos requisitos de tráfego.

1.  [Inspecione as configurações do adaptador e do firewall](inspecting-adapter-and-firewall-settings.md).
2.  [Use um host genérico e um cliente para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).
3.  [Use o cliente de depuração WSD para verificar o tráfego multicast](using-wsddebug-client-to-verify-multicast-traffic.md).
4.  [Inspecione os rastreamentos de rede para o WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md).

Se um aplicativo chamar [**IWSDiscoveryProvider:: SearchByAddress**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyaddress), ele será um aplicativo de descoberta direcionado. Para obter mais informações sobre solução de problemas, consulte [Solucionando problemas de aplicativos usando a descoberta dirigida](troubleshooting-applications-using-directed-discovery.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com a solução de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 




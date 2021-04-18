---
description: Os serviços Web na API de dispositivos (WSDAPI) são usados para desenvolver aplicativos cliente que localizam e acessam dispositivos e para desenvolver hosts de dispositivo e serviços associados que são executados no Windows Vista e no Windows Server 2008.
ms.assetid: 2b23d7d3-3b06-48c8-993e-49c72b139624
title: Visão geral das interfaces WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3e728971741f97707c1dc72effdaf0ca17dbb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781388"
---
# <a name="overview-of-the-wsdapi-interfaces"></a>Visão geral das interfaces WSDAPI

Os serviços Web na API de dispositivos (WSDAPI) são usados para desenvolver aplicativos cliente que localizam e acessam dispositivos e para desenvolver hosts de dispositivo e serviços associados que são executados no Windows Vista e no Windows Server 2008. A API de [descoberta de função](/previous-versions/windows/desktop/fundisc/fd-portal) e a ferramenta [WsdCodeGen](web-services-for-devices-code-generator.md) são ferramentas complementares que podem ser usadas para o cliente, o host do dispositivo e o desenvolvimento do serviço. As interfaces WSDAPI podem ser usadas diretamente para expor a funcionalidade avançada.

## <a name="major-wsdapi-interfaces"></a>Principais interfaces WSDAPI

As quatro principais interfaces WSDAPI são [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider), [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher), [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)e [**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost). Para obter uma lista de todas as interfaces WSDAPI, consulte [Serviços Web em interfaces de dispositivos](web-services-for-devices-interfaces.md).

## <a name="iwsdiscoveryprovider"></a>IWSDiscoveryProvider

[**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) é usado para implementar WS-Discovery funcionalidade em clientes.

[**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) problemas WS-Discovery [investigação](probe-message.md) e [resolução](resolve-message.md) de mensagens e recebe mensagens de [saudação](hello-message.md), [adeus](bye-message.md), [ProbeMatches](probematches-message.md)e [ResolveMatches](resolvematches-message.md) . Use as informações recuperadas por meio da interface **IWSDiscoveryProvider** ao criar uma interface [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) usada para descrever e controlar um dispositivo DPWS específico.

Uma interface [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) não é necessária para simplesmente resolver um endereço de dispositivo DPWS específico antes de criar um proxy de dispositivo. O [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) resolverá automaticamente o endereço do dispositivo, se necessário.

A API de [descoberta de função](/previous-versions/windows/desktop/fundisc/fd-portal) pode ser usada para descoberta de dispositivo e serviço genérico, pois a API pode descobrir dispositivos DPWS e também dispositivos usando outros protocolos. Considere o uso da descoberta de função ao escrever um aplicativo de descoberta genérico.

## <a name="iwsdiscoverypublisher"></a>IWSDiscoveryPublisher

[**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) é usado para implementar WS-Discovery funcionalidade nos serviços de destino, como dispositivos.

O [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) permite que um aplicativo publique sua presença usando WS-Discovery mensagens de saudação e adeus. Essa interface permite que um aplicativo receba solicitações de investigação e resolução e construa e envie respostas ProbeMatches e ResolveMatches.

Uma interface [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) não é necessária ao simplesmente publicar a existência de um objeto [**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) . O **IWSDDeviceHost** gerencia sua própria presença de WS-Discovery.

## <a name="iwsddeviceproxy"></a>IWSDDeviceProxy

O [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) é usado para implementar a funcionalidade WS-Discovery, WS-MetadataExchange e Control do lado do cliente. Essa funcionalidade inclui recursos opcionais de canal seguro, WS-Event e Attachment.

A interface [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) tem os três usos a seguir.

-   Resolve endereços lógicos de dispositivo, se necessário.
-   Inicia solicitações de metadados para dispositivos para enumerar os tipos e endereços de serviços.
-   Fornece uma fonte para objetos [**IWSDServiceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy) , que podem ser usados para emitir mensagens de controle para serviços específicos em um dispositivo.

O objeto [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) normalmente é criado e usado inteiramente dentro do código gerado pelo [WsdCodeGen](web-services-for-devices-code-generator.md).

## <a name="iwsddevicehost"></a>IWSDDeviceHost

O [**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) é usado para implementar o WS-Discovery, o WS-MetadataExchange e a funcionalidade de Hospedagem de serviço no lado do dispositivo. Os serviços hospedados podem responder a mensagens de controle e podem dar suporte a recursos de canal seguro, WS-Event e de anexo.

A interface [**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) tem os seguintes usos.

-   Hospeda objetos de serviço.
-   Anuncia a presença de um host de dispositivo na rede usando o WS-Discovery.
-   Responde a WS-MetadataExchange solicitações e descreve os tipos e os locais dos serviços hospedados.
-   Despacha solicitações de rede em objetos de serviço.

O WS-Discovery, o WS-MetadataExchange e a funcionalidade de gerenciamento de assinatura WS-Eventing são manipulados inteiramente dentro do objeto de host do dispositivo. Antes que um serviço possa ser hospedado dentro de um host de dispositivo, os requisitos a seguir devem ser atendidos.

-   O host deve ser criado chamando [**WSDCreateDeviceHost**](/windows/desktop/api/WsdHost/nf-wsdhost-wsdcreatedevicehost).
-   Os metadados associados ao serviço devem ser registrados.
-   O próprio serviço deve ser registrado.
-   O host do dispositivo deve ser iniciado.

O objeto [**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) normalmente é criado e usado dentro do código gerado pelo [WsdCodeGen](web-services-for-devices-code-generator.md).

 

 

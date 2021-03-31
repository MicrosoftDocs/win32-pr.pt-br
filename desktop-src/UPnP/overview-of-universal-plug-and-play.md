---
title: Visão geral da arquitetura UPnP
description: A arquitetura UPnP define a conectividade de rede ponto a ponto de dispositivos inteligentes, dispositivos e pontos de controle.
ms.assetid: 09aba033-6229-4a55-9421-a7b967508bf4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ce11009bfecfe03fa176c1e6c75be173fbde86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823904"
---
# <a name="overview-of-upnp-architecture"></a>Visão geral da arquitetura UPnP

A arquitetura UPnP define a conectividade de rede ponto a ponto de dispositivos inteligentes, dispositivos e [*pontos de controle*](c-gly.md). Ele foi projetado para trazer conectividade fácil de usar, flexível e baseada em padrões para redes ad hoc, gerenciadas ou não gerenciadas, quer essas redes estejam em casa, pequenas empresas ou anexadas diretamente à Internet. A arquitetura UPnP é uma arquitetura de rede aberta e distribuída que usa as tecnologias existentes de TCP/IP e da Web para habilitar a rede de proximidade direta, além de controle e transferência de dados entre dispositivos de rede.

UPnP é um pacote de protocolo baseado em IP baseado em versões preliminares de protocolos de serviços da Web, como XML e SOAP (Simple Object Access Protocol). Com o UPnP, um dispositivo pode ingressar dinamicamente em uma rede, obter um endereço IP, transmitir seu recurso e descobrir a presença e os recursos de outros dispositivos na rede.

Um dispositivo UPnP é um contêiner de serviços e dispositivos aninhados. Por exemplo, um videocassete pode consistir em um serviço de transporte de fita, um serviço de sintonizador e um serviço de relógio. Diferentes categorias de dispositivos UPnP são associadas a diferentes conjuntos de serviços e dispositivos inseridos. Por exemplo, os serviços em um videocassete são diferentes daqueles dentro de uma impressora. As informações sobre o conjunto de serviços que um determinado tipo de dispositivo pode fornecer são capturadas em um documento de descrição de dispositivo XML que o dispositivo hospeda. A descrição do dispositivo também lista Propriedades, como nome do dispositivo e ícones associados ao dispositivo. A Microsoft aprimorou o suporte a UPnP para incluir a integração com [PnP-X e a](/previous-versions/windows/desktop/fundisc/pnp-x) [descoberta de função](/previous-versions/windows/desktop/fundisc/fd-portal).

A arquitetura UPnP é mais do que apenas uma extensão simples do modelo periférico plug-and-Play. Ele dá suporte à configuração zero, à rede invisível e à descoberta automática para uma variedade de categorias de dispositivo de uma ampla variedade de fornecedores. Isso permite que um dispositivo ingresse dinamicamente em uma rede, obtenha um endereço IP e transmita seus recursos mediante solicitação. Em seguida, outros pontos de controle podem usar a API do ponto de controle com tecnologia UPnP para saber mais sobre a presença e os recursos de outros dispositivos. Um dispositivo pode deixar uma rede tranqüila e automaticamente quando não está mais em uso.

O que é universal sobre a tecnologia UPnP?

-   Independência de mídia e dispositivo. A tecnologia UPnP pode ser executada em qualquer meio, incluindo linha telefônica, linha de alimentação, Ethernet, RF e 1394.
-   Independência de plataforma. Os fornecedores usam qualquer sistema operacional e qualquer linguagem de programação para criar produtos baseados em UPnP.
-   Tecnologias baseadas na Internet. A tecnologia UPnP baseia-se no IP, TCP, UDP, HTTP e XML, entre outros.
-   Controle de interface do usuário. A arquitetura UPnP permite o controle do fornecedor sobre a interface do usuário do dispositivo e a interação usando o navegador.
-   Controle programático. A arquitetura UPnP também habilita o controle programático de aplicativos convencionais.
-   Protocolos de base comuns. Os fornecedores concordam com conjuntos de protocolo base por dispositivo.
-   Extensível. Cada produto baseado em UPnP pode ter serviços de valor agregado em camadas sobre a arquitetura básica do dispositivo pelos fabricantes individuais.

A tecnologia UPnP é ampla no escopo, pois destina-se a redes domésticas, redes de proximidade e redes em pequenas empresas e prédios comerciais. Ele permite a comunicação de dados entre dois dispositivos no comando de qualquer dispositivo de controle na rede. A tecnologia UPnP é independente de qualquer sistema operacional específico, linguagem de programação ou mídia física.

A Microsoft fornece duas APIs para trabalhar com dispositivos baseados em UPnP:

-   [API de ponto de controle](control-point-api.md) -fornece um conjunto de interfaces com que permitem que os aplicativos encontrem e controlem dispositivos baseados em UPnP.
-   [API de host de dispositivo](device-host-api.md) – fornece um conjunto de interfaces com que permitem aos desenvolvedores escrever a funcionalidade do dispositivo principal e registrar o dispositivo no host do dispositivo. O host do dispositivo manipula a descoberta, a descrição, o controle e as partes de eventos da funcionalidade do dispositivo baseado em UPnP.

 

 
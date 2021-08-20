---
title: Visão geral da arquitetura UPnP
description: A arquitetura UPnP define a conectividade de rede ponto a ponto de dispositivos inteligentes, dispositivos e pontos de controle.
ms.assetid: 09aba033-6229-4a55-9421-a7b967508bf4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5866d3e701f53e95225538655ca45d159fb7c5f67d00e3c46c97357c7a9ee6a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126449"
---
# <a name="overview-of-upnp-architecture"></a>Visão geral da arquitetura UPnP

A arquitetura UPnP define a conectividade de rede ponto a ponto de dispositivos inteligentes, dispositivos e pontos [*de controle*](c-gly.md). Ele foi projetado para trazer conectividade fácil de usar, flexível e baseada em padrões para redes ad hoc, gerenciadas ou não gerenciadas, independentemente de essas redes estar em casa, pequenas empresas ou conectadas diretamente à Internet. A arquitetura UPnP é uma arquitetura de rede distribuída e aberta que usa tecnologias TCP/IP e Web existentes para habilitar a rede de proximidade contínua, além de controle e transferência de dados entre dispositivos em rede.

O UPnP é um conjunto de protocolos baseado em IP com base em versões preliminares de protocolos de Serviços Web, como XML e SOAP (Simple Object Access Protocol). Com o UPnP, um dispositivo pode ingressar dinamicamente em uma rede, obter um endereço IP, transmitir sua funcionalidade e descobrir a presença e os recursos de outros dispositivos na rede.

Um dispositivo UPnP é um contêiner de serviços e dispositivos aninhados. Por exemplo, um VCR pode consistir em um serviço de transporte em fita, um serviço de ajuste e um serviço de relógio. Diferentes categorias de dispositivos UPnP estão associadas a diferentes conjuntos de serviços e dispositivos inseridos. Por exemplo, os serviços em um VCR são diferentes daqueles em uma impressora. Informações sobre o conjunto de serviços que um tipo de dispositivo específico pode fornecer são capturadas em um documento de descrição do dispositivo XML que o dispositivo hospeda. A descrição do dispositivo também lista propriedades como nome do dispositivo e ícones associados ao dispositivo. A Microsoft aprimorou o suporte a UPnP para incluir a integração com [o PnP-X](/previous-versions/windows/desktop/fundisc/pnp-x) e o [Function Discovery.](/previous-versions/windows/desktop/fundisc/fd-portal)

A arquitetura UPnP é mais do que apenas uma extensão simples do modelo periférico plug-and-play. Ele dá suporte à configuração zero, rede invisível e descoberta automática para uma variedade de categorias de dispositivo de uma ampla variedade de fornecedores. Isso permite que um dispositivo insere dinamicamente uma rede, obtenha um endereço IP e transmita seus recursos mediante solicitação. Em seguida, outros pontos de controle podem usar a API do Ponto de Controle com a tecnologia UPnP para saber mais sobre a presença e os recursos de outros dispositivos. Um dispositivo pode deixar uma rede sem problemas e automaticamente quando ele não estiver mais em uso.

O que é universal sobre a tecnologia UPnP?

-   Independência de mídia e dispositivo. A tecnologia UPnP pode ser executado em qualquer meio, incluindo linha telefônica, linha de energia, Ethernet, RF e 1394.
-   Independência de plataforma. Os fornecedores usam qualquer sistema operacional e qualquer linguagem de programação para criar produtos baseados em UPnP.
-   Tecnologias baseadas na Internet. A tecnologia UPnP é criada com base em IP, TCP, UDP, HTTP e XML, entre outros.
-   Controle de interface do usuário. A arquitetura UPnP permite que o fornecedor controle sobre a interface do usuário do dispositivo e a interação usando o navegador.
-   Controle programático. A arquitetura UPnP também habilita o controle programático de aplicativo convencional.
-   Protocolos base comuns. Os fornecedores concordam sobre conjuntos de protocolos base por dispositivo.
-   Extensível. Cada produto baseado em UPnP pode ter serviços de valor agregado em camadas sobre a arquitetura básica do dispositivo pelos fabricantes individuais.

A tecnologia UPnP é ampla no escopo, já que tem como alvo redes de residência, redes de proximidade e redes em pequenas empresas e edifícios comerciais. Ele permite a comunicação de dados entre dois dispositivos sob o comando de qualquer dispositivo de controle na rede. A tecnologia UPnP é independente de qualquer sistema operacional específico, linguagem de programação ou mídia física.

A Microsoft fornece duas APIs para trabalhar com dispositivos baseados em UPnP:

-   [API do Ponto de](control-point-api.md) Controle – fornece um conjunto de interfaces COM que permitem que os aplicativos encontrem e controlem dispositivos baseados em UPnP.
-   [API do Host do](device-host-api.md) Dispositivo – fornece um conjunto de interfaces COM que permitem que os desenvolvedores escrevam a funcionalidade principal do dispositivo e registrem o dispositivo com o Host do Dispositivo. O Host do Dispositivo lida com as partes de descoberta, descrição, controle e eventos da funcionalidade do dispositivo baseado em UPnP.

 

 
---
description: A rede ponto a ponto é uma tecnologia de rede sem servidor que permite que vários dispositivos de rede compartilhem recursos e se comuniquem diretamente entre si.
ms.assetid: d2a43d3b-2782-4777-8c65-05e2c52930d0
title: O que é rede de mesmo nível?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f6ce2175aa32e37c80c4cde5c231540a48c448360974ecbd022c21eb552ccdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034096"
---
# <a name="what-is-peer-networking"></a>O que é rede de mesmo nível?

A rede ponto a ponto é uma tecnologia de rede sem servidor que permite que vários dispositivos de rede compartilhem recursos e se comuniquem diretamente entre si. essa tecnologia está disponível para o Windows XP com Service Pack 1 (SP1) e clientes posteriores que executam o pacote de rede avançado para a infraestrutura ponto a ponto.

A infraestrutura ponto a ponto é um conjunto de APIs de rede para ajudá-lo a desenvolver aplicativos de rede descentralizados que usam a potência coletiva dos computadores em uma rede. Por exemplo, aplicativos ponto a ponto podem ser comunicações colaborativas, tecnologias de distribuição de conteúdo e assim por diante.

A infraestrutura ponto a ponto fornece uma infraestrutura de rede sólida para que você possa se concentrar no desenvolvimento de aplicativos, pois a infraestrutura é desenvolvida para você.

A infraestrutura ponto a ponto inclui os seguintes componentes principais:

-   [Resolução de nome de par escalonável e seguro](#scalable-and-secure-peer-name-resolution)
-   [Comunicação eficiente com o MultiPoint](#efficient-multipoint-communication)
-   [Gerenciamento de dados distribuídos](#distributed-data-management)
-   [Identidades de pares seguros](#secure-peer-identities)
-   [Proteger grupos ponto a ponto](#secure-peer-to-peer-groups)

## <a name="scalable-and-secure-peer-name-resolution"></a>Resolução de nome de par escalonável e seguro

A [API do provedor de Namespace PNRP (Peer Name Resolution Protocol)](pnrp-namespace-provider-api.md) é um protocolo de resolução de nome para IP. O escopo ou contexto IPv6 que inclui todos os pares participantes é chamado de [nuvem](clouds.md). O PNRP permite que os colegas interajam entre si dentro de uma nuvem.

## <a name="efficient-multipoint-communication"></a>Comunicação eficiente com o MultiPoint

A infraestrutura ponto a ponto inclui a API de [gráfico](graphing-api.md) que fornece comunicação eficiente do MultiPoint. Como o PNRP, o grafo ponto a ponto permite que um conjunto de nós interaja e passe dados entre si na forma de um [registro](records.md). Cada registro gerado por um par ou atualizações é enviado para todos os nós em um grafo.

## <a name="distributed-data-management"></a>Gerenciamento de Dados distribuídos

O gerenciamento de dados distribuídos armazena automaticamente todos os registros enviados a um grafo ponto a ponto até o tempo de expiração especificado para cada registro. A rede ponto a ponto garante que cada nó em um grafo ponto a ponto tenha uma exibição semelhante do banco de dados de registro. Se um grafo ponto a ponto tiver um modelo de segurança associado a ele, o grafo conterá as seguintes informações:

-   Who pode e não pode se conectar a um grafo
-   Who pode proteger e validar registros com base em critérios definidos externamente

## <a name="secure-peer-identities"></a>Identidades de pares seguros

A infraestrutura ponto a ponto fornece uma [API do Gerenciador de identidade](identity-manager-api.md) ponto a ponto que permite criar, gerenciar e manipular as identidades de pares. As identidades de par são usadas para definir nomes para pontos de extremidade seguros em PNRP e podem representar qualquer recurso que participe de uma rede ponto a ponto, incluindo serviços e grupos ponto a ponto seguros.

## <a name="secure-peer-to-peer-groups"></a>Proteger grupos ponto a ponto

A [API de agrupamento](grouping-api.md) ponto a ponto combina o grafo ponto a ponto, o Identity Manager e as APIs do PNRP para formar uma solução coesa e conveniente para o desenvolvimento de aplicativos de rede ponto a ponto. A API de agrupamento ponto a ponto usa a API do Gerenciador de identidade ponto a ponto e um esquema de certificado autoassinado para garantir a segurança na infraestrutura de gráfico. Cada grupo pode ser resolvido e registrado por meio de PNRP, o que permite a resolução de nomes de pares aleatórios em um grupo de ponto a ponto registrado. Um grupo pode ser um ponto de extremidade em PNRP, assim como um par.

para obter uma visão geral da infraestrutura ponto a ponto, consulte o artigo "[introdução ao Windows XP ponto a ponto de rede](https://www.microsoft.com/windowsxp/pro/techinfo/administration/p2p/introduction.asp)".

Para obter uma visão geral das APIs na infraestrutura ponto a ponto, consulte o tópico [o que é a infraestrutura de mesmo nível?](what-is-the-peer-infrastructure-.md).

 

 




---
description: A infraestrutura de pares é um conjunto de várias APIs que são poderosas e flexíveis.
ms.assetid: aed7585a-88e5-4ca3-a8c3-e2ccfe13d35d
title: O que é a infraestrutura de pares?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873717b3f90497fe9ab9f50bb9c18e6f0692a4e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811304"
---
# <a name="what-is-the-peer-infrastructure"></a>O que é a infraestrutura de pares?

A infraestrutura de pares é um conjunto de várias APIs que são poderosas e flexíveis. Os principais componentes incluem o seguinte:

-   [API de grafo de pares](#peer-graphing-api)
-   [API de agrupamento de pares](#peer-grouping-api)
-   [API do Gerenciador de identidade do par](#peer-identity-manager-api)
-   [API do provedor de Namespace PNRP](#pnrp-namespace-provider-api)

## <a name="peer-graphing-api"></a>API de grafo de pares

A infraestrutura de pares fornece uma tecnologia de gráfico que pode passar informações de forma eficiente e confiável entre os pares de um grafo de mesmo nível. A [API de grafo de pares](graphing-api.md) garante que cada nó tenha uma exibição consistente dos dados em um grafo.

Você pode usar a [API de grafo de pares](graphing-api.md) para fazer o seguinte:

-   Criar e gerenciar grafos de pares
-   Enumerar e interagir com outros pares em um grafo de mesmo nível
-   Enviar dados na forma de um [registro](records.md) para cada nó em um grafo de mesmo nível

## <a name="peer-grouping-api"></a>API de agrupamento de pares

A [API de agrupamento de pares](grouping-api.md) combina e aprimora as APIs par de [PNRP](#pnrp-namespace-provider-api) e de [grafo](#peer-graphing-api) e adiciona os dois componentes a seguir:

-   Uma camada de multiplexação que permite que vários aplicativos em execução em uma entidade de mesmo nível se conectem a um grupo
-   Um modelo de segurança específico que garante que somente os colegas convidados para um grupo possam se conectar ao grupo por meio do tempo de vida do grupo

Você pode usar a API de agrupamento de pares para fazer o seguinte:

-   Criar e gerenciar grupos de pares seguros
-   Enumerar e interagir com outros pares em um grupo
-   Enviar dados na forma de um [registro](records.md) para cada nó em um grupo de pares

## <a name="peer-identity-manager-api"></a>API do Gerenciador de identidade do par

Usando a [API do Gerenciador de identidade do par](identity-manager-api.md) , você pode criar nomes de [pares](peer-names.md) seguros que o PNRP pode usar para garantir que uma pessoa que está publicando um nome oficialmente é o nome. Os nomes de pares também são chamados de identidades e são usados na API de agrupamento de pares para identificar os indivíduos em um grupo.

Você pode usar a [API do Gerenciador de identidade do par](identity-manager-api.md) para fazer o seguinte:

-   Crie, enumere e gerencie identidades pares.

## <a name="pnrp-namespace-provider-api"></a>API do provedor de Namespace PNRP

A infraestrutura de pares fornece uma tecnologia de resolução de nomes sem servidor chamada [API do provedor de namespace do PNRP](pnrp-namespace-provider-api.md). Usando a API do provedor de namespace do Winsock 2 PNRP, um ponto de extremidade, serviço, dispositivo de computação e ponto de extremidade do grupo de pontos pode gerenciar, registrar, cancelar o registro e resolver outro ponto de extremidade em uma [nuvem](clouds.md)PNRP.

> [!Note]  
> O PNRP é um acrônimo para o **protocolo de resolução de nomes de pares**.

 

 

 




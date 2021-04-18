---
description: Gerenciador de recursos de cartão inteligente
ms.assetid: 96434996-88fa-47d3-bb44-3ebb23610b27
title: Gerenciador de recursos de cartão inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3ee8e0bf311539863502d3e789544717e6dff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756572"
---
# <a name="smart-card-resource-manager"></a>Gerenciador de recursos de cartão inteligente

O [*Gerenciador de recursos*](../secgloss/r-gly.md) de [*cartão inteligente*](../secgloss/s-gly.md) gerencia o acesso a [*leitores*](../secgloss/r-gly.md) e a *cartões inteligentes*. Para gerenciar esses recursos, ele executa as seguintes funções.

-   Identifica e controla os recursos.
-   Aloca leitores e recursos em vários aplicativos.
-   Dá suporte a primitivos de [*transação*](../secgloss/t-gly.md) para acessar serviços disponíveis em um determinado cartão.
    > [!Note]  
    > Esse é um ponto importante porque os cartões atuais são dispositivos de thread único que geralmente exigem a execução de vários comandos para concluir uma única função. [*As transações*](../secgloss/t-gly.md) permitem que vários comandos sejam executados sem interrupção, garantindo que as informações de [*estado*](../secgloss/s-gly.md) intermediário não estejam corrompidas.

     

O Gerenciador de recursos pode ser acessado diretamente por meio da API do Resource Manager ou indiretamente por meio de qualquer [*provedor de serviço*](../secgloss/s-gly.md)de cartão inteligente.

A API do Gerenciador de recursos é um conjunto de funções do Windows que fornecem acesso direto aos serviços do Gerenciador de recursos. Para obter uma visão geral das funções do Windows fornecidas pela API, consulte [API do Gerenciador de recursos de cartão inteligente](smart-card-resource-manager-api.md). Em comparação, os provedores de serviço de cartão inteligente usam interfaces COM.

Muitas das funções do Windows na API do Gerenciador de recursos têm equivalentes nas propriedades e nos métodos das interfaces COM dos provedores de serviço de cartão inteligente. E, embora a maioria dos desenvolvedores de aplicativos encontre com mais facilidade para trabalhar, alguns aplicativos ainda precisarão usar as funções do Windows para executar determinadas tarefas. Por exemplo, os aplicativos que precisam manipular a lista de leitores ou grupos de leitor no [*banco de dados de cartão inteligente*](../secgloss/s-gly.md), e aqueles que precisam de controle direto de um leitor, devem usar a API do Gerenciador de recursos. Os serviços que fornecem esses recursos estão disponíveis apenas nas funções do Windows, não no COM fornecido pelos provedores de serviço.

Para obter informações sobre como o [*Gerenciador de recursos*](../secgloss/r-gly.md) é implementado no Windows, consulte implementação do [Resource Manager](resource-manager-implementation.md).

 

 

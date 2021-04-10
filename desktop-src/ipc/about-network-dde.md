---
description: O DDE de rede é usado para iniciar e manter as conexões de rede necessárias para conversas DDE entre aplicativos em execução em computadores diferentes em uma rede.
ms.assetid: f9eee391-2b4a-4c17-bea5-72cda5124e1c
title: Sobre o DDE de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 412971f6bef8d2782dce38b5aef413e4d073f6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296666"
---
# <a name="about-network-dde"></a>Sobre o DDE de rede

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]

O DDE de rede é usado para iniciar e manter as conexões de rede necessárias para conversas DDE entre aplicativos em execução em computadores diferentes em uma rede. Uma *conversa* DDE é a interação entre aplicativos cliente e servidor. Você usa o DDE de rede junto com o DDE e a DDEML (biblioteca de gerenciamento de DDE) em seu aplicativo.

O DDE é uma forma de comunicação entre processos que usa memória compartilhada para trocar dados entre aplicativos. Os aplicativos podem usar o DDE para transferências de dados de uma vez ou para trocas contínuas e atualizar dados. Para obter mais informações sobre o DDE, consulte [troca dinâmica de dados](../dataxchg/dynamic-data-exchange.md).

O DDEML simplifica a tarefa de adicionar capacidade de DDE a um aplicativo. Em vez de enviar, postar e processar mensagens DDE diretamente, um aplicativo usa as funções fornecidas pelo DDEML para gerenciar conversas DDE. Para obter mais informações sobre DDEML, consulte [troca dinâmica de dados biblioteca de gerenciamento](../dataxchg/dynamic-data-exchange-management-library.md).

## <a name="network-dde-files"></a>Arquivos DDE de rede

Para usar os elementos de API do DDE de rede, você deve incluir o arquivo de cabeçalho NDDEApi. h em seus arquivos de origem e incluir o arquivo NDDEApi. lib na linha de link. Você também deve verificar se o arquivo de NDDEApi.dll está carregado.

Para mais informações, consulte os seguintes tópicos:

-   [Agente DDE de rede](network-dde-agent.md)
-   [Compartilhamentos DDE](dde-shares.md)
-   [Compartilhamentos e segurança confiáveis](trusted-shares-and-security.md)
-   [Gerenciando compartilhamentos DDE](managing-dde-shares.md)

 

 

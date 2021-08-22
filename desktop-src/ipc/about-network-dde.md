---
description: O DDE de rede é usado para iniciar e manter as conexões de rede necessárias para conversas DDE entre aplicativos em execução em computadores diferentes em uma rede.
ms.assetid: f9eee391-2b4a-4c17-bea5-72cda5124e1c
title: Sobre o DDE de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeb8f232dc10080a575a6afe500727435bed7913ae95364daf697844c3c65dc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756452"
---
# <a name="about-network-dde"></a>Sobre o DDE de rede

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ NOT \_ IMPLEMENTED.\]

O DDE de rede é usado para iniciar e manter as conexões de rede necessárias para conversas DDE entre aplicativos em execução em computadores diferentes em uma rede. Uma conversa *de* DDE é a interação entre aplicativos cliente e servidor. Você usa o DDE de rede junto com o DDE e a DDEML (biblioteca de gerenciamento DDE) em seu aplicativo.

DDE é uma forma de comunicação entre processos que usa memória compartilhada para trocar dados entre aplicativos. Os aplicativos podem usar o DDE para transferências de dados uma vez ou para trocas contínuas e atualização de dados. Para obter mais informações sobre o DDE, [consulte Dados Dinâmicos Exchange](../dataxchg/dynamic-data-exchange.md).

O DDEML simplifica a tarefa de adicionar a funcionalidade DDE a um aplicativo. Em vez de enviar, postar e processar mensagens DDE diretamente, um aplicativo usa as funções fornecidas pelo DDEML para gerenciar conversas DDE. Para obter mais informações sobre DDEML, [consulte Dados Dinâmicos Exchange Management Library](../dataxchg/dynamic-data-exchange-management-library.md).

## <a name="network-dde-files"></a>Arquivos DDE de rede

Para usar os elementos de API do DDE de rede, você deve incluir o arquivo de título NDDEApi.h em seus arquivos de origem e incluir o arquivo NDDEApi.lib em sua linha de link. Você também deve certificar-se de que o arquivo NDDEApi.dll está carregado.

Para obter mais informações, consulte estes tópicos:

-   [Agente DDE de rede](network-dde-agent.md)
-   [Compartilhamentos DDE](dde-shares.md)
-   [Compartilhamentos confiáveis e segurança](trusted-shares-and-security.md)
-   [Gerenciando compartilhamentos DDE](managing-dde-shares.md)

 

 

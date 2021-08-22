---
title: Informações do conjunto de trabalho
description: O conjunto de trabalho de um processo é a quantidade de memória fisicamente mapeada para seu contexto de processo. O PSAPI permite que você tire instantâneos do conjunto de trabalho ou monitore o conjunto de trabalho.
ms.assetid: 33c42f79-cc77-4d44-84c3-8bf0a4a60019
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b6003886d50cb47b128bfce92cba4c28950ee078dbe13499d8909676d938aad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032974"
---
# <a name="working-set-information"></a>Informações do conjunto de trabalho

O conjunto de trabalho de um processo é a quantidade de memória fisicamente mapeada para seu contexto de processo. O PSAPI permite que você tire instantâneos do conjunto de trabalho ou monitore o conjunto de trabalho.

A [**função QueryWorkingSet**](/windows/desktop/api/Psapi/nf-psapi-queryworkingset) ou [**QueryWorkingSetEx**](/windows/desktop/api/Psapi/nf-psapi-queryworkingsetex) preenche um buffer com um instantâneo das informações para cada página no conjunto de trabalho atual do processo especificado. A função relata apenas as páginas que estão fisicamente presentes no momento exato em que ela é chamada.

Você pode usar o monitoramento do conjunto de trabalho para descobrir quanto RAM adicional uma operação específica leva (por exemplo, salvando um arquivo). Para começar a monitorar o conjunto de trabalho, chame a [**função InitializeProcessForWsWatch.**](/windows/desktop/api/Psapi/nf-psapi-initializeprocessforwswatch) Nem todos os processos permitem que você leia as informações do conjunto de trabalho, portanto, certifique-se de que a função retorne um valor não zero antes de continuar. Em seguida, chame a [**função GetWsChanges.**](/windows/desktop/api/Psapi/nf-psapi-getwschanges) Essa função relata apenas as páginas que foram carregadas na memória desde que você começou a monitorar o conjunto de trabalho. A função retorna dados em uma matriz de [**estruturas PSAPI \_ WS \_ WATCH \_ INFORMATION,**](/windows/desktop/api/Psapi/ns-psapi-psapi_ws_watch_information) uma estrutura para cada nova página adicionada ao conjunto de trabalho do processo. A estrutura informa quais páginas estão na memória e o que fez o sistema paginá-las.

A [**função EmptyWorkingSet**](/windows/desktop/api/Psapi/nf-psapi-emptyworkingset) assume um alçamento de processo. Ele remove o máximo de páginas possível do conjunto de trabalho do processo. Essa operação é útil principalmente para teste e ajuste. Observe que a [**função SetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsize) faz a mesma coisa se você passá-la -1 para os tamanhos mínimo e máximo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conjunto de Trabalho](/windows/desktop/Memory/working-set)
</dt> </dl>

 

 
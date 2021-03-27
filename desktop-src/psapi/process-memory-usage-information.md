---
title: Informações de uso de memória do processo
description: A função GetProcessMemoryInfo usa um identificador de processo como entrada e preenche uma \_ estrutura de contadores de memória de processo \_ com informações sobre as estatísticas de memória para o processo.
ms.assetid: 683c899e-a7e8-4440-8f13-2a713c1618bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133032b8cfb8a9af4ccea5661c9e0e0181ab4d93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822863"
---
# <a name="process-memory-usage-information"></a>Informações de uso de memória do processo

A função [**GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) usa um identificador de processo como entrada e preenche uma estrutura de [**\_ \_ contadores de memória de processo**](/windows/desktop/api/Psapi/ns-psapi-process_memory_counters) com informações sobre as estatísticas de memória para o processo. O membro **CB** recebe o tamanho da estrutura. O membro **PageFaultCount** recebe o número de falhas de página. Os membros restantes recebem o uso de memória atual e de pico nas seguintes categorias:

-   conjunto de trabalho
-   Pool Paginável
-   pool não paginável
-   Page

O *conjunto de trabalho* é a quantidade de memória mapeada fisicamente para o contexto do processo em um determinado momento. A memória no *pool paginável* é a memória do sistema que pode ser transferida para o arquivo de paginação no disco (paginável) quando não está sendo usada. A memória no *pool não paginável* é a memória do sistema que não pode ser paginada para o disco, desde que os objetos correspondentes sejam alocados. O uso de *arquivo de paginação* representa a quantidade de memória reservada para o processo no arquivo de paginação do sistema. Quando a utilização de memória é muito alta, as páginas do Gerenciador de memória virtual selecionam a memória no disco. Quando um thread precisa de uma página que não está na memória, o Gerenciador de memória o recarrega a partir do arquivo de paginação.

 

 





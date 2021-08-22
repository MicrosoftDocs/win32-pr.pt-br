---
title: Processar informações de uso de memória
description: A função GetProcessMemoryInfo assume um handle de processo como entrada e preenche uma estrutura PROCESS MEMORY COUNTERS com informações sobre as estatísticas de \_ \_ memória para o processo.
ms.assetid: 683c899e-a7e8-4440-8f13-2a713c1618bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac85a62853cf95dcf42380c76b914f23045152b32499870182a47ee2449e8ed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094698"
---
# <a name="process-memory-usage-information"></a>Processar informações de uso de memória

A [**função GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) assume um handle de processo como entrada e preenche uma estrutura [**PROCESS MEMORY \_ \_ COUNTERS**](/windows/desktop/api/Psapi/ns-psapi-process_memory_counters) com informações sobre as estatísticas de memória para o processo. O **membro cb** recebe o tamanho da estrutura. O **membro PageFaultCount** recebe o número de falhas de página. Os membros restantes recebem o uso de memória atual e de pico nas seguintes categorias:

-   conjunto de trabalho
-   pool de páginas
-   pool não papagado
-   Paginação

O *conjunto de* trabalho é a quantidade de memória fisicamente mapeada para o contexto do processo em um determinado momento. A memória no *pool pa páginado* é a memória do sistema que pode ser transferida para o arquivo de paging no disco (pa pageado) quando ele não está sendo usado. A memória no *pool não papagado* é a memória do sistema que não pode ser pa pageada no disco, desde que os objetos correspondentes sejam alocados. O *uso de pagefile* representa a memória que é reservado para o processo no arquivo de paging do sistema. Quando o uso de memória é muito alto, as páginas do gerenciador de memória virtual selecionam a memória para o disco. Quando um thread precisa de uma página que não está na memória, o gerenciador de memória o recarrega do arquivo de paging.

 

 





---
description: A diretriz recomendada é usar o menor número possível de threads, minimizando assim o uso de recursos do sistema.
ms.assetid: ed9bd3cf-b10c-49f9-bf62-7332517350b7
title: Considerações sobre multitarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec64bf1b7d59a42a1aec3511a72328f18bfaa88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091631"
---
# <a name="multitasking-considerations"></a>Considerações sobre multitarefas

A diretriz recomendada é usar o menor número possível de threads, minimizando assim o uso de recursos do sistema. Isso melhora o desempenho. A multitarefa tem requisitos de recursos e possíveis conflitos a serem considerados ao criar seu aplicativo. Os requisitos de recurso são os seguintes:

-   O sistema consome memória para as informações de contexto exigidas por processos e threads. Portanto, o número de processos e threads que podem ser criados é limitado pela memória disponível.
-   Manter o controle de um grande número de threads consome muito tempo do processador. Se houver muitos threads, a maioria deles não será capaz de fazer um progresso significativo. Se a maioria dos threads atuais estiver em um processo, os threads em outros processos serão agendados com menos frequência.

Fornecer acesso compartilhado a recursos pode criar conflitos. Para evitá-los, você deve sincronizar o acesso aos recursos compartilhados. Isso é verdadeiro para recursos do sistema (como portas de comunicação), recursos compartilhados por vários processos (como identificadores de arquivo) ou os recursos de um único processo (como variáveis globais) acessados por vários threads. Falha ao sincronizar o acesso corretamente (no mesmo ou em processos diferentes) pode levar a problemas como as condições de deadlock e de corrida. Os objetos de sincronização e as funções que você pode usar para coordenar o compartilhamento de recursos entre vários threads. Para obter mais informações sobre sincronização, consulte [sincronizando a execução de vários threads](synchronizing-execution-of-multiple-threads.md). Reduzir o número de threads torna mais fácil e mais eficaz sincronizar os recursos.

Um bom design para um aplicativo multi-threaded é o servidor de pipeline. Nesse design, você cria um thread por processador e cria filas de solicitações para as quais o aplicativo mantém as informações de contexto. Um thread processaria todas as solicitações em uma fila antes de processar solicitações na próxima fila.

 

 




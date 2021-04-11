---
description: O Agendador mantém uma fila de threads executáveis para cada nível de prioridade.
ms.assetid: 82463d71-9cef-4608-b997-25dc9c1e1c0a
title: Opções de Contexto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7628ee9e659cdbc2369b5f69d25847e8864dbd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169507"
---
# <a name="context-switches"></a>Opções de Contexto

O Agendador mantém uma fila de threads executáveis para cada nível de prioridade. Eles são conhecidos como *threads prontos*. Quando um processador fica disponível, o sistema executa uma *alternância de contexto*. As etapas em uma alternância de contexto são:

1.  Salve o contexto do thread que acabou de ser executado.
2.  Coloque o thread que acabou de ser executado no final da fila para sua prioridade.
3.  Localize a fila de prioridade mais alta que contém threads prontos.
4.  Remova o thread no cabeçalho da fila, carregue seu contexto e execute-o.

As classes de threads a seguir não são threads prontos.

-   Threads criados com o \_ sinalizador criar suspenso
-   Threads interrompidos durante a execução com a função [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) ou [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread)
-   Threads aguardando um objeto de sincronização ou entrada.

Até que os threads que estão suspensos ou bloqueados se tornem prontos para serem executados, o Agendador não aloca nenhum tempo de processador a eles, independentemente de sua prioridade.

Os motivos mais comuns para uma alternância de contexto são:

-   A fração de tempo esgotou.
-   Um thread com prioridade mais alta se tornou pronto para ser executado.
-   Um thread em execução precisa aguardar.

Quando um thread em execução precisa esperar, ele abandona o restante de sua fatia de tempo.

 

 

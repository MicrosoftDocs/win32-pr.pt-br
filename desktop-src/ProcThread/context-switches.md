---
description: O agendador mantém uma fila de threads executáveis para cada nível de prioridade.
ms.assetid: 82463d71-9cef-4608-b997-25dc9c1e1c0a
title: Opções de Contexto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c15f5d762525fd4a80030ea10e128e2c30a1ab914e9f17d0f954d80ecfd2e204
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143129"
---
# <a name="context-switches"></a>Opções de Contexto

O agendador mantém uma fila de threads executáveis para cada nível de prioridade. Eles são conhecidos como *threads prontos.* Quando um processador fica disponível, o sistema executa uma opção *de contexto*. As etapas em uma opção de contexto são:

1.  Salve o contexto do thread que acabou de ser executado.
2.  Coloque o thread que acabou de ser executado no final da fila para sua prioridade.
3.  Encontre a fila de prioridade mais alta que contém threads prontos.
4.  Remova o thread no início da fila, carregue seu contexto e execute-o.

As classes de threads a seguir não são threads prontos.

-   Threads criados com o sinalizador CREATE \_ SUSPENDED
-   Threads interrompidos durante a execução com a [**função SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) ou [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread)
-   Threads aguardando um objeto de sincronização ou entrada.

Até que os threads suspensos ou bloqueados se tornem prontos para ser executados, o agendador não aloca nenhum tempo do processador a eles, independentemente de sua prioridade.

Os motivos mais comuns para uma opção de contexto são:

-   A fatia de tempo decorrido.
-   Um thread com prioridade mais alta ficou pronto para ser executado.
-   Um thread em execução precisa aguardar.

Quando um thread em execução precisa aguardar, ele relincha o restante de sua fatia de tempo.

 

 

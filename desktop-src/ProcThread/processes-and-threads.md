---
description: Implemente multitarefa, agende prioridades e trabalhe com processos, threads, pools de threads, objetos de trabalho e fibra. Use o agendamento de modo de usuário para agendar threads.
ms.assetid: 6bff848c-0c55-41e7-aff1-84c6b21a1b8d
title: Processos e threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482f9f394001503350d4e213bd51e441ea43d073aacd8d10a49512e04404ba17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081306"
---
# <a name="processes-and-threads"></a>Processos e threads

Um aplicativo consiste em um ou mais processos. Um *processo*, nos termos mais simples, é um programa em execução. Um ou mais threads são executados no contexto do processo. Um *thread* é a unidade básica para a qual o sistema operacional aloca o tempo do processador. Um thread pode executar qualquer parte do código do processo, incluindo partes que estão sendo executadas atualmente por outro thread.

Um *objeto de trabalho* permite que grupos de processos sejam gerenciados como uma unidade. Os objetos de trabalho são objetos que podem ser encontrados, que podem ser controlados por objetos compartilháveis que controlam os atributos dos processos associados a eles. As operações executadas no objeto de trabalho afetam todos os processos associados ao objeto de trabalho.

Um *pool de threads* é uma coleção de threads de trabalho que executam retornos de chamada assíncronos com eficiência em nome do aplicativo. O pool de threads é usado principalmente para reduzir o número de threads de aplicativo e fornecer gerenciamento dos threads de trabalho.

Uma *fibra* é uma unidade de execução que deve ser agendada manualmente pelo aplicativo. As fibra são executados no contexto dos threads que as agendam.

*O UMS (agendamento de* modo de usuário) é um mecanismo leve que os aplicativos podem usar para agendar seus próprios threads. Os threads UMS diferem das [fibra,](fibers.md) já que cada thread UMS tem seu próprio contexto de thread em vez de compartilhar o contexto de thread de um único thread.

-   [Novidades em processos e threads](what-s-new-in-processes-and-threads.md)
-   [Sobre Processos e Threads](about-processes-and-threads.md)
-   [Usando processos e threads](using-processes-and-threads.md)
-   [Referência de processo e thread](process-and-thread-reference.md)

 

 




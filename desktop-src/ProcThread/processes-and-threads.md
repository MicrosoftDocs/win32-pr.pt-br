---
description: Implemente multitarefas, prioridades de agendamento e trabalhe com processos, threads, pools de threads, objetos de trabalho e fibras. Use o agendamento do modo de usuário para agendar threads.
ms.assetid: 6bff848c-0c55-41e7-aff1-84c6b21a1b8d
title: Processos e threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f469806a5f803910a773c78c9847d0f7b0ecc7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759607"
---
# <a name="processes-and-threads"></a>Processos e threads

Um aplicativo consiste em um ou mais processos. Um *processo*, nos termos mais simples, é um programa em execução. Um ou mais threads são executados no contexto do processo. Um *thread* é a unidade básica para a qual o sistema operacional aloca o tempo do processador. Um thread pode executar qualquer parte do código do processo, incluindo partes que estão sendo executadas atualmente por outro thread.

Um *objeto de trabalho* permite que grupos de processos sejam gerenciados como uma unidade. Os objetos de trabalho são objetos namable, protegíveis e compartilháveis que controlam os atributos dos processos associados a eles. As operações executadas no objeto de trabalho afetam todos os processos associados ao objeto de trabalho.

Um *pool de threads* é uma coleção de threads de trabalho que executam com eficiência retornos de chamada assíncronos em nome do aplicativo. O pool de threads é usado principalmente para reduzir o número de threads do aplicativo e fornecer gerenciamento dos threads de trabalho.

Uma *fibra* é uma unidade de execução que deve ser agendada manualmente pelo aplicativo. Os fibras são executados no contexto dos threads que os agendam.

O ums ( *agendamento de modo de usuário* ) é um mecanismo leve que os aplicativos podem usar para agendar seus próprios threads. Threads UMS diferem de [fibras](fibers.md) em que cada thread UMS tem seu próprio contexto de thread em vez de compartilhar o contexto de thread de um único thread.

-   [O que há de novo em processos e threads](what-s-new-in-processes-and-threads.md)
-   [Sobre Processos e Threads](about-processes-and-threads.md)
-   [Usando processos e threads](using-processes-and-threads.md)
-   [Processo e referência de thread](process-and-thread-reference.md)

 

 




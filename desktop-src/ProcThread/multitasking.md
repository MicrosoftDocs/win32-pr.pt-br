---
description: Um sistema operacional multitarefa divide o tempo de processador disponível entre os processos ou threads que precisam dele.
ms.assetid: ac45bef6-f078-40ac-95f4-06bd61ff46c4
title: Multitarefa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d06c1d8d44f397f06923c793971bcb20f35b2b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296742"
---
# <a name="multitasking"></a>Multitarefa

Um sistema operacional multitarefa divide o tempo de processador disponível entre os processos ou threads que precisam dele. O sistema foi projetado para a Preemptive multitarefas; Ele aloca uma *fatia de tempo* de processador para cada thread que executa. O thread atualmente em execução é suspenso quando sua fração de tempo expira, permitindo que outro thread seja executado. Quando o sistema alterna de um thread para outro, ele salva o contexto do thread admitido e restaura o contexto salvo do próximo thread na fila.

A duração da fração de tempo depende do sistema operacional e do processador. Como cada fração de tempo é pequena (aproximadamente 20 milissegundos), vários threads parecem estar sendo executados ao mesmo tempo. É esse o caso em sistemas de multiprocessador, em que os threads executáveis são distribuídos entre os processadores disponíveis. No entanto, é preciso ter cuidado ao usar vários threads em um aplicativo, pois o desempenho do sistema pode diminuir se houver muitos threads.

Para mais informações, consulte os seguintes tópicos:

-   [Vantagens da multitarefa](advantages-of-multitasking.md)
-   [Quando usar multitarefa](when-to-use-multitasking.md)
-   [Considerações sobre multitarefas](multitasking-considerations.md)

 

 




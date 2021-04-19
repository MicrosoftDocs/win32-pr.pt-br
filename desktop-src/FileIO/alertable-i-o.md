---
description: E/s de alerta é o método pelo qual os threads de aplicativo processam solicitações de e/s assíncronas somente quando estão em um estado de alerta.
ms.assetid: d996f1cc-eeab-456b-818b-5307a79effd9
title: E/s alertável
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb830dfadb97051c47b2472eb3e7a3c2d6a0bd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768767"
---
# <a name="alertable-io"></a>E/s alertável

E/s de alerta é o método pelo qual os threads de aplicativo processam solicitações de e/s assíncronas somente quando estão em um estado de alerta.

Para entender quando um thread está em um estado de alerta, considere o seguinte cenário:

1.  Um thread inicia uma solicitação de leitura assíncrona chamando [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) com um ponteiro para uma função de retorno de chamada.
2.  O thread inicia uma solicitação de gravação assíncrona chamando [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) com um ponteiro para uma função de retorno de chamada.
3.  O thread chama uma função que busca uma linha de dados de um servidor de banco de dado remoto.

Nesse cenário, as chamadas para [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) e [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) provavelmente serão retornadas antes da chamada de função na etapa 3. Quando isso ocorre, o kernel coloca os ponteiros para as funções de retorno de chamada na fila da APC (assíncrona de procedimento assíncrono) do thread. O kernel mantém essa fila especificamente para manter os dados de solicitação de e/s retornados até que possa ser processado pelo thread correspondente.

Quando a busca de linha é concluída e o thread retorna da função, sua prioridade mais alta é processar as solicitações de e/s retornadas na fila chamando as funções de retorno de chamada. Para fazer isso, ele deve inserir um estado de alerta. Um thread só pode fazer isso chamando uma das seguintes funções com os sinalizadores apropriados:

-   [**SleepEx**](/windows/desktop/api/synchapi/nf-synchapi-sleepex)
-   [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)
-   [**WaitForMultipleObjectsEx**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex)
-   [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait)
-   [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex)

Quando o thread entra em um estado alertado, ocorrem os seguintes eventos:

1.  O kernel verifica a fila da APC do thread. Se a fila contiver ponteiros de função de retorno de chamada, o kernel removerá o ponteiro da fila e o enviará para o thread.
2.  O thread executa a função de retorno de chamada.
3.  As etapas 1 e 2 são repetidas para cada ponteiro restante na fila.
4.  Quando a fila está vazia, o thread retorna da função que a colocou em um estado de alerta.

Nesse cenário, depois que o thread entrar em um estado de alerta, ele chamará as funções de retorno de chamada enviadas para [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) e [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex), em seguida, retornará da função que a colocou em um estado de alerta.

Se um thread entrar em um estado alertado enquanto sua fila da APC estiver vazia, a execução do thread será suspensa pelo kernel até que ocorra um dos seguintes:

-   O objeto de kernel que está sendo aguardado é sinalizado.
-   Um ponteiro de função de retorno de chamada é colocado na fila da APC.

Um thread que usa e/s alerta solicitações de e/s assíncronas com mais eficiência do que quando simplesmente aguarda o sinalizador de evento na estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) ser definido, e o mecanismo de e/s alertado é menos complicado do que [as portas de conclusão de e/s](i-o-completion-ports.md) a serem usadas. No entanto, a e/s alertável retorna o resultado da solicitação de e/s somente para o thread que a iniciou. As portas de conclusão de e/s não têm essa limitação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Chamadas de procedimento assíncrono](/windows/desktop/Sync/asynchronous-procedure-calls)
</dt> </dl>

 

 

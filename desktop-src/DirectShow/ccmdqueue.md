---
description: A classe CCmdQueue é uma classe base que fornece uma fila de objetos CDeferredCommand e funções membro para adicionar, remover, verificar o status e invocar os comandos na fila.
ms.assetid: 6bd0f0f3-3c56-47d2-9fd8-e2863a2afa33
title: Classe CCmdQueue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5aac6f7315df58a39d119c72fc481816bdc40aab3c449852041b7a490f22f44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074400"
---
# <a name="ccmdqueue-class"></a>Classe CCmdQueue

A classe é uma classe base que fornece uma fila de `CCmdQueue` [**objetos CDeferredCommand**](cdeferredcommand.md) e funções membro para adicionar, remover, verificar status e invocar os comandos na fila. Um `CCmdQueue` objeto é uma parte de um objeto que implementa métodos [**IQueueCommand.**](/windows/desktop/api/Control/nn-control-iqueuecommand) O gerenciador de grafo de filtro implementa **métodos IQueueCommand** para que os aplicativos possam enfileirar comandos para o grafo de filtro. Os filtros que implementam a interface **IQueueCommand** usam essa classe diretamente. Se você quiser usar **objetos CDeferredCommand,** sua fila deverá ser derivada dessa classe.

Há dois modos de sincronização: grosseira e precisa. No modo de grosseria, o aplicativo aguarda até que uma hora especificada chegue e, em seguida, execute o comando . No modo preciso, o aplicativo aguarda até que o processamento comece no exemplo que aparece no momento e, em seguida, executa o comando . O filtro determina qual deles será implementado. O gerenciador de grafo de filtro sempre implementa o modo de grosseria para comandos que estão na fila no gerenciador de grafo de filtro.

Se você quiser sincronização grosseira, provavelmente deseja aguardar até que haja um comando devido e, em seguida, executá-lo. Você pode fazer isso chamando [**CCmdQueue::GetDueCommand.**](ccmdqueue-getduecommand.md) Se você tiver várias coisas para aguardar, obter o handle de evento de [**CCmdQueue::GetDueHandle**](ccmdqueue-getduehandle.md) e, em seguida, chame **CCmdQueue::GetDueCommand** quando isso for sinalizado. [**O tempo de**](stream-time.md) fluxo avançará apenas entre as chamadas para as funções de membro [**CCmdQueue::Run**](ccmdqueue-run.md) e [**CCmdQueue::EndRun.**](ccmdqueue-endrun.md) Não há nenhuma garantia de que, se o handle estiver definido, haverá um comando pronto. Sempre que o evento for sinalizado, chame a função de membro **GetDueCommand** (provavelmente com um tempo fora de zero); isso poderá retornar E \_ ABORT se nenhum comando estiver pronto.

Se você quiser sincronização precisa, chame a função membro [**CCmdQueue::GetCommandDueFor**](ccmdqueue-getcommandduefor.md) e passe os exemplos que você está prestes a processar como um parâmetro. Isso retorna o seguinte:

-   Um comando de tempo de fluxo devido a ou antes dessa hora de fluxo.
-   Um comando de tempo de apresentação devido a ou antes da apresentação da hora do fluxo. Faça isso somente entre as funções de membro [**CCmdQueue::Run**](ccmdqueue-run.md) e [**CCmdQueue::EndRun,**](ccmdqueue-endrun.md) porque, fora disso, o mapeamento do tempo de fluxo para o tempo de apresentação não é conhecido.
-   Qualquer comando de tempo de apresentação deve ser agora.

Se você quiser sincronização precisa para exemplos que podem ser processados durante o modo em pausa, use comandos de tempo de fluxo.

Em todos os casos, os comandos permanecem na fila até que seja chamado ou cancelado. A configuração e a redefinição do identificador de evento são totalmente gerenciadas por esse objeto de fila.



| Membros de Dados Protegidos                                 | Descrição                                                                                            |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| m \_ bRunning                                            | Sinalizador para estado de execução; definir **TRUE ao** executar.                                                     |
| m \_ dwAdvise                                            | Informe o identificador do relógio de referência (zero se não for um alerta pendente).                            |
| m \_ evDue                                               | Define a hora em que qualquer comando é devido.                                                               |
| m \_ listPresentation                                    | Armazena comandos na fila no tempo de apresentação.                                                           |
| m \_ listStream                                          | Armazena comandos na fila em tempo de fluxo.                                                                 |
| bloqueio \_ m                                                | Protege o acesso a listas.                                                                              |
| m \_ pClock                                              | Relógio de referência atual.                                                                               |
| m \_ StreamTimeOffset                                    | Contém o deslocamento de tempo de fluxo **quando m \_ bRunning** é **TRUE.**                                      |
| m \_ StreamTimeOffset                                    | Contém o deslocamento de tempo de fluxo **quando m \_ bRunning** é **TRUE.**                                      |
| Funções de membro                                       | Descrição                                                                                            |
| [**CCmdQueue**](ccmdqueue-ccmdqueue.md)               | Constrói um **objeto CCmdQueue.**                                                                     |
| [**CheckTime**](ccmdqueue-checktime.md)               | Determina se um determinado tempo é devido.                                                                     |
| [**GetDueHandle**](ccmdqueue-getduehandle.md)         | Recupera o alça de evento que será sinalizado.                                                      |
| Funções de membro que podem ser substituídos                           | Descrição                                                                                            |
| [**Endrun**](ccmdqueue-endrun.md)                     | Alterna para o modo parado ou em pausa.                                                                    |
| [**GetCommandDueFor**](ccmdqueue-getcommandduefor.md) | Recupera um comando adiado agendado em um momento especificado.                                    |
| [**GetDueCommand**](ccmdqueue-getduecommand.md)       | Recupera um ponteiro para o próximo comando que é devido.                                                   |
| [**Inserir**](ccmdqueue-insert.md)                     | Adiciona o [**objeto CDeferredCommand**](cdeferredcommand.md) à fila.                             |
| [**Novo**](ccmdqueue-new.md)                           | Inicializa um comando a ser executado e retorna um novo [**objeto CDeferredCommand.**](cdeferredcommand.md) |
| [**Remover**](ccmdqueue-remove.md)                     | Remove o [**objeto CDeferredCommand**](cdeferredcommand.md) da fila.                        |
| [**Executar**](ccmdqueue-run.md)                           | Alterna para o modo de execução.                                                                              |
| [**SetSyncSource**](ccmdqueue-setsyncsource.md)       | Define o relógio usado para o tempo.                                                                        |
| [**SetTimeAdvise**](ccmdqueue-settimeadvise.md)       | Configura um evento de temporizador com o relógio de referência.                                                        |



 

 

 




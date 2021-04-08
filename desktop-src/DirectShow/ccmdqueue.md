---
description: A classe CCmdQueue é uma classe base que fornece uma fila de objetos CDeferredCommand e funções de membro para adicionar, remover, verificar o status e invocar os comandos em fila.
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
ms.openlocfilehash: 78af7a975d54ba832bbdf1fb7f8027f87b747660
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087354"
---
# <a name="ccmdqueue-class"></a>Classe CCmdQueue

A `CCmdQueue` classe é uma classe base que fornece uma fila de objetos [**CDeferredCommand**](cdeferredcommand.md) e funções de membro para adicionar, remover, verificar o status e invocar os comandos em fila. Um `CCmdQueue` objeto é uma parte de um objeto que implementa os métodos [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) . O Gerenciador de gráfico de filtro implementa métodos **IQueueCommand** para que os aplicativos possam enfileirar comandos para o grafo de filtro. Filtros que implementam a interface **IQueueCommand** diretamente usam essa classe. Se você quiser usar objetos **CDeferredCommand** , sua fila deverá ser derivada dessa classe.

Há dois modos de sincronização: grande e preciso. Em modo grosso, o aplicativo aguarda até que um tempo especificado chegue e, em seguida, execute o comando. Em modo preciso, o aplicativo aguarda até que o processamento comece no exemplo que aparece no momento e, em seguida, execute o comando. O filtro determina qual deles será implementado. O Gerenciador de gráfico de filtro sempre implementa o modo grosso para comandos que são enfileirados no Gerenciador de gráficos de filtro.

Se você quiser uma sincronização grosseira, provavelmente desejará aguardar até que haja um comando devido e, em seguida, executá-lo. Você pode fazer isso chamando [**CCmdQueue:: GetDueCommand**](ccmdqueue-getduecommand.md). Se você tiver várias coisas a aguardar, obtenha o identificador de evento de [**CCmdQueue:: GetDueHandle**](ccmdqueue-getduehandle.md) e, em seguida, chame **CCmdQueue:: GetDueCommand** quando isso for sinalizado. o [**tempo de transmissão**](stream-time.md) avançará apenas entre chamadas para as funções de membro [**CCmdQueue:: Run**](ccmdqueue-run.md) e [**CCmdQueue:: EndRun**](ccmdqueue-endrun.md) . Não há nenhuma garantia de que, se o identificador for definido, haverá um comando pronto. Cada vez que o evento é sinalizado, chame a função de membro **GetDueCommand** (provavelmente com um tempo limite de zero); Isso pode retornar E \_ abortar se nenhum comando estiver pronto.

Se você quiser uma sincronização precisa, chame a função de membro [**CCmdQueue:: GetCommandDueFor**](ccmdqueue-getcommandduefor.md) e passe os exemplos que você está prestes a processar como um parâmetro. Isso retorna o seguinte:

-   Um comando de tempo de fluxo devido à hora do fluxo ou antes dela.
-   Um comando de tempo de apresentação devido à apresentação do horário do fluxo ou antes dela. Faça isso somente entre as funções de membro [**CCmdQueue:: Run**](ccmdqueue-run.md) e [**CCmdQueue:: EndRun**](ccmdqueue-endrun.md) , porque fora disso, o mapeamento do tempo de transmissão para o tempo de apresentação não é conhecido.
-   Qualquer comando de tempo de apresentação devido ao momento.

Se você quiser uma sincronização precisa para exemplos que possam ser processados durante o modo de pausa, você deve usar comandos de tempo de transmissão.

Em todos os casos, os comandos permanecem na fila até que sejam chamados ou cancelados. A configuração e a redefinição do identificador de eventos são totalmente gerenciadas por esse objeto de fila.



| Membros de Dados Protegidos                                 | Descrição                                                                                            |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| \_bRunning m                                            | Sinalizador para estado de execução; Defina **true** ao executar.                                                     |
| \_dwAdvise m                                            | Identificador de aviso do relógio de referência (zero se não houver aviso pendente).                            |
| \_evDue m                                               | Define a hora em que os comandos são devidos.                                                               |
| \_listPresentation m                                    | Armazena comandos enfileirados em tempo de apresentação.                                                           |
| \_listStream m                                          | Armazena comandos enfileirados em tempo de transmissão.                                                                 |
| bloqueio de m \_                                                | Protege o acesso a listas.                                                                              |
| \_pClock m                                              | Relógio de referência atual.                                                                               |
| \_StreamTimeOffset m                                    | Contém o deslocamento de tempo do fluxo quando **m \_ BRunning** é **verdadeiro**.                                      |
| \_StreamTimeOffset m                                    | Contém o deslocamento de tempo do fluxo quando **m \_ BRunning** é **verdadeiro**.                                      |
| Funções de membro                                       | Descrição                                                                                            |
| [**CCmdQueue**](ccmdqueue-ccmdqueue.md)               | Constrói um objeto **CCmdQueue** .                                                                     |
| [**Checktime**](ccmdqueue-checktime.md)               | Determina se um determinado tempo é devido.                                                                     |
| [**GetDueHandle**](ccmdqueue-getduehandle.md)         | Recupera o identificador de evento que será sinalizado.                                                      |
| Funções de membro substituíveis                           | Descrição                                                                                            |
| [**EndRun**](ccmdqueue-endrun.md)                     | Alterna para o modo parado ou pausado.                                                                    |
| [**GetCommandDueFor**](ccmdqueue-getcommandduefor.md) | Recupera um comando adiado que está agendado em um horário especificado.                                    |
| [**GetDueCommand**](ccmdqueue-getduecommand.md)       | Recupera um ponteiro para o próximo comando que está vencido.                                                   |
| [**Inserido**](ccmdqueue-insert.md)                     | Adiciona o objeto [**CDeferredCommand**](cdeferredcommand.md) à fila.                             |
| [**Novo**](ccmdqueue-new.md)                           | Inicializa um comando a ser executado e retorna um novo objeto [**CDeferredCommand**](cdeferredcommand.md) . |
| [**Remover**](ccmdqueue-remove.md)                     | Remove o objeto [**CDeferredCommand**](cdeferredcommand.md) da fila.                        |
| [**Executar**](ccmdqueue-run.md)                           | Alterna para o modo de execução.                                                                              |
| [**Setsynce**](ccmdqueue-setsyncsource.md)       | Define o relógio usado para o tempo.                                                                        |
| [**SetTimeAdvise**](ccmdqueue-settimeadvise.md)       | Configura um evento de temporizador com o relógio de referência.                                                        |



 

 

 




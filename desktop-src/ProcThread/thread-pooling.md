---
description: Há muitos aplicativos que criam threads que passam muito tempo no estado de suspensão aguardando a ocorrência de um evento.
ms.assetid: a5e52080-35d4-47f5-9050-90889e3bf2f8
title: Pooling de thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf3565401dc57b077e333043861d42b683e810c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828354"
---
# <a name="thread-pooling"></a>Pooling de thread

Há muitos aplicativos que criam threads que passam muito tempo no estado de suspensão aguardando a ocorrência de um evento. Outros threads podem entrar em estado de suspensão apenas para serem despertados periodicamente para sondar informações de status de alteração ou atualização. O *pool de threads* permite que você use threads com mais eficiência, fornecendo ao aplicativo um pool de threads de trabalho que são gerenciados pelo sistema. Pelo menos um thread monitora o status de todas as operações de espera enfileiradas para o pool de threads. Quando uma operação de espera for concluída, um thread de trabalho do pool de threads executará a função de retorno de chamada correspondente.

Este tópico descreve a API do pool de threads original. A API do pool de threads introduzida no Windows Vista é mais simples, mais confiável, tem melhor desempenho e fornece mais flexibilidade para os desenvolvedores. Para obter informações sobre a API do pool de threads atual, consulte [pools de threads](thread-pools.md).

Você também pode enfileirar itens de trabalho que não estão relacionados a uma operação de espera para o pool de threads. Para solicitar que um item de trabalho seja manipulado por um thread no pool de threads, chame a função [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) . Essa função usa um parâmetro para a função que será chamada pelo thread selecionado no pool de threads. Não é possível cancelar um item de trabalho após ele ter sido enfileirado.

[Temporizador-temporizadores de fila](../sync/timer-queues.md) e [operações de espera registradas](../sync/wait-functions.md) também usam o pool de threads. Suas funções de retorno de chamada são enfileiradas para o pool de threads. Você também pode usar a função [**BindIoCompletionCallback**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback) para postar operações de e/s assíncronas. Na conclusão da e/s, o retorno de chamada é executado por um thread do pool de threads.

O pool de threads é criado na primeira vez que você chama [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) ou [**BindIoCompletionCallback**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback), ou quando um timer de fila de temporizador ou uma operação de espera registrada enfileira uma função de retorno de chamada. Por padrão, o número de threads que podem ser criados no pool de threads é de cerca de 500. Cada thread usa o tamanho de pilha padrão e é executado com a prioridade padrão.

Há dois tipos de threads de trabalho no pool de threads: e/s e não-e/s. Um *thread de trabalho de e/s* é um thread que aguarda um estado de espera alertável. Os itens de trabalho são enfileirados em threads de trabalho de e/s como APC (chamadas de procedimento assíncrono). Você deve enfileirar um item de trabalho para um thread de trabalho de e/s se ele deve ser executado em um thread que aguarda um estado de alerta.

Um *thread de trabalho que não é de e/s* aguarda em portas de conclusão de e/s. Usar threads de trabalho que não são de e/s é mais eficiente do que usar threads de trabalho de e/s. Portanto, você deve usar threads de trabalho que não sejam de e/s sempre que possível. Os threads de trabalho de e/s e não de e/s não serão encerrados se houver solicitações de e/s assíncronas pendentes. Ambos os tipos de threads podem ser usados por itens de trabalho que iniciam solicitações de conclusão de e/s assíncronas. No entanto, evite postar solicitações de conclusão de e/s assíncrona em threads de trabalho que não sejam de e/s se demorarem muito tempo para serem concluídas.

Para usar o pool de threads, os itens de trabalho e todas as funções que eles chamam devem ser seguros ao pool de threads. Uma função segura não pressupõe que o thread que a executa é um thread dedicado ou persistente. Em geral, você deve evitar usar o [armazenamento local de thread](thread-local-storage.md) ou fazer uma chamada assíncrona que exija um thread persistente, como a função [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) . No entanto, essas funções podem ser chamadas em um thread dedicado (criado pelo aplicativo) ou enfileiradas em um thread de trabalho persistente (usando [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) com a \_ opção WT EXECUTEINPERSISTENTTHREAD).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[E/s alertável](../fileio/alertable-i-o.md)
</dt> <dt>

[Chamadas de procedimento assíncrono](../sync/asynchronous-procedure-calls.md)
</dt> <dt>

[Portas de conclusão de e/s](../fileio/i-o-completion-ports.md)
</dt> <dt>

[Pools de threads](thread-pools.md)
</dt> </dl>

 

 
